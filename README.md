# ZAP for YunoHost

[![Integration level](https://dash.yunohost.org/integration/zap.svg)](https://dash.yunohost.org/appci/app/zap) ![](https://ci-apps.yunohost.org/ci/badges/zap.status.svg) ![](https://ci-apps.yunohost.org/ci/badges/zap.maintain.svg)  
[![Install Zap with YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=zap)

> *This package allow you to install ZAP quickly and simply on a YunoHost server.
If you don't have YunoHost, please see [here](https://yunohost.org/#/install) to know how to install and enjoy it.*


Version: 21.02.11

### Interesting links

- [YunoHost project](https://yunohost.org)
- [Zap website](https://zotlabs.com/zap/)
- [Zap code on codeberg](https://codeberg.org/zot/zap)
- [Zap addons on codeberg](https://codeberg.org/zot/zap-addons)


## Overview

[Zap](https://zotlabs.com/zap/) is an an ethical alternative to Fediverse that provides powerful features for creating interconnected websites featuring a decentralized identity, communications, and permissions framework built using common webserver technology.

Compatible with **Mastodon**, **Pleroma**, **Pixelfed**, **Friendica**, **Hubzilla**, **Funkwhale**, **Peertube**, **Plume**, **WriteFreely** and many, many more.

**Shipped version:**  21.02.05

## Unique Features of ZAP

- **Groups** : public, private, and moderated.
- **Events** : Calendar and attendance; automatic birthday notifications for friends using this feature.
- **Cloud**storage : Built-in network file storage integrated with social networking access.
- **Editor** : Supports both markdown and bbcode. Use either or both - if you want.
- **Share**: Drag-and-drop a number of different things such as files, photos, webpages, maps, phone numbers to share- them.
- **Lists**: Sometimes referred to as circles or aspects, this lets you define your own groups of related friends and- communicate with them as a private group.
- **Extend** : Change or upgrade your software functionality as desired by installing additional features from addons and- the free app collection.

## This app claims following features:
- [X] Ldap integration
- [X] Multi-instance
- [X] Adeed php.log in the root folder for debugging php, with logrotate applied on it (can be accesssed by **admin->logs** and entering the **php.log**).
- [X] Fail2ban
- [X] Option to choose between **Mysql** and **PostgreSQL**.

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

* x86-64 - [![Build Status](https://ci-apps.yunohost.org/ci/logs/Zap%20%28Official%29.svg)](https://ci-apps.yunohost.org/ci/apps/zap/)
* ARMv8-A - [![Build Status](https://ci-apps-arm.yunohost.org/ci/logs/Zap%20%28Official%29.svg)](https://ci-apps-arm.yunohost.org/ci/apps/zap/)

## Links

 * YunoHost project: https://yunohost.org
 * Zap website: https://zotlabs.com/zap/
 * Zap code on codeberg: https://codeberg.org/zot/zap
 * Zap addons on codeberg: https://codeberg.org/zot/zap-addons

---

## Developer info

Please send your pull request to the [testing branch](https://github.com/YunoHost-Apps/zap_ynh/tree/testing).

To try the testing branch, please proceed like that.
```
sudo yunohost app install https://github.com/YunoHost-Apps/zap_ynh/tree/testing --debug
or
sudo yunohost app upgrade zap -u https://github.com/YunoHost-Apps/zap_ynh/tree/testing --debug
```
