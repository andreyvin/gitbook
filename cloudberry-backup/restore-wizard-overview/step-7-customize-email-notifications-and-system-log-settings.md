# Step 7 - Customize Email Notifications and System Log Settings

You can choose whether you need to receive email notifications informing you about the restore process results, and maintain a system activity log.

![](https://github.com/robertzakiev/gitbook/tree/703d9f96af3546d5a85e17cd24df8e3834d130e4/assets/customize-email-notifications.png)

You can receive email notifications after each run of the restore routine or only in case if it fails for some reason.

You can specify one or more email recipients \(separated by a semicolon or comma\), the recipient name \(one for all of them\), and the email subject that can also contain any of the following templates:

* **%COMPUTER\_NAME%** Indicates the name of a computer on which the routine was running.
* **%RESULT%** Indicates whether the routine was finished successfully or failed.
* **%PLAN\_NAME%** Indicates the restore plan's name.

You can also route the email notifications to a custom SMTP server. After specifying the server address, port, sender email and SSL settings, you can send a test email to make sure that the specified settings are valid.

![](https://github.com/robertzakiev/gitbook/tree/703d9f96af3546d5a85e17cd24df8e3834d130e4/assets/smtp-settings-dialog-window.png)

In addition, you can register the activity related to the restore routine in the [System Event Log](https://msdn.microsoft.com/en-us/library/windows/desktop/aa385780%28v=vs.85%29.aspx). You can choose whether to log all activity, or add new entries to the log only when a restore routine fails.

