## 3.2.5 - Specify the Database Options

On this wizard page, you can specify additional options for the restored database.

![](/assets/restore-sql-db-options.png)

The following options are available on this wizard page:

* **Data file folder**
  Specifies the location for MDF files containing database schema and data information.

* **Log file folder**
  Specifies the location for LDF files containing logs.

* **File name template**
  Enables you to specify a custom template for naming the restored MDF and LDF files.

  > You can specify the **%DATABASENAME%** template to make the wizard automatically generate these names according to the restored database name.

In addition, you can choose whether the wizard should close all existing connections to the destination database by enabling the corresponding option on this wizard page.



