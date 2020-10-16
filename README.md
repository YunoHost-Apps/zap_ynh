# ZAP for YunoHost

![Integration level](https://dash.yunohost.org/integration/zap.svg)(https://dash.yunohost.org/appci/app/zap) ![](https://ci-apps.yunohost.org/ci/badges/zap.status.svg) ![](https://ci-apps.yunohost.org/ci/badges/zap.maintain.svg)
[![Install Zap with YunoHost](https://install-app.yunohost.org/install-with-yunohost.png)](https://install-app.yunohost.org/?app=Zap)

> *This package allow you to install ZAP quickly and simply on a YunoHost server.
If you don't have YunoHost, please see [here](https://yunohost.org/#/install) to know how to install and enjoy it.*


Version: 2020-10

### Interesting links

- [YunoHost project](https://yunohost.org)
- [Zap website](https://zotlabs.com/zap/)
- [Zap code on codeberg](https://codeberg.org/zot/zap)
- [Zap addons on codeberg](https://codeberg.org/zot/zap-addons)

## ZAP
[Zap](https://zotlabs.com/zap/) is a powerful platform for creating interconnected websites featuring a decentralized identity, communications, and permissions framework built using common webserver technology.

## This app claims following features:
- [X] Ldap integration
- [X] Multi-instance
- [X] Adeed php.log in the root folder for debugging php, with logrotate applied on it (can be accesssed by **admin->logs** and entering the **php.log**).
- [X] Fail2ban
- [X] Choose between **Mysql** and
**PostgreSQL** database to be used for the Zap while installation.


## Installation
Before installing, read the [Zap installation instructions](https://codeberg.org/zot/zap/src/branch/release/install/INSTALL.txt) for important information about:


### Register a new domain and add it to YunoHost
- Zap requires a dedicated domain, so obtain one and add it using the YunoHost admin panel. **Domains -> Add domain**. As Zap uses the full domain and is installed on the root, you can create a subdomain such as Zap.domain.tld. Don't forget to update your DNS if you manage them manually.


## Ldap Admin user rights, logs and failed database updates

- **For admin rights**: When installation is complete, you will need to visit your new hub's page and login with the **admin account username** which was entered at the time of installation process. You should then be able to create your first channel and have the **admin rights** for the hub.

- **For normal YunoHost users :** Normal LDAP users can login through Ldap authentication and create there channels.

- **Failing to get admin rights :** If the admin cannot access the admin settings at `https://zap.example.com/admin` or you want to grant admin rights to any other user(s) on the hub, then you have to **manually add 4096** to the **account_roles** under **accounts** for that user in the **database through phpMYAdmin**.

- **For logs :**  Go to **admin->logs** and enter the file name **php.log**.

- **Failed Database after Upgrade :** Some times databse upgrade fails after version upgrade. You can go to hub  eg. `https://zap.example.com/admin/dbsync/` and check the numbers of failled update. These updates will have to be ran manually by **phpMYAdmin**.

#### Supported architectures

* x86-64b - [![Build Status](https://ci-apps.yunohost.org/ci/logs/Zap%20%28Official%29.svg)](https://ci-apps.yunohost.org/ci/apps/zap/)
* ARMv8-A - [![Build Status](https://ci-apps-arm.yunohost.org/ci/logs/Zap%20%28Official%29.svg)](https://ci-apps-arm.yunohost.org/ci/apps/zap/)
* Jessie x86-64b - [![Build Status](https://ci-stretch.nohost.me/ci/logs/Zap%20%28Official%29.svg)](https://ci-stretch.nohost.me/ci/apps/zap/)
