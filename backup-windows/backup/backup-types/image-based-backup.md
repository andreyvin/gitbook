# Image Based Backup

Image-based backup is a very powerful type of backup that allows you to back up the entire disk image. Unlike file-level backup where you select singular files, image-based backup allows you to either back up the entire disk or only certain volumes. The are two main use-cases for image-based backup:

* All-inclusive backup of the entire disk as an insurance policy against hardware failure and other emergencies;
* Replacement of physical servers by the cloud; namely, image-based backups can later be used as a base for Amazon EC2, Google Cloud, and Microsoft Azure virtual machines.

To create an image-based backup plan, launch CloudBerry Backup. On the main toolbar, click **Image Based**.

![](../../../.gitbook/assets/image1.PNG)

The first step is to indicate whether you want to perform backup just to a local or cloud storage or whether you want to use [**Hybrid Backup**](hybrid-backup.md)** **to back up data simultaneously to a local and a cloud storage.

![](../../../.gitbook/assets/image2.PNG)

If you selected _Hybrid Backup_, first specify the local storage that will be used to store a local backup. Click **Next** and select the cloud storage that will be used to store a cloud backup. Click Next.

**NB**: Please note that Amazon Glacier cannot be used as a backup destination  for image-based backup destinations. Use another cloud storage instead or configure an S3-to-Glacier lifecycle policy that will automatically transfer the backup to Glacier.

![](../../../.gitbook/assets/image3.PNG)

Enter the backup plan name and indicate whether you want to save the plan's configuration in the cloud.

![](../../../.gitbook/assets/image4.PNG)

Now select the required partitions. Here you can back up:

* Only system required partitions \(automatic selection\);
* All drives;
* Selected partitions only. 

![](../../../.gitbook/assets/image5.PNG)

Indicate if you want to use block-level backup. If this checkbox is selected, the initial backup will back up the entire mage and the subsequent backups will only back up modified blocks.

![](../../../.gitbook/assets/image6.PNG)

Enable compression and encryption if necessary. CloudBerry Backup supports up to 256-bit military grade encryption out of the box. If you're backing up data to Amazon S3, you can also use server side encryption. Note that we don't store the key anywhere for security purposes. If you forget it, the data is permanently gone.

![](../../../.gitbook/assets/image7.PNG)

The next step is retention policy configuration. You can indicate if you want to delete versions older than a pre-defined number of days from the modification or backup date. Similarly, you can explicitly determine the number of versions of each file that must be retained on the storage.

![](../../../.gitbook/assets/image8.PNG)

Next up is scheduling. Here you can set the required schedule with various parameters like frequency, recurrence, immediate resumption of the plan following the computer restart, and so forth.

![](../../../.gitbook/assets/image9.PNG)

To ensure that you can at any point revert to the older versions, it is recommended to perform full backup every now and then. You can schedule full backup with the required frequency and even enforce it when the size of block-level backup exceeds the specified threshold.

![](../../../.gitbook/assets/image10.PNG)

Next, specify the optional pre- and post-actions. These are essentially scripts that can be executed prior to and immediately following backup. For instance, you can run a script that turns off the computer when the backup plan completes executing. Alternatively, you can run a script that, say, disables all incoming connections during the plan execution. Backup chain allows you to automatically trigger another backup plan when the current one completes.

![](../../../.gitbook/assets/image11.PNG)

Finally, you can configure email notifications to be notified of backup plan executions and failures. We even support custom SMTP servers if you use one of those. Also available is optional detailed reporting.

![](../../../.gitbook/assets/image12.png)

Conclude configuring the plan and, once finished, execute it. The Backup Wizard will be closed, and the backup plan will start executing. In the meantime, you can observe the backup process in the green progress bar in the dedicated dashboard section.    

![](../../../.gitbook/assets/image13.PNG)

That's it! When the plan completes, you will be notified over email about the status \(if you enabled notifications\). If you've enabled scheduling, the plan will recurrently execute without you having to open the app or click any buttons. Close the app and feel certain that your files are regularly backed up and are invulnerable to any cyber maleficence.

