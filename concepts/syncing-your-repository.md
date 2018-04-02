## Syncing Your Repository

[https://www.cloudberrylab.com/blog/why-you-sometimes-cannot-see-your-files-when-restoring/](https://www.cloudberrylab.com/blog/why-you-sometimes-cannot-see-your-files-when-restoring/)

+

[https://www.cloudberrylab.com/blog/how-to-continue-backup-on-another-computer/](https://www.cloudberrylab.com/blog/how-to-continue-backup-on-another-computer/)

+

[https://www.reddit.com/r/cloudberrylab/comments/7p7q8x/synchronize\_repository/](https://www.reddit.com/r/cloudberrylab/comments/7p7q8x/synchronize_repository/)

Please be informed that you cannot instantly retrieve data from long-term storages used to backup infrequently accessed data, such as_Amazon Glacier_. This is why you may need to sync your repository if**Restore Wizard**does not display some of the files in your backup.

Please be informed that the synchronization process is time-consuming, and it may take up to several hours to obtain a list of your files from such a long-term storage.

Do one of the following to sync a repository depending on the storage provider you use.

### Amazon Glacier

**If you connect Restore Only mode then it syncs instantly. You don't need to wait for all files to download and sync try that.**

**Select the same bucket, vault or container**

**When restoring data from an Amazon Glacier account, you need to run the repository sync process manually. To do this, switch to the by going to Tools \| Options \| Repository: click “Synchronize Repository”. It will take about 4-5 hours.**

### Other Storage Providers

To sync with repositories of cloud storages other than Amazon Glacier, select**Options**in your\_CloudBerry Backup\_application's menu and click**Synchronize Repository**.

{image}

Next, select a storage account that you want to sync and click**Synchronize Now**.

