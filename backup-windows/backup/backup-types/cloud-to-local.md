# Cloud to Local

Cloud to Local backup is a backup type that enables you to back up individual files or folders from one cloud account to a local storage. For instance, you can create a backup plan that will weekly back up your Amazon S3 documents bucket to your local NAS-based storage. It's similar to the regular file-level backup, except that data flows in the opposite direction — from the cloud to your computer.

To create a cloud to cloud backup plan, launch CloudBerry Backup. On the main toolbar, click **Cloud to Local**.

![](../../../.gitbook/assets/ctl1.PNG)

The Backup Wizard will appear, prompting you to configure the backup plan. The first step is to specify the source cloud storage.

![](../../../.gitbook/assets/ctl2.PNG)

Specify the files, folders, and buckets you'd like to back up and click **Next**.

![](../../../.gitbook/assets/ctl3.PNG)

Now select a local backup destination that will store the data.

![](../../../.gitbook/assets/ctl4.PNG)

Enter the backup plan name and indicate whether you want to save the plan's configuration in the cloud.

![](../../../.gitbook/assets/ctl5.PNG)

Select the desired backup mode, depending on how thoroughly you'd like to configure the backup plan.

![](../../../.gitbook/assets/ctl6.PNG)

In the next step you can specify which files should be skipped / included and a number of other options.

![](../../../.gitbook/assets/ctl7.PNG)

Now you can enable compression and encryption. CloudBerry Backup supports up to 256-bit military grade encryption by default. Note that we don't store the key anywhere for security purposes. If you forget it, the data is permanently gone.

![](../../../.gitbook/assets/ctl8.PNG)

The next step is retention policy configuration. You can indicate if you want to delete versions older than a pre-defined number of days from the modification or backup date. Similarly, you can explicitly determine the number of versions of each file to be retained on the storage.

![](../../../.gitbook/assets/ctl9.PNG)

Next up is scheduling. Here you can set the required schedule with various parameters like frequency, recurrence, immediate resumption of the plan following the computer restart, and the like.

![](../../../.gitbook/assets/ctl10.PNG)

Next, specify the optional pre- and post-actions. These are essentially scripts that can be executed prior to and immediately following backup. For instance, you can run a script that turns off the computer when the backup plan completes executing. Alternatively, you can run a script that, say, disables all incoming connections during the plan execution. Backup chain allows you to automatically trigger another backup plan when the current one completes.

![](../../../.gitbook/assets/ctl11.PNG)

Finally, you can configure email notifications to be notified of backup plan executions and failures. We even support custom SMTP servers if you use one of those. Also available is optional detailed reporting.

![](../../../.gitbook/assets/ctl12.png)

Conclude configuring the plan and, once finished, execute it. The Backup Wizard will be closed, and the backup plan will start executing. In the meantime, you can observe the backup process in the green progress bar in the dedicated dashboard section.

![](../../../.gitbook/assets/ctl13.PNG)

