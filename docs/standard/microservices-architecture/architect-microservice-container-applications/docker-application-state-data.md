---
title: "État et données dans les applications Docker"
description: "Architecture de microservices .NET pour les applications .NET en conteneur | État et données dans les applications Docker"
keywords: Docker, Microservices, ASP.NET, Conteneur, SQL, Cosmos DB, Docker
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: ef11d89c39ee02d52dab29f949d1ac6be981d87f
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="state-and-data-in-docker-applications"></a>État et données dans les applications Docker

Dans la plupart des cas, vous pouvez considérer qu’un conteneur est une instance d’un processus. Un processus ne conserve pas un état persistant. Si un conteneur peut écrire dans son stockage local, supposer qu’une instance sera présente indéfiniment revient à supposer qu’un seul emplacement en mémoire pourra perdurer. Il convient de supposer que les images de conteneur, comme les processus, peuvent avoir plusieurs instances ou qu’ils seront finalement supprimés ; s’ils sont gérés avec un orchestrateur de conteneurs, il faut supposer qu’ils peuvent être déplacés d’un nœud ou d’une machine virtuelle à l’autre.

Docker fournit une fonctionnalité appelée *système de fichiers par superposition*. Elle implémente une tâche de copie sur écriture qui stocke les informations mises à jour dans le système de fichiers racine du conteneur. Ces informations s’ajoutent à l’image d’origine sur laquelle le conteneur est basé. Si le conteneur est supprimé du système, ces modifications sont perdues. Par conséquent, bien qu’il soit possible d’enregistrer l’état d’un conteneur dans son stockage local, la conception d’un système sur cette base serait en conflit avec le principe de la conception des conteneurs, qui sont par défaut sans état.

Les solutions suivantes sont utilisées pour gérer les données persistantes dans les applications Docker :

-   Les [volumes de données](https://docs.docker.com/engine/tutorials/dockervolumes/) qui se montent sur l’hôte.

-   Les [conteneurs de volumes de données](https://docs.docker.com/engine/tutorials/dockervolumes/#creating-and-mounting-a-data-volume-container) qui fournissent un stockage partagé entre les conteneurs en utilisant un conteneur externe.

-   Les [plug-ins de volume](https://docs.docker.com/engine/tutorials/dockervolumes/) qui montent des volumes sur des services distants, en fournissant une persistance à long terme.

-   Le service [Stockage Azure](https://docs.microsoft.com/azure/storage/), qui fournit un stockage géographiquement distribuable, offrant une bonne solution de persistance à long terme pour les conteneurs.

-   Des bases de données relationnelles distantes, comme [Azure SQL Database](https://azure.microsoft.com/services/sql-database/), ou des bases de données NoSQL, comme [Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/introduction), ou des services de cache, comme [Redis](https://redis.io/).

Ces options sont détaillées ci-dessous.

Les **volumes de données** sont des répertoires mappés du système d’exploitation hôte à des répertoires dans les conteneurs. Quand le code du conteneur a accès au répertoire, cet accès se fait en réalité à un répertoire sur le système d’exploitation hôte. Ce répertoire n’est pas lié à la durée de vie du conteneur lui-même, et le répertoire est accessible à partir du code qui s’exécute directement sur le système d’exploitation hôte ou par un autre conteneur qui mappe le même répertoire de l’hôte à lui-même. Ainsi, les volumes de données sont conçus pour rendre des données persistantes indépendamment de la durée de vie du conteneur. Si vous supprimez un conteneur ou une image de l’hôte Docker, les données rendues persistantes dans le volume de données ne sont pas supprimées. Les données d’un volume sont également accessibles depuis le système d’exploitation hôte.

Les **conteneurs de volumes de données** sont une évolution des volumes de données standard. Un conteneur de volumes de données est un conteneur simple contenant un ou plusieurs volumes de données. Le conteneur de volumes de données fournit un accès aux conteneurs à partir d’un point de montage central. Cette méthode d’accès aux données est pratique, car elle permet de faire abstraction de l’emplacement des données d’origine. Pour le reste, son comportement est similaire à celui d’un volume de données standard : les données sont donc rendues persistantes dans ce conteneur dédié indépendamment du cycle de vie des conteneurs de l’application.

Comme le montre la figure 4-5, les volumes Docker standard peuvent être stockés en dehors des conteneurs eux-mêmes, mais dans les limites physiques du serveur ou de la machine virtuelle hôte. Les conteneurs Docker ne peuvent cependant pas accéder à un volume depuis un serveur ou une machine virtuelle hôte à un autre. En d’autres termes, avec ces volumes, il n’est pas possible de gérer des données partagées entre des conteneurs qui s’exécutent sur des hôtes Docker différents.

![](./media/image5.png)

**Figure 4-5**. Volumes de données et sources de données externes pour des applications basées sur des conteneurs

De plus, quand des conteneurs Docker sont gérés par un orchestrateur, les conteneurs peuvent être « déplacés » entre les hôtes, en fonction des optimisations effectuées par le cluster. Par conséquent, il n’est pas recommandé d’utiliser des volumes de données pour les données métier. Ils constituent néanmoins un bon mécanisme pour travailler avec des fichiers de trace, des fichiers temporels ou des fichiers similaires qui n’ont pas d’impact sur la cohérence des données métier.

Les **plug-ins de volume** comme [Flocker](https://clusterhq.com/flocker/) fournissent un accès aux données sur tous les hôtes d’un cluster. Tous les plug-ins de volume ne sont pas créés de la même façon, mais ils offrent généralement un stockage persistant externalisé fiable à partir de conteneurs immuables.

Des **sources de données distantes et des outils de mise en cache**, comme Azure SQL Database, Azure Cosmos DB ou un cache à distance comme Redis, peuvent être utilisés dans des applications en conteneur de la même façon qu’ils sont utilisés dans des développements sans conteneurs. Il s’agit d’un moyen éprouvé pour stocker des données d’application métier.

**Stockage Azure** Les données métier doivent généralement être placées dans des ressources ou des bases de données externes, comme le service Stockage Azure. Concrètement, Stockage Azure fournit les services suivants dans le cloud :

-   Stockage Blob stocke les données des objets non structurés. Un objet blob peut être n’importe quel type de données texte ou binaires, comme des fichiers de document ou multimédias (fichiers image, audio et vidéo). Stockage Blob est également appelé Stockage d’objets.

-   Stockage Fichier offre un stockage partagé pour les applications héritées avec le protocole SMB standard. Les machines virtuelles et les services cloud Azure peuvent partager des données de fichiers entre des composants d’application via des partages montés. Les applications locales peuvent accéder aux données des fichiers d’un partage via l’API REST du service Fichier.

-   Stockage Table stocke les jeux de données structurés. Stockage Table est un magasin de données clé-attribut NoSQL, qui permet le développement rapide et un accès rapide à de grandes quantités de données.

**Bases de données relationnelles et bases de données NoSQL.** De nombreux choix sont disponibles pour les bases de données externes, qui vont des bases de données relationnelles, comme SQL Server, PostgreSQL ou Oracle, aux bases de données NoSQL, comme Azure Cosmos DB, MongoDB, etc. Ces bases de données ne sont pas présentées dans ce guide, car il s’agit d’un tout autre sujet.


>[!div class="step-by-step"]
[Précédent] (containerize-monolithic-applications.md) [Suivant] (service-oriented-architecture.md)
