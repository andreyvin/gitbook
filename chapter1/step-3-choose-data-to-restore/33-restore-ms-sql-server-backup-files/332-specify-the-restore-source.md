## 3.2.3 - Specify the Restore Source

On this wizard page, you can select the databases whose backup files you wish to restore from the specified SQL Server instance.

![](/assets/restore-sql-source.png)

If some of the databases are missing in the file explorer, this may be because your repository has not yet been synchronized to make the file tree reflect the latest modification made to your storage. In this case, you might need to manually launch the synchronization process by clicking the corresponding link on this wizard page.

![](/assets/synchronize-repository-dialog-window.png)

> Please be informed that such synchronization may take up to several hours. This is why we do not recommend you to force synchronization unless this is absolutely necessary.
>
> See the following topic to learn how to synchronize data from Amazon Glacier and other cloud storage providers: [Synchronizing Your Repository](/concepts/synchronizing-your-repository.md).



