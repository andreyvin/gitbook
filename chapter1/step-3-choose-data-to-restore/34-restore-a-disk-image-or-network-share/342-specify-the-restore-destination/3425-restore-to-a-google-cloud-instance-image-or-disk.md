## 3.4.2.5 - Restore to Google Cloud Instance, Image, or Disk

Please be informed that [Google Compute Engine](https://cloud.google.com/compute/docs/instances/windows/) currently supports only the following Windows Server versions:

> * Windows Server 2008R2 x64 Service Pack 1, with the [KB2921916 hot fix](https://support.microsoft.com/en-us/help/2921916/the-untrusted-publisher-dialog-box-appears-when-you-install-a-driver-i) installed. Without this hot fix, the network driver will not be properly installed and you will not be able to connect to the virtual machine even after it has been restored.
> * Windows Server 2012R2 x64
> * Windows Server 2016 x64
>
> Disk images that have Windows 7, 8 or 10 installed on them will not be restored.

On this wizard page, you can select whether you need to restore an image to a Google Cloud instance, image or disk.

![](/assets/restore-google-select.png)

The following tutorials provide step-by-step instructions on how to set up you Google Cloud account for restoring an image disk:

* [Restore to a Google Cloud instance](/chapter1/step-3-choose-data-to-restore/34-restore-a-disk-image-or-network-share/342-specify-the-restore-destination/3425-restore-to-a-google-cloud-instance-image-or-disk/34251-restore-to-a-google-cloud-instance.md)
* [Restore to a Google machine image](/chapter1/step-3-choose-data-to-restore/34-restore-a-disk-image-or-network-share/342-specify-the-restore-destination/3425-restore-to-a-google-cloud-instance-image-or-disk/34252-restore-to-a-google-machine-image.md)
* [Restore to a Google data disk](/chapter1/step-3-choose-data-to-restore/34-restore-a-disk-image-or-network-share/342-specify-the-restore-destination/3425-restore-to-a-google-cloud-instance-image-or-disk/restore-to-a-google-data-disk.md)

> Before restoring your backups to Google Cloud, please take time to learn about the relevant [resource quotas](https://cloud.google.com/compute/quotas). Among these limitations, please pay special attention to the quotas imposed on the maximum number of CPUs allowed per project, because you will only be able to find out whether you are about to exceed these quotas via the Google console.



