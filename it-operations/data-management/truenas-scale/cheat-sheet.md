# Cheat sheet

## Drives

### Wipe Drive

```
dd if=/dev/urandom of=/dev/sdX bs=1M status=progress
```

### Format Drive

#### Format Drive

```
sudo sg_format --format --ffmt=1 --size=512 /dev/sdX
```

#### Check Progress

```
sudo sg_requests /dev/sdX
```

### Drive Testing

#### Short SMART Test

```
sudo smartctl -t short /dev/sdX
```

#### Long  SMART Test

```
sudo smartctl -t long /dev/sdX
```

#### Check SMART Results

```
sudo smartctl -a /dev/sdX
```

#### BadBlock Stress Test

{% hint style="warning" %}
This is a destructive test and will destroy all data on the disk
{% endhint %}

```
badblocks -b 4096 -c 65535 -wsv /dev/sdX > /mnt/tank/badblocks-$(basename /dev/sdX).log
```

#### ZFS Scrub Test

```
zpool scrub TESTR001
```

#### Check ZFS Scrub Test Results

```
zpool status TESTR001
```

### Drive Information

#### Display name, model, serial, physical and logical sector sizes

```
lsblk -o NAME,MODEL,SERIAL,SIZE,PHY-SEC,LOG-SEC -b | sort -k4 -n
```

#### SMART attributes

```
smartctl -a /dev/sdX
```

#### Identify drive model

```
udevadm info --query=all --name=/dev/sdX | grep ID_MODEL
```

#### Identify physical drive location

```
dd if=/dev/da1 of=/dev/null bs=1048576
```

## Datasets

### Dataset Usage

```
zfs list -o space Pool/Dataset
```

## Pools

### Pool Usage

```
zfs list -o space Pool
```
