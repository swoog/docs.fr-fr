---
title: État et données dans les applications Docker
description: Découvrez l’option disponible pour enregistrer l’état dans des applications en conteneur.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 30dde3ce44aa61fff3fad1841ae4a8b941573877
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61795448"
---
# <a name="state-and-data-in-docker-applications"></a>État et données dans les applications Docker

Dans la plupart des cas, vous pouvez considérer qu’un conteneur est une instance d’un processus. Un processus ne conserve pas un état persistant. Même si un conteneur peut écrire dans son stockage local, en supposant qu’une instance sera présente indéfiniment ressemble en supposant qu’un seul emplacement en mémoire pourra perdurer. Images de conteneur, comme les processus, doivent être évalués à plusieurs instances et qu’ils seront finalement supprimés ; s’ils sont gérés avec un orchestrateur de conteneurs, il doit être supposé qu’ils peuvent être déplacés d’un nœud ou une machine virtuelle à un autre.

Les solutions suivantes sont utilisées pour gérer les données persistantes dans les applications Docker :

À partir de l’hôte Docker, sous forme de [volumes Docker](https://docs.docker.com/engine/admin/volumes/) :

- Les **volumes** sont stockés dans une zone du système de fichiers hôte managée par Docker.

- **Lier les montages** peut mapper à n’importe quel dossier dans le système de fichiers hôte, afin que l’accès ne peut pas être contrôlé à partir d’un processus de Docker et peut poser un risque de sécurité comme un conteneur peut accéder à des dossiers du système d’exploitation sensibles.

- Les **montages tmpfs** sont semblables à des dossiers virtuels qui existent uniquement dans la mémoire de l’hôte et qui ne sont jamais écrits dans le système de fichiers.

À partir du stockage distant :

- [Stockage Azure](https://azure.microsoft.com/documentation/services/storage/) fournit un stockage géo-distribuable, offrant une bonne solution de persistance à long terme pour les conteneurs.

- Bases de données relationnelles distantes comme [base de données SQL Azure](https://azure.microsoft.com/services/sql-database/), bases de données NoSQL comme [Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/introduction), ou le cache des services tels que [Redis](https://redis.io/).

À partir du conteneur Docker :

- Docker fournit une fonctionnalité appelée *système de fichiers par superposition*. Cette fonction implémente une tâche de copie sur écriture que magasins informations mises à jour au système de fichiers racine du conteneur. Ces informations « fixe en haut de « l’image d’origine sur laquelle repose le conteneur. Si le conteneur est supprimé du système, ces modifications sont perdues. Par conséquent, bien qu’il soit possible d’enregistrer l’état d’un conteneur dans son stockage local, la conception d’un système basé sur cette fonctionnalité serait en conflit avec le principe de conception de conteneur, qui est sans état par défaut.

- Toutefois, les Volumes Docker est désormais la meilleure façon de gérer des données locales dans Docker. Si vous avez besoin de plus d’informations sur le stockage dans des conteneurs, vérifiez sur [des pilotes de stockage Docker](https://docs.docker.com/engine/userguide/storagedriver/) et [sur les images, les conteneurs et les pilotes de stockage](https://docs.docker.com/engine/userguide/storagedriver/imagesandcontainers/).

Vous trouverez ci-dessous des détails supplémentaires sur ces options.

Les **volumes** sont des répertoires mappés du système d’exploitation hôte à des répertoires situés dans les conteneurs. Quand le code du conteneur a accès au répertoire, cet accès se fait en réalité à un répertoire sur le système d’exploitation hôte. Ce répertoire n’est pas lié à la durée de vie du conteneur, il est managé par Docker et isolé de la fonctionnalité principale de la machine hôte. Ainsi, les volumes de données sont conçus pour rendre des données persistantes indépendamment de la durée de vie du conteneur. Si vous supprimez un conteneur ou une image de l’hôte Docker, les données rendues persistantes dans le volume de données ne sont pas supprimées.

Les volumes peuvent être nommés ou anonymes (par défaut). Les volumes nommés correspondent à l’évolution des **conteneurs de volumes de données**. Ils facilitent le partage de données entre les conteneurs. Volumes prennent également en charge les pilotes de volume qui vous permettent de stocker des données sur les hôtes distants, entre autres options.

**Lier les montages** ont été disponibles pendant une longue période et autoriser le mappage de n’importe quel dossier sur un point de montage dans un conteneur. Les montages de liaison ont plus de limitations que les volumes et présentent certains problèmes de sécurité importants. Les volumes sont donc l’option recommandée.

**`tmpfs` monte** sont des dossiers virtuels qui se trouvent uniquement dans la mémoire de l’hôte et ne sont jamais écrites dans le système de fichiers. Ils sont rapides et sécurisés, mais ils consomment de la mémoire et sont conçus uniquement pour des données non persistantes.

Comme le montre la figure 4-5, les volumes Docker standard peuvent être stockés en dehors des conteneurs eux-mêmes, mais dans les limites physiques du serveur ou de la machine virtuelle hôte. Les conteneurs Docker ne peuvent cependant pas accéder à un volume depuis un serveur ou une machine virtuelle hôte à un autre. En d’autres termes, avec ces volumes, il n’est pas possible de gérer les données partagées entre des conteneurs qui s’exécutent sur des hôtes Docker distincts. Toutefois, cela est possible avec un pilote de volume qui prend en charge les hôtes distants.

![Les volumes peuvent être partagés entre les conteneurs, mais uniquement sur le même hôte, sauf si vous utilisez un pilote distant qui prend en charge les hôtes distants. ](./media/image5.png)

**Figure 4-5**. Volumes et sources de données externes pour applications conteneurisées

De plus, quand des conteneurs Docker sont managés par un orchestrateur, ils peuvent être « déplacés » entre les hôtes, en fonction des optimisations effectuées par le cluster. Il n’est donc pas recommandé d’utiliser des volumes de données pour les données métier. Mais ils sont un bon mécanisme pour travailler avec des fichiers de trace, des fichiers temporelles, ou similaires, qui n’affectera pas la cohérence des données métier.

Des **sources de données distantes et des outils de mise en cache**, comme Azure SQL Database, Azure Cosmos DB ou un cache à distance comme Redis, peuvent être utilisés dans des applications en conteneur de la même façon qu’ils sont utilisés dans des développements sans conteneurs. Il s’agit d’un moyen éprouvé pour stocker des données d’application métier.

**Stockage Azure** Données d’entreprise doivent généralement être placés dans des ressources externes ou des bases de données, comme le stockage Azure. Stockage Azure fournit les services suivants dans le cloud :

- Stockage Blob stocke les données des objets non structurés. Un objet blob peut être n’importe quel type de données texte ou binaires, comme des fichiers de document ou multimédias (fichiers image, audio et vidéo). Stockage Blob est également appelé Stockage d’objets.

- Stockage de fichiers offre un stockage partagé pour les applications héritées utilisant le protocole SMB standard. Les machines virtuelles et les services cloud Azure peuvent partager des données de fichiers entre des composants d’application via des partages montés. Applications locales peuvent accéder à des données de fichier dans un partage via l’API REST de Service de fichier.

- Stockage Table stocke les jeux de données structurés. Stockage Table est un magasin de données clé-attribut NoSQL, qui permet le développement rapide et un accès rapide à de grandes quantités de données.

**Bases de données relationnelles et bases de données NoSQL.** De nombreux choix sont disponibles pour les bases de données externes, qui vont des bases de données relationnelles, comme SQL Server, PostgreSQL ou Oracle, aux bases de données NoSQL, comme Azure Cosmos DB, MongoDB, etc. Ces bases de données ne vont pas être expliqué dans le cadre de ce guide, car elles sont une autre rubrique complètement.

>[!div class="step-by-step"]
>[Précédent](monolithic-applications.md)
>[Suivant](soa-applications.md)
