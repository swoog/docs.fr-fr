---
title: Présentation des applications cloud natives
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Qu’en est-il des applications Cloud natives ?
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 10f7761b7c0d2ddd8cb9247b1a02aa49cdc4e5d4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62012098"
---
# <a name="what-about-cloud-native-applications"></a>Présentation des applications cloud natives

Bien que [Cloud natives](https://azure.microsoft.com/overview/cloudnative/) applications ne sont pas le principal objectif de ce guide, il est utile de comprendre de ce niveau de maturité de modernisation et pour le différencier des applications optimisé pour le Cloud.

Figure 4-3 positionne les applications Cloud natives dans les niveaux de maturité de modernisation application :

![Positionnement des applications Cloud natives](./media/image3.png)

> **Figure 4-3.** Positionnement des applications Cloud natives

Le niveau de maturité de modernisation Cloud natives nécessite généralement de nouveaux investissements de développement. Passer au niveau de Cloud natives généralement vise le doivent les moderniser des applications autant que possibles afin d’améliorer considérablement la mise à l’échelle dans les grandes applications en créant des sous-systèmes autonomes (microservices) qui peuvent être déployées et mise à l’échelle indépendamment à partir d’autres zones de l’application tout en réduisant les coûts de l’agilité d’évolution long pour le terme et augmentation des parties de l’application de ces autonomes qui fournissent significatives sont en concurrence avantages.

Les principaux piliers des applications Cloud natives sont basées sur les approches d’architecture de microservices, ce qui peuvent évoluer avec souplesse et mettre à l’échelle des limites qui serait difficile à réaliser dans une architecture monolithique, déployée en local ou cloud environnement.

Figure 4-4 illustre les principales caractéristiques du modèle de Cloud natives.

> ![Caractéristiques de cloud natives sont les Microservices, les orchestrateurs de conteneurs, résilientes sur le cloud et sans serveur](./media/image4.png)
>
> **Figure 4-4.** Caractéristiques de cloud natives

En outre, vous pouvez étendre les applications web modernes de base et les applications cloud natives en ajoutant d’autres services, tels que l’intelligence artificielle (IA), machine learning (ML) et IoT. Vous pouvez utiliser un de ces services pour étendre une des approches possibles optimisé pour le Cloud.

La différence fondamentale dans des applications au niveau du Cloud Native est dans l’architecture d’application. Applications cloud natives sont, par définition, les applications qui reposent sur des microservices. Applications cloud natives requièrent des architectures spéciales, technologies et plateformes, par rapport à une application web monolithique ou d’une application multiniveau classique.

## <a name="cloud-native-applications-details"></a>Détails des applications cloud natives

Cloud natives est un état plus avancé ou réservé aux adulte pour les applications métier critiques et de grande taille. Applications cloud natives requièrent généralement architecture et la conception qui sont créés à partir de zéro à la place d’en modernisant les applications existantes. La principale différence entre une application Cloud natives et une application web optimisé pour le Cloud plus simple est la recommandation d’utiliser des architectures de microservices dans une approche de cloud natives. Optimisé pour le cloud des applications peuvent également être des applications web monolithiques ou applications multiniveaux.

Le [applications 12 facteurs](https://12factor.net/) (il s’agit d’une collection de modèles qui sont étroitement liés aux approches de microservices) est considérée également comme une exigence pour les architectures d’application de cloud natives.

Le [Foundation de calcul natif Cloud (CNCF)](https://www.cncf.io/) est un promoteur principal des principes de cloud natives. Microsoft est un [membre de la CNCF](https://azure.microsoft.com/blog/announcing-cncf/).

Pour un exemple de définition et pour plus d’informations sur les caractéristiques des applications cloud natives, consultez l’article du cabinet Gartner [comment structurer et concevoir des applications cloud natives](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications). Pour obtenir des instructions spécifiques à partir de Microsoft sur la façon d’implémenter une application cloud natives, consultez [.NET microservices : Architecture des applications .NET en conteneur](https://aka.ms/microservicesebook).

Le facteur le plus important à prendre en compte si vous migrez une application complète pour le modèle de cloud natives est que vous devez remanier pour une architecture basée sur des microservices. Clairement, cela nécessite un investissement significatif dans le développement en raison du processus de refactorisation volumineux impliqué. Cette option est généralement choisie pour les applications stratégiques nécessitant des nouveaux niveaux d’évolutivité et l’agilité à long terme. Mais, vous pouvez commencer à déplacer vers le cloud natives en ajoutant des microservices de seulement quelques nouveaux scénarios et finalement refactoriser l’application entièrement en tant que microservices. Il s’agit d’une approche progressive de la meilleure option pour certains scénarios.

## <a name="what-about-microservices"></a>Qu’en est-il des microservices ?

Lorsque vous devez considérer les applications cloud natives pour votre organisation, il est important de comprendre les microservices et leur fonctionnement.

L’architecture de microservices est une approche avancée que vous pouvez utiliser pour les applications qui sont créées à partir de zéro ou lorsque vous faire évoluer les applications existantes vers les applications cloud natives. Vous pouvez commencer en ajoutant quelques microservices pour des applications existantes pour en savoir plus sur les nouveaux paradigmes de microservices. Mais vous devrez clairement, architecte et le code, en particulier pour ce type d’approche architecturale.

Toutefois, les microservices ne sont pas obligatoires pour n’importe quelle application nouvelle ou moderne. Microservices ne sont pas « recette miracle », et ils ne sont pas le seul, meilleures permettent de créer toutes les applications. Comment et quand vous utilisez des microservices varie selon le type d’application dont vous avez besoin pour générer.

L’architecture de microservices devient la meilleure approche pour les applications stratégiques distribuées et complexes ou volumineux qui sont basées sur des sous-systèmes indépendants plusieurs, sous la forme de services autonomes. Dans une architecture basée sur des microservices, une application est générée comme une collection de services qui peuvent être développées indépendamment, testés, versionnés, déployés et mis à l’échelle. Cela peut inclure une base de données connexe, autonome par microservice.

Pour un aperçu plus détaillé une architecture de microservices que vous pouvez implémenter à l’aide de .NET Core, consultez le PDF de livre électronique téléchargeable [.NET microservices : Architecture des applications .NET en conteneur](https://aka.ms/microservicesebook). Ce guide est également disponible [online](../../microservices-architecture/index.md).

Mais même dans les scénarios dans lesquels les microservices offrent de puissantes fonctionnalités indépendant du déploiement, des limites de sous-systèmes et la diversité de technologie-ils soulèvent aussi de nombreux nouveaux défis. Les défis liés au développement d’application distribuée, tels que les modèles de données fragmentés et indépendants ; réalisation d’une communication résiliente entre les microservices ; la nécessité de la cohérence à terme ; et une complexité opérationnelle. Microservices présentent un niveau plus élevé de complexité par rapport aux applications monolithiques traditionnelles.

En raison de la complexité d’une architecture de microservices, uniquement des scénarios spécifiques et sur certains types d’application sont idéales pour applications de microservice. Ceux-ci incluent des applications volumineuses et complexes qui ont plusieurs, en constante évolution des sous-systèmes. Dans ce cas, il est judicieux d’investir dans une architecture logicielle plus complexe, pour une souplesse accrue à long terme et la maintenance des applications plus efficace. Mais pour les scénarios moins complexes, il peut être préférable de continuer avec une approche de l’application monolithique ou multiniveau plus simple est proche.

Comme une remarque finale, même au risque d’être répétitive sur ce concept, vous ne doivent pas consulter à l’aide de microservices dans vos applications en tant que « tout dedans tout ou rien du tout. » Vous pouvez étendre et faire évoluer des applications monolithiques existantes en ajoutant de nouveaux, petits scénarios basées sur des microservices. Vous n’avez pas besoin de démarrer à partir de zéro pour commencer à travailler avec une approche d’architecture de microservices. En fait, nous recommandons que vous faire évoluer à partir de l’aide d’une application monolithique ou multiniveau existante en ajoutant de nouveaux scénarios. Finalement, vous pouvez diviser l’application en composants autonomes ou des microservices. Vous pouvez commencer en constante évolution de vos applications monolithiques dans un sens de microservices, étape par étape.

Dans tous les cas, le reste de ce guide présent concentre la plupart de tous sur « aucune application basée sur des microservices », car ce guide cible principalement la modernisation des applications existantes qui ont généralement des architectures monolithiques ou multiniveau.

> [!div class="step-by-step"]
> [Précédent](microsoft-technologies-in-cloud-optimized-applications.md)
> [Suivant](deploy-existing-net-apps-as-windows-containers.md)
