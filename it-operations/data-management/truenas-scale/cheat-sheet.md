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

### Drive Information

#### Display name, model, serial, physical and logical sector sizes

```
lsblk -o NAME,MODEL,SERIAL,SIZE,PHY-SeC,LOG-SeC
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
