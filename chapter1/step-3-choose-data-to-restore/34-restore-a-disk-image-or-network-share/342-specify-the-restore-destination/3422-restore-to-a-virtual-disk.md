## 3.4.2.2 - Restore to a Virtual Disk

Select this option to restore your backup to a virtual disk.

You can mount this disk as a virtual drive or use it in your Virtual Machine environment later on.

The following virtual file formats are supported:

* Hyper-V Virtual Disk \(VHD-format\), dynamic;

* Hyper-V Virtual Disk \(VHD-format\), fixed;

* Hyper-V Virtual Disk \(VHDX-format\), dynamic;

* RAW disk image, raw;

* RAW disk image, rawsparse;

* RAW disk image, tar;

* RAW disk image, tgz;

* VirtualBox Virtual Disk, dynamic;

* VirtualBox Virtual Disk, fixed;

* VMWare Virtual Disk, vmfsdynamic;

* VMWare Virtual Disk, vmfsfixed.

On the next wizard page, you need to select which partitions to restore.

![](/assets/image-based-virtual-select-partitions.png)

> When restoring an NTFS partition, you can customize additional options. See [Restoring NTFS Partitions](/concepts/restoring-ntfs-partitions.md) for more information.

You can also reorganize the restored partitions by selecting the corresponding option. This invokes the **Resize Partitions** dialog window where you can create new virtual disks and map the restored partitions to them using the drag-and-drop operation.

![](/assets/resize-partitions-dialog.png)

After switching to the next wizard page, you can specify the destination folder for your virtual machine file.

![](/assets/image-based-virtual-select-destination.png)





