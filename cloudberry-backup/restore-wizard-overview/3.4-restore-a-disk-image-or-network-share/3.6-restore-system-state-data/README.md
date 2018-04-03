# 3.6 - Restore System State Data

> This feature is only available for Windows Server editions of CloudBerry Backup.

A system state backup includes essential data related to an operating system. A typical Windows system state backup contains the following data:

* Windows System Registry
* Performance Counter Configuration information
* Component Services Class registration database
* Boot and system files, including those protected by Windows File Protection \(WFP\)
* Configuration of system-dependent Microsoft applications, such as Certificate Services, Active Directory, and Internet Information Services \(IIS\)

A system state backup can protect you from configuration-dependent system faults and file or system registry corruption.

> When restoring a system state, you cannot restore only some part of it because system state is always stored as a single object.

To restore a system state information, select the corresponding option in the Restore Wizard.

![](https://github.com/robertzakiev/gitbook/tree/703d9f96af3546d5a85e17cd24df8e3834d130e4/assets/restore-system-state-choice.png)

Then, proceed with the following wizard steps to configure your restore task:

* [3.6.1 - Select File Versions to Restore](3.6.1-select-file-versions-to-restore.md)
* [3.6.2 - Specify the Restore Source](3.6.2-specify-the-restore-source.md)
* [3.6.3 - Specify the Restore Desination](3.6.3-specify-the-restore-desination.md)

