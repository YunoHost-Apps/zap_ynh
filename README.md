# ZAP for YunoHost

[![Integration level](https://dash.yunohost.org/integration/zap.svg)](https://dash.yunohost.org/appci/app/zap)  
[![Install Nextcloud with YunoHost](https://install-app.yunohost.org/install-with-yunohost.png)](https://install-app.yunohost.org/?app=zap)

> *This package allow you to install ZAP quickly and simply on a YunoHost server.  
If you don't have YunoHost, please see [here](https://yunohost.org/#/install) to know how to install and enjoy it.*


Version: 2.6

### Interesting links

- [YunoHost project](https://yunohost.org)
- [Zap website](https://zotlabs.com/zap/)
- [Zap code on Framagit](https://framagit.org/zot/zap)
- [Zap addons on Framagit](https://framagit.org/zot/zap-addons)

## ZAP
[Zap](https://zotlabs.com/zap/) is a powerful platform for creating interconnected websites featuring a decentralized identity, communications, and permissions framework built using common webserver technology.

## This app claims following features:
- [X] Ldap integration
- [X] Multi-instance
- [X] Adeed php.log in the root folder for debugging php, with logrotate applied on it (can be accesssed by **admin->logs** and entering the **php.log**).
- [X] Fail2ban 



## Installation
Before installing, read the [ZAP installation instructions](https://framagit.org/zot/zap/blob/master/install/INSTALL.txt) for important information about


### Register a new domain and add it to YunoHost
- Zap requires a dedicated domain, so obtain one and add it using the YunoHost admin panel. **Domains -> Add domain**. As Hubzilla uses the full domain and is installed on the root, you can create a subdomain such as zap.domain.tld. Don't forget to update your DNS if you manage them manually.


#### YunoHost >= 2.5 :
Once the dedicated domain has been added to YunoHost, go again to the admin panel, go to domains then select your domain and click on "Install Let's Encrypt certificate".

### Install the ZAP application
Use the YunoHost admin panel to install Zap by entering the GitHub repo address in the custom app URL

		https://github.com/YunoHost-Apps/zap_ynh

Make sure to select your new domain created by the instruction in previous section as the application domain.

**For admin rights**: When installation is complete, you will need to visit your new hub's page and login with the **admin account username** which was entered at the time of installation process. You should then be able to create your first channel and have the admin rights for the hub.

**For normal YunoHost users:** Normal LDAP users can login through Ldap authentication and create there channels.

**If the admin cannot access the admin settings:** If the admin cannot access the admin settings at `https://zap.example.com/admin` or you want to grant admin rights to any other user(s) on the hub, then you have to **manually add 4096** to the **account_roles** under **accounts** for that user in the **database through phpMYAdmin**.

**For logs:** Go to **admin->logs** and enter the file name **php.log**. 

**Failed Database after Upgrade:** Some times databse upgrade fails after version upgrade. You can go to your hub eg. `https://zap.example.com/admin/dbsync/` and upgrade it manually.


#### Supported architectures

* x86-64b - [![Build Status](https://ci-apps.yunohost.org/ci/logs/zap%20%28Official%29.svg)](https://ci-apps.yunohost.org/ci/apps/zap/)
* ARMv8-A - [![Build Status](https://ci-apps-arm.yunohost.org/ci/logs/zap%20%28Official%29.svg)](https://ci-apps-arm.yunohost.org/ci/apps/zap/)
* Jessie x86-64b - [![Build Status](https://ci-stretch.nohost.me/ci/logs/zap%20%28Official%29.svg)](https://ci-stretch.nohost.me/ci/apps/zap/)
