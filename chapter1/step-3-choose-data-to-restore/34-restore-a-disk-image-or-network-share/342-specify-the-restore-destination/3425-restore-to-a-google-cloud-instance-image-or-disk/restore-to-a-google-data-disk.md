## 3.4.2.5.3 - Restore to a Google Data Disk

This wizard page enables you to restore a disk image to a [Google disk](https://cloud.google.com/compute/docs/disks/).

> The disk size \(the total of all [partitions](/chapter1/step-3-choose-data-to-restore/34-restore-a-disk-image-or-network-share/344-select-partitions.md)\) cannot exceed **2** TB.

![](/assets/restore-image-google-data-disk.png)

First, you need to select an existing, or specify a new Google Cloud account. See the following article to learn how to add a new Google Cloud account to CloudBerry Backup: [Signing up for Google](https://help.cloudberrylab.com/cloudberry-backup/signing-up-for-the-cloud/google-cloud/signing-up-for-google).

After selecting an account, specify the main settings of a target instance:

* **Name**  
  Specifies the disk name.

  > The specified name should comply with the [RFC 1035](https://www.ietf.org/rfc/rfc1035.txt) naming convention.

* **Zone**  
  Specifies the zone in which the target disk is located.

  > You can find out the information about quotas defined for the selected zone by clicking the "**View quotas**" link.  
  > ![](/assets/google-zone-quotas-popup.png)  
  > See the following document to learn about zones and their quotas: [Regions and Zones](https://cloud.google.com/compute/docs/regions-zones/).

* **Disk type**  
  Enables you to choose among the following persistent disk types:

  * **pd-ssd SSD Persistent Disk**  
  * **pd-standard Standard Persistent Disk**

  > See the following document to learn about the difference between these disk types: [Storage Options](https://cloud.google.com/compute/docs/disks/).



