# Changing the Backup Prefix

A single [bucket](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingBucket.html) \(or [container](https://cloud.google.com/containers/) in terms of a different cloud provider\) can store backups from different computers and the _backup prefix_ is used to identify different backups within the same bucket.

> The backup prefix is set to the computer name by default.

When a machine on which you are restoring a backup is different from the one that was used to back up these files, CloudBerry Backup might not be able to access the files in the backup, as it searches for files with a wrong backup prefix \(the current computer name does not match the actual backup prefix\).

In this case, you need to change the backup prefix as follows.

1. Open the CloudBerry Backup application menu and select your storage account and in the opened dialog window, click the "**Advanced settings**" link.
2. Specify a new backup prefix either by selecting a required computer in your local network, or by entering a custom prefix text.

> When changing the backup prefix to a corresponding computer name does not help, this may be because these backups use a custom prefix and you need to ask your system administrator which backup prefix to use.

