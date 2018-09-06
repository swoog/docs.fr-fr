---
title: État et données dans les applications Docker
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 78db191bdec4c25c11728d819d89eaaaff4bd7da
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43801045"
---
# <a name="state-and-data-in-docker-applications"></a>État et données dans les applications Docker

Une primitive de conteneurs est immuabilité. Par rapport à une machine virtuelle, les conteneurs ne disparaissent en tant qu’une occurrence courante. Une machine virtuelle peut échouer dans différentes formes à partir des processus obsolètes, surcharge de l’UC ou un disque complet ou ayant échoué. Pourtant, nous pensons que la machine virtuelle soit disponible et disques RAID sont très courants pour vous assurer de défaillances de disque conserver les données.

Toutefois, les conteneurs sont considérés être des instances de processus. Un processus ne conserve pas état durable. Même si un conteneur peut écrire dans son stockage local, en supposant que cette instance sera présente indéfiniment serait équivalente à en supposant qu'une copie unique de mémoire pourra perdurer. Vous devez supposer que les conteneurs, comme les processus, sont dupliqués, arrêté, ou quand gérée avec un orchestrateur de conteneurs, ils peuvent être déplacés.

Docker utilise une fonctionnalité appelée un *système de fichiers de superposition* pour implémenter un processus de copie sur écriture qui stocke une informations mises à jour au système de fichiers racine d’un conteneur, par rapport à l’image d’origine sur lequel il est basé. Ces modifications sont perdues si le conteneur est supprimé par la suite à partir du système. Un conteneur, par conséquent, n’a pas le stockage persistant par défaut. Bien qu’il soit possible d’enregistrer l’état d’un conteneur, conception d’un système de contourner ce problème serait en conflit avec le principe de l’architecture de conteneur.

Pour gérer les données persistantes dans les applications Docker, il existe des solutions courantes :

-   [**Volumes de données**](https://docs.docker.com/engine/tutorials/dockervolumes/) ces montent à l’hôte, comme mentionné plus haut uniquement.

-   [**Conteneurs de volumes de données**](https://docs.docker.com/engine/tutorials/dockervolumes/#/creating-and-mounting-a-data-volume-container) ceux-ci fournissent un stockage partagé entre les conteneurs, à l’aide d’un conteneur externe qui peut faire.

-   [**Plug-ins de volume**](https://docs.docker.com/engine/tutorials/dockervolumes/#/mount-a-shared-storage-volume-as-a-data-volume) ces monter les volumes vers des emplacements distants, en fournissant une persistance à long terme.

-   **Sources de données distantes** exemples incluent des bases de données SQL et NoSQL ou cache des services tels que Redis.

-   [**Stockage Azure**](https://docs.microsoft.com/azure/storage/) ainsi en tant que service (PaaS) stockage, qui offre le meilleur de conteneurs de persistance à long terme comme plateforme distribuable géo.

Volumes de données sont désignés spécialement les répertoires au sein d’un ou plusieurs conteneurs qui contournent le [Union système de fichiers](https://docs.docker.com/glossary/?term=Union%20file%20system). Volumes de données sont conçus pour mettre à jour les données, indépendamment du cycle de vie du conteneur. Docker par conséquent jamais supprime automatiquement les volumes lorsque vous supprimez un conteneur, ni sera-t-il volumes « collecter garbage » qui ne sont plus référencés par un conteneur. Le système d’exploitation hôte peut parcourir et modifier les données dans n’importe quel volume de librement, ce qui est simplement une autre raison d’utiliser des volumes de données avec parcimonie.

Un [conteneur de volumes de données](https://docs.docker.com/glossary/?term=volume) est une amélioration des volumes de données standard. Il est essentiellement un conteneur dormant qui a un ou plusieurs volumes de données créés qu’il contient (comme décrit précédemment). Le conteneur de volumes de données fournit un accès aux conteneurs à partir d’un point de montage central. L’avantage de cette méthode d’accès est qu’il fournit une abstraction l’emplacement des données d’origine, ce qui le conteneur de données à un point de montage logique. Il permet également de conteneurs « application » accèdent aux volumes de conteneur de données pour être créés et détruits tout en conservant les données persistantes dans un conteneur dédié.

Figure 4-5 montre que les volumes Docker standard peuvent être placées sur le stockage hors les conteneurs eux-mêmes, mais dans les limites physiques du serveur/machine virtuelle hôte. *Volumes docker n’ont pas la possibilité d’utiliser un volume à partir d’un ordinateur hôte serveur/machine virtuelle à un autre*.

![](./media/image5.png)

Figure 4-5 : volumes de données et sources de données externes pour les applications de conteneurs/conteneurs

En raison de l’incapacité à gérer les données partagées entre les conteneurs qui s’exécutent sur des hôtes physiques distincts, il est recommandé de pas utiliser des volumes de données d’entreprise, sauf si l’hôte Docker est un ordinateur hôte/virtuel fixe, car lorsque vous utilisez des conteneurs Docker dans un orchestrateur, les conteneurs sont supposées être déplacées vers un autre hôte, selon les optimisations à effectuer par le cluster.

Par conséquent, les volumes de données régulières sont un bon mécanisme pour travailler avec des fichiers de trace, temporelles fichiers ou n’importe quel concept similaire qui n’affecte pas la cohérence des données métier si ou quand vos conteneurs sont déplacées entre plusieurs hôtes.

[Plug-ins de volume](https://docs.docker.com/engine/extend/plugins_volume/) fournissent des données sur tous les hôtes dans un cluster. Bien que pas tous les plug-ins de volume sont créés de manière égale, plug-ins de volume généralement fournir le stockage persistant externalisé fiable à partir des conteneurs immuables.

Sources de données distantes et des caches comme base de données SQL, DocumentDB ou un cache à distance comme Redis serait identique développements sans conteneurs. Il s’agit d’une des manières préféré et éprouvée, pour stocker les données d’application métier.


>[!div class="step-by-step"]
[Précédent](monolithic-applications.md)
[Suivant](soa-applications.md)
