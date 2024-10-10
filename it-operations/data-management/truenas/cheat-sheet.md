# Cheat sheet

## Wipe Drive

```
dd if=/dev/urandom of=/dev/da0 bs=1M status=progress
```

## Dataset Usage

```
zfs list -o space Pool/Dataset
```

## Pool Usage

```
zfs list -o space Pool
```

## Identify Drive Location

```
dd if=/dev/da1 of=/dev/null bs=1048576
```

## Disk SMART Info

```
smartctl -a /dev/daX
```

## Disk Model Identification

```
camcontrol devlist
```
