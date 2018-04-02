## 3.1.2.3.2 - Restore to Amazon Machine Image \(AMI\)

This option enables you to restore your disk image to an [Amazon Machine Image \(AMI\)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html) of your choice.

> This feature is supported for the following operation systems:
>
> * Windows 7
> * Windows 8
> * Windows 10
> * Windows Server 2008
> * Windows Server 2012
> * Windows Server 2016

After switching to the next wizard page, you need to specify the instance details.

![](/assets/image-based-restore-to-ami-instance-details.png)

First, you need to select an existing, or specify a new _"S3"_ or _"S3 China"_ instance account. See the following article to learn how to add a new S3 account to CloudBerry Backup: [Signing up for Amazon S3](https://help.cloudberrylab.com/cloudberry-backup/signing-up-for-the-cloud/amazon-aws/signing-up-for-amazon-s3).

> Please make sure that the specified account has all required [EC2](/concepts/permissions.md) and [S3](https://docs.aws.amazon.com/AmazonS3/latest/dev/s3-access-control.html) permissions.

After selecting an account, specify the main settings of a target machine image:

* **Region**  
  Amazon EC2 is hosted in multiple locations world-wide that are composed of separate geographic areas _\(regions\)_. Amazon EC2 provides you with the ability to place resources, such as instances, and data in multiple locations. Resources are not replicated across regions unless you do so specifically.

  > Please be informed that transferring data between different regions takes more time than performing data transfer within a single region.
  >
  > When restoring a disk for an existing virtual machine, the disk must belong to the same Availability Zone as the machine to which you are going to attach the disk.
  >
  > See [Regions and Availability Zones](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html) for more information.

  The wizard indicates whether your [VM import](https://docs.aws.amazon.com/vm-import/latest/userguide/what-is-vmimport.html) role is configured property for the selected account, because AWS will not perform input operations without appropriate permissions. You can create a VM import role in one of the following ways:

  * You can [manually configure a VM import role](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#);

  * You can grant the required IAM permissions to an [IAM user](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) whose account is used for restoring backups.

    The wizard will automatically create a VM import role when it detects that none of the above configurations are available.

* **EBS Volume Type**

  Amazon EBS \(Elastic Block Store\) provides the following volume types, which differ in their performance characteristics and price, so that you can tailor your storage performance and costs to the requirements of your applications. CloudBerry Backup supports the following volume types:

  * **General Purpose SSD \(gp2\)        
    **A general purpose SSD volume that balances price and performance for a wide variety of workloads.

  * **Provisioned IOPS SSD \(io1\)        
    **The highest-performance SSD volume for mission-critical low-latency or high-throughput workloads.

  * **Magnetic \(standard, a previous-generation type\)        
    **A previous generation HDD. If you need higher performance or performance consistency than previous-generation volumes can provide, we recommend that you consider using _General Purpose SSD \(gp2\)_ or other current volume types.

> See [Amazon EBS Volume Types](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#) to learn more.



