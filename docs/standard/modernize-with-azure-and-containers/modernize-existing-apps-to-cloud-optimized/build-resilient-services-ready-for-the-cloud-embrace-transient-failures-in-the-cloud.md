---
title: Générer des services résilients prêts pour le cloud. gérer les échecs passagers dans le cloud
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Générer des services résilients prêts pour le cloud. gérer les échecs passagers dans le cloud
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/30/2018
ms.openlocfilehash: 801d017457d1cdc3c8a495c8127b203380cb1d9e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61811840"
---
# <a name="build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud"></a>Créer des services résilients compatibles avec le cloud : gérer les échecs passagers dans le cloud

La résilience est la capacité à surmonter les défaillances et à continuer de fonctionner. La résilience n’est pas sur éviter les défaillances, mais accepter le fait que les échecs seront produit et d’y répondre de façon à éviter la perte de données ni temps d’arrêt. La résilience vise à remettre l’application dans un état entièrement fonctionnel après une défaillance.

Votre application est prête pour le cloud lorsque, au minimum, il implémente un modèle basé sur les logiciels de résilience, plutôt qu’un modèle basé sur le matériel. Votre application cloud doit des défaillances partielles qui se produiront certainement. Concevoir ou partiellement refactoriser votre application pour obtenir la résilience des défaillances partielles attendus. Il doit être conçu pour faire face aux défaillances partielles, telles que les pannes réseau temporaires et des nœuds ou des machines virtuelles se bloque dans le cloud. Conteneurs voire déplacées vers un autre nœud dans un cluster orchestrateur peuvent provoquer des brèves défaillances intermittentes au sein de l’application.

## <a name="handling-partial-failure"></a>Gestion d’une défaillance partielle

Dans une application basée sur le cloud, il existe un risque permanente d’une défaillance partielle. Par exemple, une instance de site Web unique ou un conteneur peut échouer, ou il peut être indisponible ou ne répond pas pendant une courte période. Ou bien, une machine virtuelle ou un serveur unique peut se bloquer.

Étant donné que les clients et les services sont des processus distincts, un service n’est peut-être pas en mesure de répondre en temps voulu pour une demande du client. Le service peut être surchargé et répondre lentement aux demandes, ou il est peut-être pas accessible pendant une courte période en raison de problèmes de réseau.

Par exemple, considérez une application .NET monolithique qui accède à une base de données dans la base de données SQL Azure. Si la base de données SQL Azure ou tout autre service tiers ne répond pas pour un bref temps (une base de données SQL Azure peut-être être déplacé vers un autre nœud ou un serveur et être ne répond pas pendant quelques secondes), lorsque l’utilisateur tente d’effectuer d’action, l’application peut se bloquer et afficher w une exception au même moment.

Un scénario similaire peut se produire dans une application qui consomme les services HTTP. Le réseau ou le service proprement dit peut-être pas disponible dans le cloud lors d’une défaillance courte et temporaire.

Une application résiliente comme celui illustré dans la Figure 4-9 doit implémenter des techniques telles que « nouvelles tentatives avec interruption exponentielle » pour permettre à l’application de gérer les défaillances temporaires de ressources. Vous devez également utiliser « disjoncteurs » dans vos applications. Un disjoncteur arrête une application tente d’accéder à une ressource lorsqu’il est en fait une défaillance à long terme. En utilisant un disjoncteur, l’application évite ainsi provoquer un déni de service à lui-même.

![Défaillances partielles gérées par les nouvelles tentatives avec interruption exponentielle](./media/image9.png)

> **Figure 4-9.** Défaillances partielles gérées par les nouvelles tentatives avec interruption exponentielle

Vous pouvez utiliser ces techniques à la fois dans les ressources HTTP et les ressources de base de données. Dans la Figure 4-9, l’application est basée sur une architecture à 3 couches, donc vous avez besoin de ces techniques au niveau des services (HTTP) et au niveau de la couche données (TCP). Dans une application monolithique qui utilise uniquement un niveau d’application unique en plus de la base de données (sans les services supplémentaires ou microservices), traitement des défaillances temporaires au niveau de la connexion de base de données peuvent être suffisante. Dans ce scénario, simplement une configuration particulière de la connexion de base de données est nécessaire.

Lors de l’implémentation des communications souples qui accèdent à la base de données, selon la version de .NET que vous utilisez, il peut être simple (par exemple, [avec Entity Framework 6 ou version ultérieure](/ef/ef6/fundamentals/connection-resiliency/retry-logic). Il est simplement une question de la configuration de la connexion de base de données). Ou, vous devrez peut-être utiliser des bibliothèques supplémentaires telles que la [bloc applicatif de pannes gestion](https://docs.microsoft.com/previous-versions/msp-n-p/hh680934(v=pandp.50)) (pour les versions antérieures de .NET), ou même implémenter votre propre bibliothèque.

Lors de l’implémentation de nouvelles tentatives HTTP et coupe-circuits, la recommandation pour .NET consiste à utiliser le [Polly](https://github.com/App-vNext/Polly) bibliothèque qui cible .NET Framework 4.0, .NET Framework 4.5 et .NET Standard 1.1, qui inclut la prise en charge .NET Core.

Pour savoir comment implémenter des stratégies pour la gestion des défaillances partielles dans le cloud, consultez les références suivantes.

### <a name="additional-resources"></a>Ressources supplémentaires

- **Implémentation de la communication résiliente pour gérer une défaillance partielle**

    [https://docs.microsoft.com/dotnet/standard/microservices-architecture/implement-resilient-applications/partial-failure-strategies](../../microservices-architecture/implement-resilient-applications/partial-failure-strategies.md)

- **Entity Framework la résilience et nouvelle tentative logique de connexion (version 6 et versions ultérieure)**

    [https://docs.microsoft.com/ef/ef6/fundamentals/connection-resiliency/retry-logic](/ef/ef6/fundamentals/connection-resiliency/retry-logic)

- **Le bloc d’Application de gestion des erreurs temporaires**

- <https://docs.microsoft.com/previous-versions/msp-n-p/hh680934(v=pandp.50)>

- **Bibliothèque Polly pour les communications HTTP résilientes**

    https://github.com/App-vNext/Polly

>[!div class="step-by-step"]
>[Précédent](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)
>[Suivant](modernize-your-apps-with-monitoring-and-telemetry.md)
