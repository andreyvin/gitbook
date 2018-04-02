## 3.1.5 - Schedule your Restore Plan

On this wizard page, you can specify the schedule settings to make your restore routine run automatically.

![](/assets/schedule-your-restore-plan.png)

You can choose among the following options:

* **No schedule \(run manually\)**

  Select this option to disable automatic running of the restore routine.

* **Specific date**

  Select this option to specify the date and time at which to run the restore process.

* **Recurring**

  When you chose to save the restore plan earlier in this wizard, you can select this option to schedule your restore routine.

  You can make the restore routine run on a daily, weekly, monthly or yearly basis and specify the additional settings, such as the time at which the restore process should start.

  ![](/assets/schedule-recurring-options-dialog-window.png)

After choosing the appropriate scheduling settings, you can enable the following options:

* **Synchronize repository before restore**

  Select this option if you need to sync your repository before each run of the restore routine.

  > Before enabling this feature, please be informed that the sync process can be very time consuming and can take up to several hours.
  >
  > See the following article to learn more about using this feature: [Synchronizing Your Repository](/concepts/synchronizing-your-repository.md).

* **Stop the plan if it runs for...**

  Use this option to interrupt a restore process if it runs for too long.

* **Run missed scheduled backup immediately when computer starts up**

  This option is only available if you enabled restore on schedule. It makes a restore routine run automatically at startup, in case it was missed for any reason.



