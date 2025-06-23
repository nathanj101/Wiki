# ZFS Pool Migration

ZFS does not support renaming a pool while it is mounted, and the `zfs rename` command cannot be used for this purpose. However, you can safely rename a ZFS pool by exporting it and re-importing it under a new name. This method is commonly used after migrating data to a new pool and wanting to retain the original pool name to avoid reconfiguring shares or services.

## Common Use Case

This process is typically used when:

1. A new pool (e.g., `vaulttemp`) is created with a different set of disks or layout.
2. Data is replicated from the existing pool (e.g., `vault`) to the new one.
3. The original pool is destroyed.
4. The new pool is renamed to take on the original pool’s name (`vault`).

## Copy Data to a New Pool Before Renaming

If you're migrating from an old pool to a new one (e.g., `vault` to `vaulttemp`) and plan to rename the new one:

1. Create the new pool (`vaulttemp`).
2. Copy data from the old pool:

```bash
rsync -a --info=progress2 /mnt/vault/ /mnt/vaulttemp/
```

3. Verify the data:

```bash
diff -qr /mnt/vault /mnt/vaulttemp
```

4. Stop any services or jails using the old pool.
5. Export and destroy the old pool:

```bash
zpool export vault
zpool destroy vault
```

6. Export the new pool:

```bash
zpool export vaulttemp
```

7. Import it under the original name:

```bash
zpool import vaulttemp vault
```

8. Confirm datasets are accessible under `/mnt/vault`.

## Renaming Pool

### 1. Move the System Dataset (If Necessary)

If the system dataset is hosted on the pool you wish to rename:

1. Go to **System > System Dataset** in the GUI.
2. Choose a different pool (or the boot pool) from the dropdown.
3. Click **Save**.

### 2. Export the Pool from the GUI

1. Navigate to **Storage > Pools**.
2. Click the gear icon next to the pool you want to rename.
3. Choose **Export/Disconnect**.
4. Ensure **"Destroy data on this pool?"** is **not** checked.
5. Check **"Confirm Export/Disconnect"**.
6. Click **EXPORT/DISCONNECT**.

### 3. Import the Pool with a New Name

Use the following command to import the pool under a new name:

```bash
zpool import oldpoolname newpoolname
```

Verify the import:

```bash
zpool status
```

### 4. Export the Renamed Pool

Before importing it into the GUI, export the pool again via CLI:

```bash
zpool export newpoolname
```

### 5. Import the Renamed Pool in the GUI

1. Go to **Storage > Pools**.
2. Click **Add**.
3. Select **Import an existing pool**.
4. Choose the renamed pool (`vault`).
5. Follow the prompts to complete the import.

