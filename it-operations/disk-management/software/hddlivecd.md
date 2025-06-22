# HDDLiveCD

## Introduction <a href="#introduction" id="introduction"></a>

HDDLiveCD is a powerful and versatile tool designed for managing and troubleshooting hard drives and file systems. This bootable live CD (Xubuntu) environment enables users to perform a variety of tasks without the need for an installed operating system.&#x20;

**Key features of HDDLiveCD include:**

* **HDDSuperClone**: A tool used for cloning damaged or failing hard drives. It aims to maximize data recovery by handling bad sectors and other drive errors.
* **HDDSCViewer**: A viewer for HDDSuperClone logs, providing detailed insights into the cloning process and any errors encountered.
* **smartmontools**: A package containing utilities to control and monitor storage systems using the SMART (Self-Monitoring, Analysis, and Reporting Technology) system built into most modern ATA and SCSI hard disks.
* **gparted**: A graphical partition editor for creating, reorganizing, and deleting disk partitions.

## Installation <a href="#installation" id="installation"></a>

**Requirements:**

* Empty USB Flash Drive (2GB or larger)
* Functional computer running Windows or Linux

**Installation:**

1. Download the HDDLiveCD.iso file from [HDDSuperClone's official Google Drive](https://www.hddsuperclone.com/hddlivecd). In almost all cases, you should choose "xubuntu-18.04.5-desktop-hddlive.2022\_07\_24.x64.1.5G.iso", this supports all 64-bit, modern systems. The alternate file "xubuntu-14.04.5-desktop-hddlive.2022\_07\_24.x86.943M.iso", is intended for 32-bit machines.
2. Download Rufus from the [official website](https://rufus.ie/en/).
3. Open Rufus and select your HDDLiveCD.iso file and destination USB.
4. Click ‘start’ and wait for the .iso to be written to the USB.
5. Connect the USB drive to your computer, which has the drives to be rescued attached, and set the USB drive as the boot device in the BIOS boot priority.

## Usage <a href="#usage" id="usage"></a>

### Compatibility <a href="#compatibility" id="compatibility"></a>

* Don't use USB to connect any drives.
* Don't use on any drive which shows physical signs of damage i.e. clicking, buzzing, damaged case
* Connect drives using either SATA, IDE or M.2
* For any device which is not SATA or IDE, you must set 'Mode' setting to 'Generic Source Device'.

### Cloning Hard Drives and SSDs <a href="#cloning-hard-drives-and-ssds" id="cloning-hard-drives-and-ssds"></a>

A **clone** refers to a direct disk-to-disk copy, where sectors from Disk A are copied to Disk B at the same offsets, creating an identical replica of the source drive. This process overwrites any data on the destination drive and replaces its partitioning with that of the source drive. Cloning requires the destination drive to be equal to or larger than the source drive in size.

1. Open HDDSuperClone.
2. Click 'File' and create a new project. The project file will store your progress and allow a clone to be paused or resumed. (Note: if you save this file to the Linux USB flash drive (e.g. on the Desktop, Documents, etc., it will be lost when the Linux OS is shutdown. Ideally this file should be stored on another external drive so it can be saved permanently.)
3. 'Drive' > 'Choose source drive'.
4. 'Drive' > 'Choose Destination' drive (clone).
5. Double check that the source and destination drives are correct.
6. Click 'Connect', then 'Start'.

### Imaging Hard Drives and SSDs <a href="#imaging-hard-drives-and-ssds" id="imaging-hard-drives-and-ssds"></a>

An **image** refers to a container file where sectors from Disk A are copied into a file stored in Disk B's filesystem. Essentially, the image file acts as a "virtual drive" that mirrors the physical source drive. This process does not overwrite existing data on the destination drive nor modify its partitions, making it safe to use on a drive with existing data. The destination drive must be larger than the source drive and have equal or greater free space than the source drive's total capacity. Since the image file is stored within the destination drive's filesystem, which inherently consumes some space, the destination drive must always have a larger capacity to accommodate the image. Image files can protect data from unintended modifications by the operating system, filesystem checking utilities, or user error, making them generally safer to work with compared to direct cloning.

1. Open HDDSuperClone.
2. Click 'File' and create a new project. The project file will store your progress and allow a clone to be paused or resumed. (Note: if you save this file to the Linux USB flash drive (e.g. on the Desktop, Documents, etc., it will be lost when the Linux OS is shutdown. Ideally this file should be stored on another external drive so it can be saved permanently.)
3. 'Drive' > 'Choose source drive'.
4. 'Drive' > 'Choose Destination' image file (image).
5. Double check that the source and destination drives are correct.
6. Click 'Connect', then 'Start'.

## Manual <a href="#official-manual" id="official-manual"></a>

[/documents/hddsuperclone.pdf](http://192.168.2.9:3000/documents/hddsuperclone.pdf)

## References <a href="#references" id="references"></a>

https://www.hddsuperclone.com/hddlivecd
