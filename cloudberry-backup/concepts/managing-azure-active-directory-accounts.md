# Managing Azure Active Directory Accounts

Unlike Amazon Web Services that provides a [single IAM account](https://aws.amazon.com/iam/) for managing any user activity, Microsoft Azure uses different sets of credentials for backing up, storing and restoring data. See the following article to learn more about the Role-Based Access Control \(RBAC\) used in the Azure portal: [Use Role-Based Access Control to manage access to your Azure subscription resources](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#)

> A user must be assigned the **Owner** or **Contributor** role to be able to use Microsoft Azure services via CloudBerry Lab products. See the following article for more information: [Get started with Role-Based Access Control in the Azure portal](https://www.gitbook.com/book/yuriyshutov/restore-wizard-draft/edit#).

## Using Azure Active Directory to Access Azure Virtual Machines

Each Azure subscription is associated with one [Azure Active Directory \(AD\)](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-whatis). Users, groups, and applications from that directory can manage resources in the Azure subscription. Microsoft provides two different types of accounts, both of which can be linked to an Azure AD:

* **Personal account **\(can be referred to as _"Microsoft account"_, formerly known as _"Windows Live ID"_\)

  This account is linked to an individual and is not supposed to change after changing one's job. Such accounts cannot access services outside of their respective Azure AD.

* **Work or school account** \(sometimes, it is also called an "_organizational account"_\)  
  This account is tied to your company and is used to manage access to your Office 365, Azure cloud, SharePoint, and other services. Furthermore, this account can belong to one of the following domains:

  * **A local domain**
  * **An Azure AD**

  > It is important to keep in mind that external Azure AD users can be [invited to an Azure AD from outside](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b). Please be informed that invited users may not have access to your Azure Virtual Machine account via CloudBerry products. You need to manually add a new to the Azure AD instead. Otherwise, an [error will occur on an attempt to authorize using such user's credentials](https://kb.cloudberry.online/microsoft-azure/sorry-but-were-having-trouble-signing-you-in.-we-received-a-bad-request.).

## Restoring to Azure Virtual Machine Using a Personal Windows Account

When using a Desktop edition of CloudBerry backup to restore an image-based backup to an Azure virtual machine, you can sign in to the Azure portal using a _personal Microsoft account _\(see above\).

However, this feature is not supported in [CloudBerry Managed Backup \(MBS\)](https://www.cloudberrylab.com/managed-backup.aspx) where you can sign in only using an _organizational \("work or school"\) account_. The following error will be displayed on attempting to authenticate using a personal account in MBS:

> "Selected user account does not exist in tenant 'CloudBerry Lab' and cannot access the application 'ApplicationName' in that tenant. The account needs to be added as an external user in the tenant first. Please use a different account."

