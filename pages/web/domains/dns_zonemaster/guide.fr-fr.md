---
title: 'Utilisation de Zonemaster'
slug: zonecheck-de-votre-domaine
section: DNS et zone DNS
order: 08
---

**Dernière mise à jour le 01209/2022**

## Objectif

[Zonemaster](https://zonemaster.fr/) est un outil né de la colaboration entre l'AFNIC (registre français) et [The Swedish Internet Foundation](https://internetstiftelsen.se/en/) (registre Suédois) permettant d'analyser la configuration DNS (Domain Name System) d'un nom de domaine et d'identifier les éléments de configuration DNS qui peuvent être améliorés ou corrigés.

> [!primary]
>
> Pour mieux comprendre la notion de DNS,n'hésitez pas à lire l'indroduction de notre guides sur la [configuration d'une zone DNS](https://docs.ovh.com/fr/domains/editer-ma-zone-dns/)

## Prérequis

- Disposer d'un [nom de domaine](https://www.ovhcloud.com/fr/domain/)

## En pratique

### Champ de saisie

L'outil Zonemaster sert à vérifier la bonne configuration DNS sur un nom de domaine.

Pour vérifier la configuration actuelle d'un nom de domaine, saisissez votre nom de domaine, puis cliquez sur `check`{.action}

![domains](images/zonemaster01.jpg){.thumbnail}

Pour vérifier une configuration DNS qui a été préparée, mais pas encore appliqué sur le nom de domaine concerné, cochez la case `Options`{.action}

- **Serveurs DNS** : Saisissez les informations des serveurs DNS associés à un nom de domaine ou une zone DNS, puis cliquez sur le `+`{.action} pour valider votre saisie. La saisie d'une adresse IP est facultative.
- **Délégation du Signataire (enregistrement DS)**: Dans le cadre d'une protection DNSSEC, saisissez les éléments de l'enregistrement DS, puis cliquez sur `+`{.action} pour ajouter la valeur

Vous pouvez également forcer les vérifications uniquement sur un protocole IP, via les cases `Désactiver IPv6` et `Désactiver IPv4`

> [!primary]
>
> Lorsque vous saisissez un nom de domaine et que vous cliquez sur le bouton `Obtenir les données de la zone parente`{.action}, les serveur DNS associés au nom de domaine apparaitront

![domains](images/zonemaster01.jpg){.thumbnail}

### Resultat

Une fois le formulaire validé, le résultat apparaît après quelques instants :

- Si tout est au vert : Votre zone est correcte. Vous pouvez valider le changement de serveurs DNS depuis votre manager
- Si vous avez des éléments en rouge : Le détail du résultat vous permettra de mener les corrections nécessaires.

Attention, si vous avez des élements en rouge , il ne faut pas lancer de mise à jour de serveurs DNS sans savoir ce que vous faites, car l'opération lancée risquera d'être bloquée et vos services liés au domaines pourraient ne plus fonctionner.

![domains](images/img_3211.jpg){.thumbnail}

### Informations utiles

Si vous avez des questions concernant cet outil et ses fonctionnalités, je vous invite à vous rendre dans la rubrique [FAQ](https://zonemaster.net/faq) de ZoneMaster.

![domains](images/img_3212.jpg){.thumbnail}

## Aller plus loin

[Généralités sur les serveurs DNS](../generalites-serveurs-dns/){.external}.

[ Modification d'une zone DNS](https://docs.ovh.com/fr/domains/editer-ma-zone-dns/){.external} DNS OVHcloud.

[Ajouter un champ SPF à la configuration de son nom de domaine](../le-champ-spf/){.external}.

[Protégez votre domaine contre le Cache Poisoning avec le DNSSEC](https://www.ovhcloud.com/fr/domains/dnssec/){.external}.

Pour des prestations spécialisées (référencement, développement, etc), contactez les [partenaires OVHcloud](https://partner.ovhcloud.com/fr/).

Si vous souhaitez bénéficier d'une assistance à l'usage et à la configuration de vos solutions OVHcloud, nous vous proposons de consulter nos différentes [offres de support](https://www.ovhcloud.com/fr/support-levels/).

Échangez avec notre communauté d'utilisateurs sur <https://community.ovh.com>
