## 3.2.4 - Specify the Database Names

On this wizard page, you can specify the names for the restored databases.

![](/assets/restore-sql-db-names-2.png)

You can select one of the default names when restoring system databases or specify a custom name on this wizard page.

When restoring to an already existing database, you can also choose whether to overwrite the current databases with their restored versions by including a a "**WITH REPLACE**" statement in the executed query.

> Please be informed that this option affects all selected databases.

> The wizard will not be able to overwrite an existing database unless you explicitly enable this option. It will display the following error on such an attempt, prompting you to enable this option or specify a custom database name.
>
> ![](/assets/restore-wizard-warning-restore-existing-db.png)
>
> The wizard will not be able to overwrite a "**master**" database.

See [System Databases](https://docs.microsoft.com/en-us/sql/relational-databases/databases/system-databases) for more information.

