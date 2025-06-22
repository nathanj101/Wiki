# Solid state drive

When selecting a solid-state drive (SSD), the right choice depends heavily on whether you're installing it in a server or enterprise environment, or simply using it in a desktop or personal laptop. In server or data centre environments, SSDs are subjected to sustained heavy workloads, so it is important to choose a drive that is rated for high endurance, consistent performance, and long-term reliability. These are typically enterprise-grade SSDs with features such as power-loss protection, high TBW (terabytes written), and consistent IOPS under load. In contrast, for typical home or desktop use, such as gaming, general productivity, or light media editing, a consumer-grade SSD will usually provide more than enough speed and responsiveness, with the added benefit of being more cost-effective. While endurance ratings are still relevant, most users in a desktop setting are unlikely to exceed the write limits of a well-sized consumer SSD during the drive’s useful life.

## Home

<table data-full-width="false"><thead><tr><th width="159.40185546875">Device</th><th>Purpose</th><th>Protocol</th><th>NAND Type</th><th>Endurance</th><th>DRAM Cache</th><th>PLP</th></tr></thead><tbody><tr><td>Desktop PC</td><td>Boot</td><td>NVMe</td><td>TLC</td><td>0.3 – 0.5 DWPD</td><td>Yes</td><td>No</td></tr><tr><td>Desktop PC</td><td>Games</td><td>NVMe</td><td>TLC</td><td>0.3 – 0.5 DWPD</td><td>Yes, but not essential</td><td>No</td></tr><tr><td>Desktop PC</td><td>Media</td><td>NVMe</td><td>QLC</td><td>0.1 DWPD</td><td>No</td><td>No</td></tr></tbody></table>

## Production

| Purpose         | DWPD Range                 | Recommended model                                                                                                                                                                         |
| --------------- | -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Mixed usage     | Typically > 1 and ≤ 3 DWPD | <ul><li>Micron 5300 MAX</li><li>Intel S4600</li><li>Intel D3‑S4610</li><li>Intel S3610</li><li>Samsung SM883</li><li>Samsung SM863a</li><li>Samsung PM897</li><li>Samsung SM863</li></ul> |
| Write-intensive | Typically > 3 DWPD         | <ul><li>Intel S3710</li><li>Intel S3700</li></ul>                                                                                                                                         |
| Read-intensive  | Typically ≤ 1 DWPD         | <ul><li>Intel D3‑S4510</li><li>Samsung PM863</li><li>Samsung PM883</li></ul>                                                                                                              |
