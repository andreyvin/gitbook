## **3.4.5 - Specify the Destination Disk Capacity**

On this wizard page, you can specify the capacity of the destination disk.

![](/assets/ami-destination-capacity.png)

The wizard indicates the minimum and maximum allowed capacity.

The minimum size is the total of the **Target Size** values specified on the [previous wizard page](/chapter1/step-3-choose-data-to-restore/34-restore-a-disk-image-or-network-share/344-select-partitions.md) for all selected partitions, plus approximately **1** GB reserved by CloudBerry Backup for storing temporary information.

> CloudBerry Backup reserves **1** GB to allocate the GUID Partition Table \(GPT\) / Master Boot Record \(MBR\) partition tables and align the partitions' and disk's boundaries in multiplies of the sector size.

For example, the following image illustrates a volume with two selected partitions having the target size set to **1** GB and **148** GB.

![](/assets/restore-image-select-partitions-target-size.png)

As a result, the minimum allowed capacity equals **150** GB \(**1** + **148** + **1**\).

![](/assets/restore-image-disk-capacity-example.png)

When specifying the maximum capacity, please consider the following limitations:

* A Master Boot Record \(MBR\) disk size cannot exceed **2** TB.
* A Windows MBR partition cannot exceed **2** TB.
* With most cloud services, the maximum disk size is limited by **2 **TB for virtual machine instances and by **4 **TB for data disks.



