# VMware Virtual Machine Backup

CloudBerry Backup \([VM edition](https://www.cloudberrylab.com/backup/vmware-hyperv.aspx)\) supports backup and restore of virtual machines created and controlled by a vSphere ESXi server.

Here are the requirements for vSphere ESXi backup:

* Windows OS 64-bit;
* vSphere version 5.1 or higher;
* [CloudBerry Backup VM Edition](https://www.cloudberrylab.com/backup/vmware-hyperv.aspx).

## Backing up vSphere ESXi virtual machines

To create a VMware backup plan, launch CloudBerry Backup. On the main toolbar, click **VMware**.

![](../../../../.gitbook/assets/capture1vm.PNG)

The first step is to indicate whether you want to perform backup just to a local or cloud storage or whether you want to use [**Hybrid Backup**](https://www.cloudberry.help/overview/data-backup/backup-types/hybrid-backup.html) to back up data simultaneously to a local and a cloud storage.

![](../../../../.gitbook/assets/capture2vm.PNG)

Select a local or cloud backup destination and click **Next**. If you selected Hybrid Backup, first specify the local backup destination and then the cloud one.

![](../../../../.gitbook/assets/capture3vm.PNG)

Enter the backup plan name and indicate whether you want to save the plan's configuration in the cloud.

![](../../../../.gitbook/assets/capture4vm.PNG)

Now it's time to connect to the VMware Host Server. Enter the server address and credentials. Click **Next **and CloudBerry Backup will shortly connect to the server

![](../../../../.gitbook/assets/capture5pvm.PNG)

Now you can select one of the following options:

* Back up all Virtual Machines on the ESXi server;
* Backup only running VMs;
* Backup selected VMs from the list.

Optionally, you can enable the so-called [_Changed Block Tracking_](https://kb.vmware.com/s/article/1020128) that automatically tracks virtual disk modifications of a given VM and backups only modified blocks as opposed to complete re-upload of a VM.

Select the required VMs and click **Next**.

![](../../../../.gitbook/assets/vmwarediskselection5.PNG)

Next, specify which disks you'd like to back up. 

![](../../../../.gitbook/assets/vmwarediskselection4.PNG)

Optionally, you can click on the disk's size and specify which folders or files should be skipped during backup.

![](../../../../.gitbook/assets/vmwarediskselection3.PNG)

Next, enable compression and encryption if necessary. CloudBerry Backup supports up to 256-bit military grade encryption out of the box. If you're backing up data to Amazon S3, you can also use server side encryption. Note that we don't store the key anywhere for security purposes. If you forget it, the data is permanently gone.

![](../../../../.gitbook/assets/capture7vm.PNG)

The next step is retention policy configuration. You can indicate if you want to delete versions older than a pre-defined number of days from the modification or backup date. Similarly, you can explicitly determine the number of versions of each file that must be retained on the storage.

![](../../../../.gitbook/assets/capture8vm.PNG)

Next up is scheduling. Here you can set the required schedule with various parameters like frequency, recurrence, immediate resumption of the plan following the computer restart, and so forth.

![](../../../../.gitbook/assets/capture9vm.PNG)

To ensure that you can at any point revert to the older versions, it is recommended to perform full backup every now and then. You can schedule full backup with the required frequency and even enforce it when the size of block-level backup exceeds the specified threshold.

![](../../../../.gitbook/assets/capture10vm.PNG)

Next, specify the optional pre- and post-actions. These are essentially scripts that can be executed prior to and immediately following backup. For instance, you can run a script that turns off the computer when the backup plan completes executing. Alternatively, you can run a script that, say, disables all incoming connections during the plan execution. Backup chain allows you to automatically trigger another backup plan when the current one completes.

![](../../../../.gitbook/assets/capture11vm.PNG)

Finally, you can configure email notifications to be notified of backup plan executions and failures. We even support custom SMTP servers if you use one of those. Also available is optional detailed reporting.

![](../../../../.gitbook/assets/capture12vm.png)

Conclude configuring the plan and, once finished, execute it. The Backup Wizard will be closed, and the backup plan will start executing. In the meantime, you can observe the backup process in the green progress bar in the dedicated dashboard section.

![](../../../../.gitbook/assets/capture13vm.PNG)

