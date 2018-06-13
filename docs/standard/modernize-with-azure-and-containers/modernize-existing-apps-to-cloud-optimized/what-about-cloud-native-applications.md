---
title: Que se passe-t-il pour les applications de Cloud en mode natif ?
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Que se passe-t-il pour les applications de Cloud en mode natif ?
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 0e880689001ece2b770811cfbe3fea43aa425b32
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2018
ms.locfileid: "33957989"
---
# <a name="what-about-cloud-native-applications"></a>Que se passe-t-il pour les applications de Cloud en mode natif ?

Bien que [natif Cloud](https://www.gartner.com/doc/3738117/comparing-leading-cloudnative-application-platforms) applications ne sont pas le principal objectif de ce guide, il est utile de comprendre de ce niveau de maturité modernisation et pour le distinguer des applications d’optimisée pour le Cloud.

Figure 4-3 positionne les applications Cloud en mode natif dans les niveaux de maturité modernisation application :

![Positionnement des applications de Cloud en mode natif](./media/image3.png)

> **Figure 4-3.** Positionnement des applications de Cloud en mode natif

Le niveau de maturité modernisation Cloud en mode natif nécessite généralement de nouveaux investissements de développement. Déplacement au niveau natif Cloud généralement vise le besoin de moderniser des applications autant que possibles afin d’améliorer considérablement les échelle dans les grandes applications en créant des sous-systèmes autonomes (microservices) qui peuvent être déployées et l’échelle indépendamment d’autres zones de l’application tout en réduisant les coûts de l’agilité d’évolution long pour le terme et l’augmentation des parties de ces applications autonomes qui fournissent des importantes sont en concurrence avantages. 

Principaux piliers de [natif Cloud](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications) applications sont basées sur les approches d’architecture microservices, ce qui peuvent évoluer avec souplesse et de répondre aux limites qui seraient difficiles à réaliser une architecture monolithique déployée soit en local ou l’environnement de cloud computing.

Figure 4-4 indique les principales caractéristiques du modèle de Cloud en mode natif.  

> ![Caractéristiques de cloud en mode natif sont Microservices, conteneurs, résilientes de cloud computing, orchestrators et serverles](./media/image4.png)
>
> **Figure 4-4.** Caractéristiques de cloud en mode natif

En outre, vous pouvez étendre les applications web modernes de base et les applications cloud en mode natif en ajoutant d’autres services, tels que l’intelligence artificielle (AI), apprentissage (ML) et IoT. Vous pouvez utiliser un de ces services pour étendre une des approches possibles optimisée pour le Cloud.

La différence fondamentale dans les applications au niveau du Cloud en mode natif est dans l’architecture d’application. [Cloud natif](https://www.gartner.com/doc/3738117/comparing-leading-cloudnative-application-platforms) applications sont, par définition, les applications qui reposent sur microservices. Les applications de cloud en mode natif nécessitent des architectures spéciales, technologies et plateformes, par rapport à une application web de monolithique ou d’une application multicouche classique.

## <a name="cloud-native-applications-details"></a>Détails des applications de cloud en mode natif

[Cloud natif](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications) est un état plus avancé ou mature pour les applications critiques volumineux. Les applications cloud en mode natif nécessitent généralement l’architecture et conception qui sont créés à partir de zéro à la place de par rénovation des applications existantes. La principale différence entre une application Cloud en mode natif et une application web Cloud optimisés plus simple est la recommandation d’utiliser des architectures de microservices dans une approche de cloud en mode natif. Optimisée pour le cloud des applications peuvent également être des applications web monolithique ou les applications multicouches.

Le [douze-facteur application](https://12factor.net/) (il s’agit d’une collection de modèles qui sont étroitement liés aux approches de microservices) est considérée également une exigence pour [cloud natif](https://www.gartner.com/doc/3738117/comparing-leading-cloudnative-application-platforms) architectures d’application.

Le [Foundation de calcul natif Cloud (CNCF)](https://www.cncf.io/) est un principal promoteur des principes de cloud en mode natif. Microsoft est un [membre de la CNCF](https://azure.microsoft.com/blog/announcing-cncf/).

Pour un exemple de définition et pour plus d’informations sur les caractéristiques des applications de cloud en mode natif, consultez l’article de Gartner [comment structurer et concevoir des applications de cloud natif](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications). Pour obtenir des instructions spécifiques à partir de Microsoft sur l’implémentation d’une application cloud en mode natif, consultez [.NET microservices : Architecture pour les applications .NET en conteneur](https://aka.ms/microservicesebook).

Le facteur le plus important à prendre en compte les si vous migrez une application complète pour la [natif cloud](https://www.gartner.com/doc/3738117/comparing-leading-cloudnative-application-platforms) modèle est que vous devez remanier pour une architecture basée sur des microservices. Clairement, cela nécessite un investissement important dans le développement en raison du grand processus de refactorisation impliqué. Cette option est généralement choisie pour les applications critiques qui ont besoin de nouveaux niveaux d’évolutivité et de souplesse à long terme. Mais, vous pouvez démarrer un déplacement vers le cloud en mode natif en ajoutant des microservices de quelques nouveaux scénarios et finalement refactoriser l’application entièrement comme microservices. Il s’agit d’une approche progressive qui est la meilleure option pour certains scénarios.

## <a name="what-about-microservices"></a>Qu’en est-il des microservices ? 

Si vous envisagez des applications cloud en mode natif pour votre organisation, il est important de comprendre microservices et leur fonctionnement.

L’architecture de microservices est une approche avancée que vous pouvez utiliser pour les applications qui sont créées à partir de zéro ou lorsque vous développez des applications existantes vers des applications de cloud en mode natif. Vous pouvez commencer par ajouter quelques microservices aux applications existantes pour en savoir plus sur les nouveaux modèles de microservices. Mais clairement, vous devez architecte et le code, en particulier pour ce type d’approche architecturale.

Toutefois, les microservices ne sont pas obligatoires pour toutes les applications nouvelles ou modernes. Microservices ne sont pas un « magique », et ils ne sont pas le seul, meilleures permet de créer chaque application. Comment et quand vous utilisez microservices dépend du type d’application que vous souhaitez générer.

L’architecture de microservices devient la meilleure approche pour les applications critiques distribuées et volumineux ou complexes qui sont basées sur des sous-systèmes indépendantes multiples, sous la forme de services autonomes. Dans une architecture basée sur des microservices, une application est générée comme une collection de services qui peuvent être développées indépendamment, testée et une version déployée et à l’échelle. Cela peut inclure une base de données connexe, autonome par microservice.

Pour une présentation détaillée sur une architecture de microservices que vous pouvez implémenter à l’aide de .NET Core, consultez l’e-livre PDF téléchargeable [.NET microservices : Architecture pour les applications .NET en conteneur](https://aka.ms/microservicesebook). Le guide est également disponible [online](../../microservices-architecture/index.md).

Mais même dans les scénarios dans lesquels microservices offrent des puissantes fonctionnalités indépendant du déploiement, les limites de sous-système fort et diversité technologique-ils déclenchent également de nombreux défis de nouveau. Les défis liés au développement d’applications distribuées, tels que les modèles de données fragmentés et indépendante ; Pour parvenir à communication résiliente entre microservices ; le besoin de cohérence éventuelle ; et la complexité opérationnelle. Microservices présentent un niveau supérieur de complexité par rapport aux applications monolithiques traditionnelles.

En raison de la complexité d’une architecture de microservices, uniquement les scénarios spécifiques et certains types d’applications conviennent pour les applications microservice. Ceux-ci incluent des applications volumineuses et complexes qui ont plusieurs évolution sous-systèmes. Dans ces cas, il convient d’investir dans une architecture plus complexe de logiciel, pour une souplesse accrue à long terme et la maintenance des applications plus efficace. Mais pour les scénarios moins complexes, il peut être préférable continuer avec une approche application monolithique ou multicouches plus simple est proche.

En tant qu’une note finale, même au risque d’être répétitive sur ce concept, vous ne doivent pas consulter à l’aide de microservices dans vos applications en tant que « tout dedans tout ou rien du tout. » Vous pouvez étendre et faire évoluer des applications monolithiques existantes en ajoutant de nouveaux, petits scénarios basés sur microservices. Vous n’avez pas besoin de démarrer à partir de zéro pour commencer à utiliser avec une approche d’architecture microservices. En fait, nous recommandons que vous développez à l’aide d’une application monolithique ou multicouches existant en ajoutant de nouveaux scénarios. Par la suite, vous pouvez décomposer l’application en composants autonomes ou microservices. Vous pouvez démarrer l’évolution de vos applications monolithiques dans une direction microservices, étape par étape.

Dans tous les cas, le reste de ce guide présent concentre surtout sur « aucune application basée sur des microservices », car cette aide ciblée principalement la modernisation des applications existantes qui ont généralement des architectures monolithiques ou multicouche.


>[!div class="step-by-step"]
[Précédent](microsoft-technologies-in-cloud-optimized-applications.md)
[Suivant](deploy-existing-net-apps-as-windows-containers.md)
