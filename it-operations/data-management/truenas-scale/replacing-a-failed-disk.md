# Replacing a failed disk

View the pool status to see which disk is reported as failed.

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

We can see that disk da3 is in faulted status.

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

We need to visually determine which disk da3 corresponds to in our drive bays. By executing the dd command, we simulate drive activity by reading data from da3 and discarding it. This will cause the drive activity LED for da3 to blink rapidly and consistently, allowing us to identify it among the other drives.

```
dd if=/dev/da3 of=/dev/null bs=1048576
```

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Now that we have identified the disk we are going to pull out of the drive bay and replace, we can proceed to offline the disk. Offlining the disk effectively instructs TrueNAS to unmount it, making it safe to remove without causing data loss or corruption. This process ensures that the system recognises the disk as offline, allowing any ongoing operations to complete safely before the physical removal.

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

We can now insert our replacement drive into the drive bay. Once the new drive is securely connected, we will proceed to click the Replace option in TrueNAS. This action will prompt the system to recognize the new drive as a replacement for the offline disk. TrueNAS will then begin the process of resilvering, which involves copying the data from the remaining healthy drives in the pool to the new drive, ensuring that it is fully integrated and mirrors the data correctly.

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>
