## 3.4.4 - Select Partitions to Restore

On this wizard page, you can select which partitions to restore.

> The restored partitions must include system volumes as they store information required for loading the operating system.

> Do not exclude recovery partitions unless you are restoring an image to an [Elastic Block Store \(EBS\) Volume](/chapter1/step-3-choose-data-to-restore/34-restore-a-disk-image-or-network-share/342-specify-the-restore-destination/3423-restore-as-an-amazon-ec2-instance-elastic-block-store-volume-or-machine-image/31233-restore-to-elastic-block-store-ebs-volume.md).

![](/assets/image-based-virtual-select-partitions-2.png)

When restoring an NTFS partition, you can customize additional options. See [Resizing NTFS Partitions](/concepts/restoring-ntfs-partitions.md) for more information.

> Please be informed that import of UEFI/EFI BIOS and boot partitions is not supported by most cloud services \(such as AWS, Miscrosoft Azure and Google Cloud\). Please consult the official documentation of a particular cloud service vendor to find out the information about their specific requirements for virtual machine import.

You can also reorganize the restored partitions by selecting the corresponding option. This invokes the **Resize Partitions** dialog window where you can create new virtual disks and map the restored partitions to them using the drag-and-drop operation.

![](/assets/resize-partitions-dialog-2.png)

