## 3.6 - Restore System State Data

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

![](/assets/restore-system-state-choice.png)

Then, proceed with the following wizard steps to configure your restore task:

* [3.6.1 - Select File Versions to Restore](/chapter1/step-3-choose-data-to-restore/35-restore-system-state-data/361-select-the-backup-type.md)
* [3.6.2 - Specify the Restore Source](/chapter1/step-3-choose-data-to-restore/35-restore-system-state-data/362-select-an-intermediate-storage.md)
* [3.6.3 - Specify the Restore Desination](/chapter1/step-3-choose-data-to-restore/35-restore-system-state-data/363-check-network-shares.md)



