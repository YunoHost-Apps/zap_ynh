<!--
Nota bene : ce README est automatiquement généré par <https://github.com/YunoHost/apps/tree/master/tools/readme_generator>
Il NE doit PAS être modifié à la main.
-->

# Zap pour YunoHost

[![Niveau d’intégration](https://dash.yunohost.org/integration/zap.svg)](https://dash.yunohost.org/appci/app/zap) ![Statut du fonctionnement](https://ci-apps.yunohost.org/ci/badges/zap.status.svg) ![Statut de maintenance](https://ci-apps.yunohost.org/ci/badges/zap.maintain.svg)

[![Installer Zap avec YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=zap)

*[Lire le README dans d'autres langues.](./ALL_README.md)*

> *Ce package vous permet d’installer Zap rapidement et simplement sur un serveur YunoHost.*  
> *Si vous n’avez pas YunoHost, consultez [ce guide](https://yunohost.org/install) pour savoir comment l’installer et en profiter.*

## Vue d’ensemble

Zap est une alternative éthique à Fediverse qui fournit des fonctionnalités puissantes pour créer des sites Web interconnectés dotés d'un cadre décentralisé d'identité, de communications et d'autorisations construit à l'aide d'une technologie de serveur Web commune.

Compatible avec **Mastodon**, **Pleroma**, **Pixelfed**, **Friendica**, **Hubzilla**, **Funkwhale**, **Peertube**, **Plume**, **WriteFreely** et bien d'autres encore.

## Caractéristiques uniques de ZAP

- **Groupes** : publics, privés et modérés.
- **Événements** : Calendrier et participation ; notifications d'anniversaire automatiques pour les amis utilisant cette fonctionnalité.
- Stockage **Cloud** : stockage de fichiers réseau intégré intégré à l'accès aux réseaux sociaux.
- **Éditeur** : Prend en charge à la fois le markdown et le bbcode. Utilisez l'un ou les deux, si vous le souhaitez.
- **Partager** : faites glisser et déposez un certain nombre d'éléments différents tels que des fichiers, des photos, des pages Web, des cartes, des numéros de téléphone pour les partager.
- **Listes** : parfois appelées cercles ou aspects, cela vous permet de définir vos propres groupes d'amis liés et de communiquer avec eux en tant que groupe privé.
- **Extend** : modifiez ou mettez à niveau les fonctionnalités de votre logiciel comme vous le souhaitez en installant des fonctionnalités supplémentaires à partir des modules complémentaires et de la collection d'applications gratuites.

**Version incluse :** 21.11.28~ynh3
## :red_circle: Anti-fonctionnalités

- **Application non maintenue**: Ce logiciel n'est plus maintenu. Attendez-vous à ce qu'il ne fonctionne plus avec le temps, et que l'on découvre des failles de sécurité qui ne seront pas corrigées, etc.

## Documentations et ressources

- Site officiel de l’app : <https://codeberg.org/zot-archive/zap>
- Dépôt de code officiel de l’app : <https://codeberg.org/zot-archive/zap>
- YunoHost Store : <https://apps.yunohost.org/app/zap>
- Signaler un bug : <https://github.com/YunoHost-Apps/zap_ynh/issues>

## Informations pour les développeurs

Merci de faire vos pull request sur la [branche `testing`](https://github.com/YunoHost-Apps/zap_ynh/tree/testing).

Pour essayer la branche `testing`, procédez comme suit :

```bash
sudo yunohost app install https://github.com/YunoHost-Apps/zap_ynh/tree/testing --debug
ou
sudo yunohost app upgrade zap -u https://github.com/YunoHost-Apps/zap_ynh/tree/testing --debug
```

**Plus d’infos sur le packaging d’applications :** <https://yunohost.org/packaging_apps>
