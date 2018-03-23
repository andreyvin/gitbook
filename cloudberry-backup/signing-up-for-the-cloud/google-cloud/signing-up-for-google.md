# Signing up for Google

In this tutorial we will explain how to sign up for Google Cloud in just a few steps.

## Signing up for Google Cloud

Go to [https://cloud.google.com/storage/](https://cloud.google.com/storage/) and click **TRY IT FREE**.

![](../../../.gitbook/assets/capture1.png)

Agree with their terms of service and fill in the registration form.

![](../../../.gitbook/assets/capture2.png)

![](../../../.gitbook/assets/capture3.png)

Once the registration form is complete, click **Start my free trial**.** **

![](../../../.gitbook/assets/capture4.png)

Next up you'll see the main dashboard. Proceed to the navigation drawer to create a so-called project.

![](../../../.gitbook/assets/capture5.png)

Select **IAM & Admin**.

![](../../../.gitbook/assets/capture6.png)

In **Projects**, click **Create Project**.

![](../../../.gitbook/assets/capture7.png)

All data in Google Cloud Storage belongs inside a project. A project consists of a set of users, a set of APIs, billing, authentication, and monitoring settings for those APIs. You can have one or multiple projects.

Give your project a name and click **Create**.

![](../../../.gitbook/assets/capture8.png)

Once the new project is created you will be able to create your first storage bucket inside this project. In the navigation drawer, click **Storage**.

![](../../../.gitbook/assets/capture10.png)

Click **Create bucket**.

![](../../../.gitbook/assets/capture11.png)

Specify the bucket name, default storage class, and location. Click **Create**.

![](../../../.gitbook/assets/capture12.png)

**Note**: Buckets belong to a particular project and cannot be shared among projects. There is no limit however on the number of buckets that you can create within a project.

## Preparing Service Account

Google Cloud Storage lets you use service accounts to authenticate your application. A service account's credentials include a generated email address that is unique, a client ID, and at least one public/private key pair.

In the navigation drawer, select **API Manager**.

![](../../../.gitbook/assets/screen-shot-2017-03-22-at-19.49.42-624x757.png)

Under **Credentials**, expand **Create credentials **and click **Service account key**.

![](../../../.gitbook/assets/screen-shot-2017-03-22-at-19.54.53-1024x616.png)

Specify the service account and the key type \(P12\). Click **Create**.

![](../../../.gitbook/assets/screen-shot-2017-03-22-at-20.14.08-1024x459.png)

The key will shortly start downloading. The private key's password will be shown on a pop-up window. Write it down somewhere so as to not lose it in the future.

![](../../../.gitbook/assets/screen-shot-2017-03-22-at-20.18.21-1024x434.png)

In addition to the mentioned file, the service account information will also be displayed in the Credentials Dashboard.

![](../../../.gitbook/assets/screen-shot-2017-03-22-at-20.20.03-1024x312.png)

You're finished. Now that you've signed up for Google Cloud, it's time to use the newly created credentials when [adding a backup destination](../../getting-started/installation-and-configuration/adding-a-backup-destination.md) in CloudBerry Backup.

