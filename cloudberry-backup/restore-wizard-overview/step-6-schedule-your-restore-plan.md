# Step 6 - Schedule Your Restore Plan

While in most cases, it is not reasonable to run a restore routine on schedule, CloudBerry Backup Restore Wizard still provides such an option.

> When choosing to schedule a restore plan for reasons of regular emergency recovery, please be informed that the resulting ID will be different for every restored virtual machine instance, making it impossible to automatically override your virtual machine on a regular basis.

On this wizard page, you can specify the schedule settings to make your restore routine run automatically.

![](https://github.com/robertzakiev/gitbook/tree/703d9f96af3546d5a85e17cd24df8e3834d130e4/assets/schedule-your-restore-plan.png)

You can choose among the following options:

* **No schedule \(run manually\)   **Select this option to disable automatic running of the restore routine.
* **Specific date   **Select this option to specify the date and time at which to run the restore process.
* **Recurring    
  **When you chose to save the restore plan earlier in this wizard, you can select this option to schedule your restore routine.

  You can make the restore routine run on a daily, weekly, monthly or yearly basis and specify the additional settings, such as the time at which the restore process should start.

  ![](https://github.com/robertzakiev/gitbook/tree/703d9f96af3546d5a85e17cd24df8e3834d130e4/assets/schedule-recurring-options-dialog-window.png)

After choosing the appropriate scheduling settings, you can enable the following options:

* **Synchronize repository before restore    
  **Select this option if you need to sync your repository before each run of the restore routine.

  > Before enabling this feature, please be informed that the sync process can be very time consuming and can take up to several hours.
  >
  > See the following article to learn more about using this feature: [Synchronizing Your Repository](../concepts/making-the-file-tree-display-missing-backup-files.md).

* **Stop the plan if it runs for...    
  **Use this option to interrupt a restore process if it runs for too long.

  > We strongly suggest that you do not use this feature, because CloudBerry Backup is unable to predict the recovery time which may vary depending on a variety of factors, and premature termination of a recovery process may result in getting the restored data corrupted.

* **Run missed scheduled backup immediately when computer starts up   **This option is only available if you scheduled the restore routine. Enabling this option makes the restore process begin automatically after your computer starts up if the restore was not able to start at the appointed time for any reason.

