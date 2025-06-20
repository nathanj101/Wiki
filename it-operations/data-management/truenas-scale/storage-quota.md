# Storage Quota

Filling a ZFS pool beyond 80% capacity is not advisable due to performance degradation, increased risk of data loss, and challenges in managing the system. As the pool nears full capacity, the performance can significantly decline because ZFS uses a copy-on-write mechanism that requires available free space for writing new data, leading to slower read and write operations. Additionally, insufficient space can hinder the ability to create new snapshots or replicate data safely, compromising data protection and recovery options.

For this reason, it’s generally advised to set a usage quota on the appropriate datasets within a ZFS pool to prevent usage from exceeding 80%. I prefer to nest each of my datasets under a main dataset, which allows me to efficiently manage settings for each individual dataset. With this hierarchical setup, I can apply a quota to the parent dataset that automatically cascades to all child datasets. This means that the combined usage of all datasets cannot surpass 80% of the pool's total capacity.

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>
