# Scrub Tasks

Scrub tasks in TrueNAS help prevent signs of corruption or inconsistencies such as bit rot, which refers to the gradual decay of data integrity over time, typically caused by factors such as hardware degradation, environmental conditions, or cosmic rays affecting the physical storage medium. During a scrub, the system reads the data and its associated checksums, which are calculated when the data is written. By verifying these checksums against the stored data, the scrub can identify any discrepancies or corruption.

## Recommended Configuration

To minimise the impact on system performance, it’s best to schedule scrub tasks during periods of low disk activity, such as overnight when user access and data operations are minimal. This ensures that the scrub can complete efficiently without disrupting normal system usage, allowing for thorough verification of data integrity while maintaining optimal performance for users and applications during peak usage hours.

{% hint style="info" %}
Running a scrub task simultaneously with a SMART test is not advisable because both operations are resource-intensive and can significantly impact disk performance.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>
