## Preparing a Bootable USB/ISO Image for Bare Metal Recovery

With CloudBerry Backup, you can create a bootable USB drive or create ISO image file for an emergency "bare metal" recovery in case of a system or hardware crash.

> CloudBerry Backup runs under the Local System account by default. When running it under a user account, this user must be granted local administrator permissions to be able to make a recovery disk.

To create a recovery disk, switch to the **Home** tab of the CloudBerry Backup main menu and click the **Make Bootable USB** button.![](/assets/bare-metal-make-bootable-usb-menu.png)This invokes the **Create Recovery Disk** dialog window where you need to select a USB device or specify the ISO image file name for storing the recovery data.

![](/assets/bare-metal-make-bootable-usb-dialog.png)

> When selecting a USB device, please be informed that all information on it will be permanently lost after starting the disk creation process. Please backup all necessary information from the target USB device beforehand.

In addition, you can specify the following options:

* **Add CloudBerry Remote Assistant to the recovery disk**  
  This installs [CloudBerry Remote Assistant](https://www.cloudberrylab.com/remote-assistant.aspx)** **that will simplify the recovery process and provide you with additional features, such as ...

* **Protect the recovery disk with a master password**  
  We strongly recommend that you specify a password to protect the recovery drive against unauthorized access to any sensitive information that may be stored on it, such as ...

### Installing Additional Drivers

Next, you can install additional drivers to the recovery disk by specifying a folder where they are located.

> Use this option to be able to use this disk on a hardware configuration that is different from the current machine.

The specified folder must contain the required drivers in the INF file format \(EXE and other file types will be ignored\).

Most importantly, you need to add network drivers compatible with the target machine. Without such drivers, the boot disk will be unable to discover the network environment. A live network connection is required for recovering a disk image from a network share, as well as for WinPE installation.

> Normally, the operation system automatically installs [Windows Preinstallation Environment \(WinPE\)](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/winpe-intro) in a dedicated [recovery partition](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference). If the recovery disk is unable to locate a WinPE image in this partition, it prompts you to download and install an appropriate version of [Windows Assessment and Deployment Kit \(Windows ADK\)](https://www.microsoft.com/en-us/download/details.aspx?id=39982) or [Windows Automated Installation Kit \(AIK\)](https://www.microsoft.com/en-us/download/details.aspx?id=5753) which in turn, will install WinPE as well.

---

**min ADK 3 GB \(in memory???\)**

minimum setup \(2 options\)

---

Upon booting from a recovery disk, you can check the network access by running the "**ipconfig**" command in the **Command Prompt** that is available in the **Tools** category of the **CloudBerry Boot Menu** \(see the **CloudBerry Boot Menu** section of this document for more information\).

![](/assets/boot-menu-command-prompt.png)

The recovery disk will include information about all accounts that are currently available in CloudBerry Backup and you will be able to restore a disk image from any of these accounts after booting from the recovery disk. The available accounts are listed in the application's main menu.

![](/assets/backup-app-main-menu-accounts.png)

### Configuring a Network Share

To be able to restore a disk image from a network share, you need to configure a corresponding account before starting the recovery disk creation process.

> We do not recommend that you use a Local File system account because the recovery disk might change the drive letter in the path string.

To specify valid credentials so that the recovery disc is able to access the network share, switch to the Tools tab on the application's menu and click **Network Credentials**.

![](/assets/app-ribbon-tools-network-credentials.png)

### Configuring BIOS Settings

When booting from a recovery disk, you might need to customize some of the BIOS settings to make the recovery disk match the configuration of the current PC.

For example, you might not be able to restore a disk image unless the SATA configuration of the current PC matches that of a computer on which the recovery disk was created.

### CloudBerry Boot Menu

Booting from a recovery USB device or ISO disk image file opens the **CloudBerry Boot Menu**.

![](/assets/cloudberry-boot-menu.png)

This menu provides the following options:

* **Bare Metal Recovery**  
  Runs CloudBerry Backup where you can start the recovery process.

* **CloudBerry Remote Assistant**  
  This option is available when [CloudBerry Remote Assistant](https://www.cloudberrylab.com/remote-assistant.aspx) is installed on the recovery disk.  
  It enables you to allow remote control over the current PC or take control over another computer remotely.

* **Tools**  
  Provides various tools for configuring the restored machine. These tools include:

  * [Microsoft Windows Command Prompt](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)

    > See the [Command Line Interface](https://help.cloudberrylab.com/cloudberry-backup/miscellaneous/command-line-interface) for an overview of the native CloudBerry commands.

  * [Registry Editor](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-6.0/aa243964%28v=vs.60%29)

  * Save CloudBerry Backup application logs

### Changing the Virtual Disk Size

Upon loading, the recovery disk creates a virtual drive in the PC memory \(this drive is assigned the letter **X**\).

The virtual disk size varies depending on the operating system family and generally, it does not exceed **512 **MB.

This virtual disk is used to contain a repository storing the image-related data. Every time you boot from the restore disk, this repository is created from scratch.

When you are required to store an increased amount of image-related information, the repository might exceed the virtual disk size, which results in an error and the failure of the recovery process. To avoid this, you can check the required repository size before starting the recovery disk creation process by switching to the **Tools** tab of the application menu and clicking the **Options** button.

![](/assets/app-ribbon-tools-options.png)

This invokes the **Options **dialog window where you can switch to the **Repository **tab indicating the current database size.

![](/assets/backup-options-repository.png)

If it exceeds **512 **MB, you can shrink and/or relocate the repository.

**\[see "Moving repository file \(CBBackup.db\) to alternative location" at **[https://help.cloudberrylab.com/cloudberry-backup/miscellaneous/command-line-interface\](https://help.cloudberrylab.com/cloudberry-backup/miscellaneous/command-line-interface\)**\]**

### Troubleshooting

**Problem:**  
The boot disk cannot discover the network

**Possible solution \(our favorite one\):**  
Make sure that the network cable is connected.

---

**Problem:**  
When restoring a disk image from Amazon S3, the following error occurs: "The clock is not synchronized."

**Solution:**  
On the **CloudBerry Boot Menu**, switch to **Tools** and press **T** to synchronize the local and network clocks.

---

**Problem:**  
The disk image is not found.

**Possible solution:**  
Try changing the [backup prefix](/concepts/changing-the-backup-prefix.md) to make it match the name of a computer on which the disk image was created.

---



