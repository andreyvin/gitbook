## 3.4.2.4.1 - Restore to an Azure Virtual Machine

This wizard page enables you to restore a disk image to a [Microsoft Azure virtual machine](https://docs.microsoft.com/en-us/azure/virtual-machines/).

![](/assets/restore-azure-vm.png)

Before running this wizard, you need to create a new user and select a subscription, region, resource groups, as well as create a storage account and virtual network via the [Microsoft Azure Portal](https://portal.azure.com/).

> To be able to restore a disk image, you should use a [general-purpose storage account](https://docs.microsoft.com/en-us/azure/storage/common/storage-account-options) and not a blob storage, because blob storage accounts support only _block_ and _append blobs_, and not _page blobs_ on on which virtual machines are stored. Page blobs are only available in general-purpose accounts and they do not provide [zone-redundant storage \(ZRS\)](https://docs.microsoft.com/en-us/azure/storage/common/storage-redundancy#zone-redundant-storage).
>
> See the following article to learn about managing Azure Active Directory accounts when using CloudBerry Lab products: [Managing Azure Active Directory Accounts](/concepts/managing-azure-active-directory-accounts.md).

Next, you need to select an existing Azure account or create and configure a new one on this wizard page.

After you selected an account, specify the following options:

* **Computer name**  
  Specifies the name of the created virtual machine.

* **Location**  
  Specifies the virtual machine's [location](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/regions-and-availability).

  > Please be informed that transferring data between different locations takes more time than performing data transfer within a single location.

* **Resource group**  
  Specifies the container that holds related _resources_ \(such as virtual machines, storage accounts, web apps, databases, and virtual networks\) for an Azure solution. See [Resource groups](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-overview#resource-groups) for more information.

* **VM size**  
  Specifies the size of the target virtual machine.

  > The **"Disk size"** value displayed for a virtual machine selected on this wizard page indicates a space allocated by Microsoft Azure for storing various temporary information \(such as swap files and memory page data\). This value is not related to the [total size that a restored disk can have](/chapter1/step-3-choose-data-to-restore/34-restore-a-disk-image-or-network-share/344-select-partitions.md) \(which is limited to **2** TB for Azure virtual machines\). See the following documents for more information:

  * [Sizes for Windows virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes)

  * [Sizes for Linux virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/sizes)

* **Network**  
  When you create an Azure virtual machine, you must create a new [_virtual network \(VNet\)_](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/network-overview) or use an existing one.

  > The specifies network must belong to the same location and resource group as the specified _storage _\(see below\). Otherwise, you will not be able to set up a virtual machine. See the following Knowledge Base article for more information: [Cannot specify all Azure Virtual Machine instance details in the restore wizard](https://kb.cloudberrylab.com/kb1063/).

* **Subnet**  
  Specifies the subnet in the virtual network.

  > A subnet is a range of IP addresses in the VNet. You can divide a VNet into multiple _subnets_ for organization and security. Each NIC in a VM is connected to one subnet in one VNet. NICs connected to subnets \(same or different\) within a VNet can communicate with each other without any extra configuration.
  >
  > See the following document for more information: [Virtual networks and virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/network-overview).

* **Storage**  
  Specifies the [disk storage](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/about-disks-and-vhds) on the target virtual machine.

  > The specified storage must belong to the same location and resource group as the specified _network _\(see above\). Otherwise, you will not be able to set up a virtual machine. See the following Knowledge Base article for more information: [Cannot specify all Azure Virtual Machine instance details in the restore wizard](https://kb.cloudberrylab.com/kb1063/).

* **Container**  
  Specifies the bucket to which the virtual machine's disks will be placed.

* **Boot diagnostic storage**  
  Specifies the storage for [boot diagnostic files](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/boot-diagnostics).

  > We strongly recommend that you never disable boot diagnostics when restoring a disk image on an Azure machine. Otherwise, you will not be able to find out the reason of why the restore process has failed. This is because an Azure virtual machine can only be accessed via the Remote Desktop Protocol \(RDP\), and unlike a VMware workstation, you cannot access an Azure virtual machine unless it has an operating system, network, RDP service and external IP address assigned to it.
  >
  > Boot diagnostics provides a machine's screenshot that may become critical for accessing the restored machine. Please keep in mind that Azure launches a virtual machine silently, without any warnings, and you will be charged regardless of whether or not its operating system has been launched and of whether or not you are able to access the restored machine.
  >
  > You need to use a regular storage account for storing boot diagnostics. The premium account is only used to store page blobs \(and virtual machine disks\) and comes at a much higher price as it uses SSD. See [Azure Managed Disks Overview](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/managed-disks-overview) for more information.

  Azure Virtual Machine Agent is not automatically installed during VM import. You can manually install it if required. See the following documents for more information:

  * [Azure Virtual Machine Agent overview](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/agent-user-guide)
    [OMS virtual machine extension for Windows](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/extensions-oms) [Virtual machine extensions and features for Windows](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/extensions-features)

* **Operating system**  
  Specifies the operating system of the target virtual machine.

  > If you are restoring a Windows virtual machine, we recommend that you do not select Linux.



