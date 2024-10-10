# Periodic Snapshot Tasks

Periodic Snapshot Tasks in TrueNAS create point-in-time snapshots of datasets or volumes at regular intervals. These snapshots capture the state of the data at the time they are taken, allowing you to revert to a previous version if needed. Snapshots are efficient since they only record changes made after the last snapshot, not duplicating the entire dataset. Periodic Snapshot Tasks are essential for data protection and recovery, providing a way to roll back to earlier versions in case of accidental deletion, corruption, or ransomware attacks, while using minimal additional storage.

{% hint style="warning" %}
While periodic snapshots are an excellent tool for protecting against **logical incidents**—such as accidental file deletion, corruption, or ransomware attacks—it's important to note that they do **not** protect against **physical incidents**, like drive failures or hardware damage.
{% endhint %}

## Recommended Configuration

For my main dataset, which contains all my important photos, documents, and work-related files, I’ve set snapshots to be captured every 15 minutes. This frequent interval is crucial because the data in this dataset changes often, and taking snapshots every 15 minutes ensures I minimise potential data loss in case of a logical incident, like accidental deletion or ransomware. However, for something like a data share that stores static media, such as movies, there’s no need to capture snapshots so frequently. For those, I can safely extend the interval to weekly snapshots since the data is rarely modified. Regardless of the dataset, I always retain snapshots for 2 weeks. This gives me a buffer of time to handle any issues, such as a family member accidentally deleting important files—like family photos—while I'm away on holiday. With 2 weeks of snapshots, I have enough time to restore the dataset to just before the deletion occurred, ensuring no permanent data loss.

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>
