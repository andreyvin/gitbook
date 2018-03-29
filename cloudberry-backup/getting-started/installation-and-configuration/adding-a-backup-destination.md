# Adding a Backup Destination

Having installed and activated CloudBerry Backup, the next step is adding a backup destination \(a.k.a. backup storage\). Backup destination is a cloud or local storage that will be used to store your backups. We support pretty much all of the most popular cloud storage services, including Amazon S3, Google Cloud Platform, and Microsoft Azure, among others.

## Adding a Cloud Storage

To add a cloud storage, launch CloudBerry Backup and click on the _CloudBerry_ button. Click **Add New Account**.

![](../../../.gitbook/assets/addaccount1.png)

Select the cloud storage you'd like to add and double-click on it.

![](../../../.gitbook/assets/addaccount2.png)

In this example we'll go with Amazon S3. Specify the display name that will appear throughout the programm. Enter the S3 credentials — **Access and Secret keys**. Finally, select or create a bucket on the cloud storage and click **OK**.

![](../../../.gitbook/assets/addaccount.png)

{% hint style="success" %}
Your storage has been added!
{% endhint %}

## Adding a Local Storage

The process of adding a local storage does not differ much from adding a local storage. Simply click **File System** when adding a backup destination.

![](../../../.gitbook/assets/storage1.PNG)

Next, enter the display name and specify the path. In this case we're going to use our local shared storage. Click **OK**.

![](../../../.gitbook/assets/addaccount3.png)

That's it. Now that you've added a backup destination, you may proceed to create backup plans and start backing up your data to a local storage or to the cloud!

