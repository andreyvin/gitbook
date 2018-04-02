# Granting EC2 Permissions to an Amazon IAM Role

When adding a new S3 Account, we strongly recommend that you use an [IAM role](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html) with a policy that grants minimum permissions required for proper functioning of CloudBerry Backup.

The IAM role should have the following permissions to be able to successfully use EC2 services via CloudBerry products:

* ImportInstance
* ImportImage
* DescribeInstances
* MonitorInstances
* RequestSpotInstances
* RunInstances
* StartInstances
* TerminateInstances
* ModifyInstanceAttribute
* CreateTags
* CancelImportTask
* StartInstances
* DescribeConversionTasks
* DescribeImportImageTasks
* ImportVolume
* DescribeAvailabilityZones
* DescribeSecurityGroups
* DescribeSubnets
* StopInstances
* DescribeKeyPairs
* ImportSnapshot
* DescribeImportSnapshotTasks
* CreateVolume
* DescribeImages

You can use [CloudBerry Explorer](https://www.cloudberrylab.com/explorer/amazon-s3.aspx) to create an IAM role and grant it the required permissions, or manually create a new user role using [AWS Management Console](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=mbs&templateURL=https://cblmbssystem.s3.amazonaws.com/mbs-iam-role.template). See the following articles for more information:

* [How to Use an External ID When Granting Access to Your AWS Resources to a Third Party](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user_externalid.html)
* [How To Setup a VMimport Role](https://www.cloudberrylab.com/blog/how-to-configure-vmimport-role/)

