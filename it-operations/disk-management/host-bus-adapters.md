# Host Bus Adapters

When using a Host Bus Adapter (HBA) in a system that relies on software-managed redundancy, such as a NAS or server running ZFS, it is highly recommended that the HBA be flashed to IT Mode (Initiator Target mode). This mode disables any hardware RAID functionality and ensures that the operating system has direct, unaltered access to each individual drive. This is crucial for ZFS, which handles redundancy, integrity checking, and data repair entirely in software. If the HBA abstracts or modifies drive behavior, it can interfere with ZFS's ability to detect and correct data corruption, undermining the reliability of the entire storage pool. By using IT Mode, the system gains full visibility and control over every disk, enabling ZFS to manage its advanced features, such as checksumming, copy-on-write, RAID-Z, and self-healing capabilities, without interference. This setup is ideal for platforms like TrueNAS, Proxmox, or Linux servers where ZFS is used for robust, fault-tolerant storage.

## 8 Internal Drive Controllers

| Generation | Model   | Controller | PCIe Interface | SAS Speed    | Idle Power | Load Power | IOPS    |
| ---------- | ------- | ---------- | -------------- | ------------ | ---------- | ---------- | ------- |
| 2nd Gen    | 9211-8i | SAS2008    | PCIe 2.0 x8    | SAS2 6 Gb/s  | 7w         | 8w         | ≥ 320K  |
| 3rd Gen    | 9207-8i | SAS2308    | PCIe 3.0 x8    | SAS2 6 Gb/s  | 9w         | 10w        | ≥ 650K  |
| 4th Gen    | 9300-8i | SAS3008    | PCIe 3.0 x8    | SAS3 12 Gb/s | 11w        | 12w        | ≥ 1000K |
| 6th Gen    | 9400-8i | SAS3408    | PCIe 4.0 x8    | SAS3 12 Gb/s | 6w         | 7w         | ≥ 1.5M  |
| 7th Gen    | 9500-8i | SAS3808    | PCIe 4.0 x8    | SAS3 12 Gb/s | 4w         | 6w         | ≥ 3M    |

## 16 Internal Drive Controllers

| Generation | Model    | Controller            | PCIe Interface | SAS Speed    | Idle Power | Load Power | IOPS   |
| ---------- | -------- | --------------------- | -------------- | ------------ | ---------- | ---------- | ------ |
| 2nd Gen    | 9201-16i | SAS2116               | PCIe 2.0 x8    | SAS2 6 Gb/s  | 13w        | 15w        | ≥ 430K |
| 4th Gen    | 9300-16i | dual SAS3008 with PLX | PCIe 3.0 x8    | SAS2 12 Gb/s | 24w        | 25w        | ≥ 2M   |
| 5th Gen    | 9305-16i | SAS3224               | PCIe 3.0 x8    | SAS3 12 Gb/s | 13w        | 14w        | ≥ 1.5M |
| 6th Gen    | 9400-16i | SAS3416               | PCIe 3.0 x8    | SAS3 12 Gb/s | 8w         | 9w         | ≥ 1.5M |
| 7th Gen    | 9500-16i | SAS3816               | PCIe 4.0 x8    | SAS3 12 Gb/s | 6w         | 8w         | ≥ 3M   |
