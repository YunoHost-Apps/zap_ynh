## Installation

Before installing, read the [Zap installation instructions](https://codeberg.org/zot/zap/src/branch/release/install/INSTALL.txt) for important information about:

### Register a new domain and add it to YunoHost

- Zap requires a dedicated domain, so obtain one and add it using the YunoHost admin panel. **Domains -> Add domain**. As Zap uses the full domain and is installed on the root, you can create a subdomain such as Zap.domain.tld. Don't forget to update your DNS if you manage them manually.

## LDAP Admin user rights, logs and failed database updates

- **For admin rights**: When installation is complete, you will need to visit your new hub's page and login with the **admin account username** which was entered at the time of installation process. You should then be able to create your first channel and have the **admin rights** for the hub.

- **For normal YunoHost users :** Normal LDAP users can login through Ldap authentication and create there channels.

- **Failing to get admin rights :** If the admin cannot access the admin settings at `https://zap.example.com/admin` or you want to grant admin rights to any other user(s) on the hub, then you have to **manually add 4096** to the **account_roles** under **accounts** for that user in the **database through phpMYAdmin**.

- **For logs:** Go to **admin->logs** and enter the file name **php.log**.

- **Failed Database after Upgrade:** Some times databse upgrade fails after version upgrade. You can go to hub eg. `https://zap.example.com/admin/dbsync/` and check the numbers of failled update. These updates will have to be ran manually by **phpMYAdmin**.
