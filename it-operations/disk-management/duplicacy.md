# Duplicacy

## Introduction <a href="#introduction" id="introduction"></a>

Duplicacy is a backup tool designed for efficient, cross-platform data backup with advanced features for data deduplication and versioning

Key features of Duplicacy include:

* **Web-Based Management**: Duplicacy offers a web-based user interface for managing backups, making it easy to configure and monitor backup jobs remotely.
* **Lock-Free Deduplication:** Works by relying on the basic file system API to manage deduplicated chunks without using any locks. This feature significantly reduces storage requirements and improves backup speed by eliminating redundant chunks of data.
* **Incremental Backups**: The tool supports incremental backups, meaning that only changes made since the last backup are stored. This approach reduces the amount of data transferred and stored, making the process faster and more efficient.
* **Cloud Storage Support**: Duplicacy supports various cloud storage providers, including Amazon S3, Google Cloud Storage, Microsoft Azure, Backblaze B2, Wasabi, and others
* **Versioning**: Duplicacy maintains multiple versions of backups, allowing users to restore their data to any point in time. This feature is useful for recovering from accidental deletions, data corruption, or ransomware attacks.
* **Open-Source Option**: There is an open-source version of Duplicacy available, providing transparency and allowing users to review the code and even contribute to its development.
* **Encryption**: Duplicacy offers strong encryption to secure backup data. It uses a combination of RSA and AES encryption algorithms to protect data both in transit and at rest.
* **Scheduler**: The tool includes a built-in scheduler for automating backup jobs, ensuring regular and timely backups without manual intervention.

## Installation <a href="#installation" id="installation"></a>

**Requirements:**

* Windows (x64, i386)
* macOS (x64, arm64)
* Linux (x64, arm64, armv5)
* FreeBSD (x64)

**Installation:**

1. Download duplicacy from the [official website](https://duplicacy.com/download.html).
2. Run the setup executable.

## Manual <a href="#official-manual" id="official-manual"></a>

https://duplicacy.com/guide.html

## References <a href="#references" id="references"></a>

https://duplicacy.com/
