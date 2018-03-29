# Microsoft Hyper-V Virtual Machine Backup

CloudBerry Backup \([VM edition](https://www.cloudberrylab.com/backup/vmware-hyperv.aspx)\) supports backup and restore of virtual machines created and controlled by a Microsoft Hyper-V server.

Here are the requirements for vSphere ESXi backup:

* Hyper-V-enabled Windows Server 2008 or higher;
* [CloudBerry Backup VM Edition](https://www.cloudberrylab.com/backup/vmware-hyperv.aspx).

## Backing up Hyper-V virtual machines {#backing-up-vsphere-esxi-virtual-machines}

To create a Hyper-V backup plan, launch CloudBerry Backup. On the main toolbar, click **Hyper-V**.

![](../../../../.gitbook/assets/image-1.png)

The first step is to indicate whether you want to perform backup just to a local or cloud storage or whether you want to use [**Hybrid Backup**](https://www.cloudberry.help/overview/data-backup/backup-types/hybrid-backup.html) to back up data simultaneously to a local and a cloud storage.

![](../../../../.gitbook/assets/image-2%20%281%29.png)

Select a local or cloud backup destination and click **Next**. If you selected Hybrid Backup, first specify the local backup destination and then the cloud one.

![](../../../../.gitbook/assets/image-3%20%281%29.png)

Enter the backup plan name and indicate whether you want to save the plan's configuration in the cloud.

![](../../../../.gitbook/assets/image-4%20%281%29.png)

Now it's time to connect to the Hyper-V server and select the required virtual machines.

You can select one of the following options:

* Back up all Virtual Machines on the ESXi server;
* Backup only running VMs;
* Backup selected VMs from the list.

Select the required VMs and click **Next**.

![](../../../../.gitbook/assets/image-5.png)

Enable compression and encryption if necessary. CloudBerry Backup supports up to 256-bit military grade encryption out of the box. If you're backing up data to Amazon S3, you can also use server side encryption. Note that we don't store the key anywhere for security purposes. If you forget it, the data is permanently gone.

![](../../../../.gitbook/assets/image-6%20%281%29.png)

The next step is retention policy configuration. You can indicate if you want to delete versions older than a pre-defined number of days from the modification or backup date. Similarly, you can explicitly determine the number of versions of each file that must be retained on the storage.

![](../../../../.gitbook/assets/image-7.png)

Next up is scheduling. Here you can set the required schedule with various parameters like frequency, recurrence, immediate resumption of the plan following the computer restart, and so forth.

![](../../../../.gitbook/assets/image-8.png)

To ensure that you can at any point revert to the older versions, it is recommended to perform full backup every now and then. You can schedule full backup with the required frequency and even enforce it when the size of block-level backup exceeds the specified threshold.

![](../../../../.gitbook/assets/image-9%20%281%29.png)

Next, specify the optional pre- and post-actions. These are essentially scripts that can be executed prior to and immediately following backup. For instance, you can run a script that turns off the computer when the backup plan completes executing. Alternatively, you can run a script that, say, disables all incoming connections during the plan execution. Backup chain allows you to automatically trigger another backup plan when the current one completes.

![](../../../../.gitbook/assets/image-10.png)

Finally, you can configure email notifications to be notified of backup plan executions and failures. We even support custom SMTP servers if you use one of those. Also available is optional detailed reporting.

![](../../../../.gitbook/assets/image-11.png)

Conclude configuring the plan and, once finished, execute it. The Backup Wizard will be closed, and the backup plan will start executing. In the meantime, you can observe the backup process in the green progress bar in the dedicated dashboard section.

![](../../../../.gitbook/assets/image-12.png)

