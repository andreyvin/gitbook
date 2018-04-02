## 3.4.2.5.1 - Restore to a Google Cloud Instance

This wizard page enables you to restore a disk image to a [Google Cloud instance](https://cloud.google.com/compute/docs/instances/).

![](/assets/restore-google-vm-instance-2.png)

First, you need to select an existing, or specify a new Google Cloud account. See the following article to learn how to add a new Google Cloud account to CloudBerry Backup: [Signing up for Google](https://help.cloudberrylab.com/cloudberry-backup/signing-up-for-the-cloud/google-cloud/signing-up-for-google).

> Please make sure that the "Request Google Cloud Platform scopes" option is enabled for the specified account. This option is required to be able restore to Google Compute Engine instances. Unless this option is enabled, you will not be able to configure the target machine settings.
>
> You can find this setting in the **Google Cloud Account** dialog window that is invoked by clicking the **Edit Google VM Account** button on this wizard page. To enable this option, you first need to sign out from the current account and then sign in once this setting is turned on.  
> ![](/assets/google-cloud-account-dialog-window.png)

After selecting an account, specify the main settings of a target instance:

* **Name**  
  Specifies the name of a [Google Compute Engine instance](https://cloud.google.com/compute/docs/instances/) to which to restore your disk image.

  > The specified name should comply with the [RFC 1035](https://www.ietf.org/rfc/rfc1035.txt) naming convention.

* **Zone**  
  Specifies the zone in which the target instance is located.

  > You can find out the information about quotas defined for the selected zone by clicking the "**View quotas**" link.  
  > ![](/assets/google-zone-quotas-popup.png)  
  > See the following document to learn about zones and their quotas: [Regions and Zones](https://cloud.google.com/compute/docs/regions-zones/).

* **Machine type**  
  Specifies the hardware configuration of a virtual machine machine instance to which your disk image will be restored.

  > See the following document to learn about the available configurations: [Machine Types](https://cloud.google.com/compute/docs/machine-types).

* **Disk type**  
  Enables you to choose among the following persistent disk types to use on the selected instance:

  * **pd-ssd SSD Persistent Disk**  
  * **pd-standard Standard Persistent Disk**

  > See the following document to learn about the difference between these disk types: [Storage Options](https://cloud.google.com/compute/docs/disks/).

* **Subnet**  
  Enables you to select a range of default IP addresses that can be assigned to the virtual machine within a specific subnet.

  > Please ensure that the assigned IP range is available in your virtual private cloud network. You can enter a custom IP manually to the "**IP address**" field \(see below\).

  See the following document for more information: [Virtual Private Cloud \(VPC\) Network Overview](https://cloud.google.com/vpc/docs/vpc).

* **IP address** \(optional\)  
  Enables you to assign a custom IP address to the virtual machine within a specific subnet.

  > Please ensure that the assigned IP is available in your virtual private cloud network.

  See the following document for more information: [Virtual Private Cloud \(VPC\) Network Overview](https://cloud.google.com/vpc/docs/vpc).



