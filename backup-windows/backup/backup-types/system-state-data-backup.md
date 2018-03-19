# System State Data Backup

System state backup is a native Windows data backup type that only includes crucial OS data. CloudBerry Backup extends this function with the ability to store the data on a cloud storage of your choice.

{% hint style="warning" %}
System State Data Backup is available only on Windows Server 2008 or higher
{% endhint %}

Typical Windows system state backup contains the following data:

* Windows System Registry. 
* Performance Counter Configuration information.
* Component Services Class registration database.
* Boot and system files, including those protected by Windows File Protection \(WFP\).
* Configuration of system-dependent Microsoft applications, such as Certificate Services, Active Directory, IIS, etc.

To create an System State backup plan, launch CloudBerry Backup. On the main toolbar, click **Image Based**.

![](../../../.gitbook/assets/image1.PNG)

The first step is to indicate whether you want to perform backup just to a local or cloud storage or whether you want to use [**Hybrid Backup**](https://www.gitbook.com/book/cloudberry/cloudberry-backup/edit#) to back up data simultaneously to a local and a cloud storage.

![](../../../.gitbook/assets/image2.PNG)

If you selected _Hybrid Backup_, first specify the local storage that will be used to store a local backup. Click **Next **and select the cloud storage that will be used to store a cloud backup. Click **Next**.

![](../../../.gitbook/assets/image3.PNG)

Enter the backup plan name and indicate whether you want to save the plan's configuration in the cloud.

![](../../../.gitbook/assets/image4.PNG)

Select **System State**. Click **Next**.

![](../../../.gitbook/assets/systemstate.png)

If you don't have _Windows Backup_ installed, simply select the checkbox and CloudBerry Backup will install it for you.

![](../../../.gitbook/assets/systemstate2.png)

Now select a temporary intermediate storage that will store the backup data before it will be transferred to the cloud. In this case we'll go with one of our local servers.

![](../../../.gitbook/assets/systemstate4.png)

CloudBerry Backup will next verify that the specified location is accessible. You may need to enter your credentials to do that.

![](../../../.gitbook/assets/systemstate5.png)

The rest of the process is pretty much identical to that of image-based backup. Indicate if you want to use block-level backup. If this checkbox is selected, the initial backup will back up the entire mage and the subsequent backups will only back up modified blocks.

![](../../../.gitbook/assets/systemstate6.png)

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

![](../../../.gitbook/assets/systemstate7.png)

That's it! When the plan completes, you will be notified over email about the status \(if you enabled notifications\). If you've enabled scheduling, the plan will recurrently execute without you having to open the app or click any buttons. Close the app and feel certain that your files are regularly backed up and are invulnerable to any cyber maleficence.

