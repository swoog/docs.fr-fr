---
title: Architectures courantes des applications web
description: Architecturer des applications web modernes avec ASP.NET Core et Microsoft Azure | Architectures courantes des applications web
author: ardalis
ms.author: wiwagn
ms.date: 10/06/2017
ms.openlocfilehash: 943163ca4c82ad75f177ebe73559d909e7292c52
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33592494"
---
# <a name="common-web-application-architectures"></a>Architectures courantes des applications web

> « Si vous pensez qu’une bonne architecture est coûteuse, faites l’expérience d’une mauvaise architecture. »  
> _- Brian Foote et Joseph Yoder_

## <a name="summary"></a>Récapitulatif

La plupart des applications .NET conventionnelles sont déployées sous forme d’unités individuelles qui correspondent à un exécutable ou à une application web unique s’exécutant dans un seul domaine d’application IIS. C’est le modèle de déploiement le plus simple, qui convient parfaitement à beaucoup d’applications internes et applications publiques de petite taille. Toutefois, même avec ce déploiement en unités individuelles, la majorité des applications métier non triviales tirent avantage à avoir leur logique séparée en plusieurs couches.

## <a name="what-is-a-monolithic-application"></a>Qu’est-ce qu’une application monolithique ?

Une application monolithique est une application qui se comporte de façon totalement autonome. Elle peut avoir des interactions avec d’autres services ou magasins de données pendant son exécution, mais son comportement est fondamentalement géré en interne. L’ensemble de l’application est généralement déployée comme une seule unité. Quand une application monolithique doit faire l’objet d’une mise à l’échelle horizontale, en général, l’application entière est dupliquée sur plusieurs serveurs ou machines virtuelles.

## <a name="all-in-one-applications"></a>Des applications tout-en-un

L’architecture d’une application peut se réduire à un seul projet. Dans cette architecture, toute la logique de l’application est contenue dans un seul projet, compilé dans un assembly unique et déployé comme une seule unité.

Tout nouveau projet ASP.NET Core, créé dans Visual Studio ou à partir de la ligne de commande, est au début une simple application monolithique « tout-en-un ». Le projet contient le comportement complet de l’application, y compris la logique de présentation, métier et d’accès aux données. La figure 5-1 montre la structure de fichiers d’une application à projet unique.

**Figure 5-1.** Application ASP.NET Core à projet unique

![](./media/image5-1.png)

Dans un scénario de projet unique, la séparation des préoccupations s’obtient par l’utilisation de dossiers. Le modèle par défaut inclut des dossiers distincts pour les responsabilités des modèles, vues et contrôleurs du schéma MVC, ainsi que des dossiers supplémentaires pour les services et les données. Dans cette organisation, les détails de présentation doivent être limités autant que possible au dossier Vues, et les détails d’implémentation de l’accès aux données doivent être limités aux classes stockées dans le dossier Données. La logique métier doit résider dans les services et les classes contenus dans le dossier Modèles.

La solution monolithique à projet unique est simple, mais elle présente certains inconvénients. Le nombre de fichiers et de dossiers augmente à mesure que le projet grossit et devient plus complexe. Les préoccupations de l’interface utilisateur (modèles, vues, contrôleurs) sont réparties entre plusieurs dossiers qui ne sont pas regroupés par ordre alphabétique. Cela devient un réel problème quand des constructions de niveau interface utilisateur supplémentaires, telles que des filtres ou des classeurs de modèles (ModelBinder), sont ajoutées dans leurs propres dossiers. La logique métier est répartie entre les dossiers Modèles et les dossiers Services, mais les dépendances entre les classes contenues dans ces dossiers ne sont pas clairement indiquées. Cette mauvaise organisation au niveau du projet se traduit fréquemment par la création de [code spaghetti](http://deviq.com/spaghetti-code/).

Pour résoudre ces problèmes, les applications se transforment souvent en solutions à projets multiples, où chaque projet est censé résider dans une *couche* spécifique de l’application.

## <a name="what-are-layers"></a>Qu’est-ce qu’une architecture en couches ?

Quand une application devient complexe, un moyen de gérer cette complexité est de scinder l’application en fonction de ses responsabilités ou préoccupations. Basée sur le principe de séparation des préoccupations, cette solution contribue à maintenir le code base parfaitement organisé à mesure qu’il grossit, ce qui permet aux développeurs de retrouver facilement les fonctionnalités implémentées. L’architecture en couches offre d’autres avantages que la simple organisation du code.

En effet, l’organisation du code en couches permet également la réutilisation des fonctionnalités communes de bas niveau dans l’ensemble de l’application. Cette possibilité est intéressante, car elle réduit la quantité de code à écrire et permet la normalisation de l’application sur une implémentation unique, selon le principe DRY (« Ne vous répétez pas »).

Avec une architecture en couches, les applications peuvent appliquer des restrictions sur les échanges autorisés entre les différentes couches. Cela contribue à améliorer l’encapsulation. De cette façon, quand une couche est modifiée ou remplacée, seules les couches qui interagissent avec elle sont impactées. En limitant l’interdépendance des couches, l’impact des modifications peut être atténué afin qu’une modification donnée n’impacte pas l’application entière.

Les couches (et l’encapsulation) facilitent le remplacement des fonctionnalités dans l’application. Par exemple, une application peut initialement utiliser sa propre base de données SQL Server pour la persistance, mais plus tard choisir d’utiliser une stratégie de persistance basée sur le cloud ou située derrière une API web. Si l’application a correctement encapsulé son implémentation de persistance au sein d’une couche logique, cette couche spécifique de SQL Server peut être remplacée par une nouvelle couche qui implémente la même interface publique.

Outre la possibilité de permuter des implémentations en réponse à des changements ultérieurs dans les exigences, les couches d’application facilitent également la permutation des implémentations pour les besoins de test. Au lieu d’écrire des tests qui s’exécutent sur la couche des données réelles ou sur la couche de l’interface utilisateur de l’application, vous pouvez remplacer ces couches durant la phase de test par des implémentations fictives qui fournissent des réponses connues aux requêtes. Cette possibilité simplifie considérablement l’écriture des tests et rend leur exécution beaucoup plus rapide par rapport à l’exécution de tests dans l’infrastructure réelle de l’application.

La mise en couches logiques est une technique courante pour améliorer l’organisation du code dans les applications d’entreprise. Le code peut être organisé en couches de plusieurs façons.

> [!NOTE]
> Les *couches* représentent une séparation logique au sein de l’application. Si la logique de l’application est répartie physiquement entre plusieurs serveurs ou processus séparés, ces différentes cibles de déploiement physiques sont appelées *niveaux*. Il est possible, et relativement courant, de déployer une application en N couches sur un seul niveau.

## <a name="traditional-n-layer-architecture-applications"></a>Applications avec une architecture en N couches conventionnelle

La figure 5-2 illustre l’organisation la plus courante d’une logique d’application en couches.

**Figure 5-2.** Couches d’application classiques.

![](./media/image5-2.png)

Ces couches sont souvent abrégées comme ceci : UI (couche d’interface utilisateur), BLL (couche métier) et DAL (couche d’accès aux données). Avec cette architecture, les utilisateurs effectuent des requêtes par le biais de la couche UI, qui interagit uniquement avec la couche BLL. La couche BLL, à son tour, peut appeler la couche DAL pour les requêtes d’accès aux données. La couche UI ne doit pas faire de requêtes directes à la couche DAL, ni interagir avec persistance directement par d’autres moyens. De même, la couche BLL doit uniquement interagir avec persistance en passant par la couche DAL. De cette manière, chaque couche a sa propre responsabilité connue.

Cette approche en couches classique a un inconvénient, à savoir que les dépendances de compilation s’exécutent de haut en bas. Autrement dit, la couche UI dépend de la couche BLL, qui dépend elle-même de la couche DAL. La couche BLL, qui contient généralement la logique la plus importante de l’application, est dépendante des détails d’implémentation de l’accès aux données (et souvent de l’existence d’une base de données). Il est souvent difficile de tester la logique métier dans ce type d’architecture, car il faut utiliser une base de données de test. Le principe d’inversion des dépendances peut être une solution à ce problème, comme vous le verrez dans la section suivante.

La figure 5-3 montre un exemple de solution qui scinde l’application en trois projets par responsabilité (ou couche).

**Figure 5-3.** Application monolithique simple constituée de trois projets.

![](./media/image5-3.png)

Cette application utilise plusieurs projets à des fins d’organisation, mais en réalité, elle est déployée comme une seule unité, et ses clients interagissent avec elle en la considérant comme une application web unique. Cela simplifie nettement le processus de déploiement. La figure 5-4 montre comment Microsoft Azure peut héberger ce type d’application.

![](./media/image5-4.png)

**Figure 5-4.** Déploiement simple d’une application web Azure

Quand l’application doit grossir, des solutions de déploiement plus complexes et robustes peuvent être nécessaires. La figure 5-5 montre un exemple de plan de déploiement plus complexe qui prend en charge des fonctionnalités supplémentaires.

![](./media/image5-5.png)

**Figure 5-5.** Déploiement d’une application web sur Azure App Service

En interne, l’organisation de ce projet en plusieurs projets par responsabilité facilite la maintenance de l’application.

Il est possible d’augmenter ou de diminuer la taille des instances de cette unité pour tirer parti de l’extensibilité à la demande sur le cloud. L’augmentation de la taille des instances revient à ajouter de l’UC, de la mémoire, de l’espace disque ou d’autres ressources sur le ou les serveurs qui hébergent votre application. La diminution de la taille des instances revient à ajouter des instances supplémentaires de ces serveurs (physiques ou virtuels). Quand votre application est hébergée sur plusieurs instances, un équilibreur de charge assigne les requêtes aux différentes instances de l’application.

L’approche la plus simple pour mettre à l’échelle une application web dans Azure est de configurer la mise à l’échelle manuellement dans le plan App Service de l’application. La figure 5-6 illustre le tableau de bord Azure qui permet de configurer le nombre d’instances d’une application.

![](./media/image5-6.png)

**Figure 5-6.** Mise à l’échelle du plan App Service dans Azure.

## <a name="clean-architecture"></a>Architecture propre

Les applications conçues selon le principe d’inversion des dépendances et les principes DDD (conception pilotée par le domaine) présentent plus ou moins la même architecture. Les noms donnés à cette architecture ont beaucoup varié au fil des années. Au début, on l’a nommée architecture hexagonale, puis architecture ports-adaptateurs. Plus récemment, on l’a appelée [architecture en oignon](http://jeffreypalermo.com/blog/the-onion-architecture-part-1/) ou [architecture propre](https://8thlight.com/blog/uncle-bob/2012/08/13/the-clean-architecture.html). C’est le terme d’architecture propre que nous allons principalement utiliser dans ce livre électronique pour décrire l’architecture.

> [!NOTE]
> Ce terme s’applique aussi bien aux applications conçues selon les principes DDD qu’à celles qui ne le sont pas. Les premières peuvent être désignées sous le terme combiné « architecture DDD propre ».

L’architecture propre met la logique métier et le modèle d’application au centre même de l’application. Au lieu que la logique métier dépende des préoccupations de l’accès aux données ou d’une autre infrastructure, cette dépendance est inversée : les détails de l’infrastructure et de l’implémentation dépendent du noyau de l’application. Cela s’obtient par la définition d’abstractions, ou interfaces, dans la couche Noyau de l’application, lesquels sont ensuite implémentés par les types définis dans la couche Infrastructure. Cette architecture est souvent représentée sous la forme d’une série de cercles concentriques, à l’image des couches d’un oignon. La figure 5-X montre un exemple de ce style de représentation architecturale.

![](./media/image5-7.png)

**Figure 5-7.** Architecture propre ; représentation des couches en oignon

Dans ce diagramme, le flux des dépendances va du cercle extérieur vers le cercle le plus intérieur. Vous pouvez constater que la couche Noyau de l’application (qui tire son nom de sa position au centre de ce diagramme) n’a aucune dépendance sur les autres couches de l’application. Au centre même du diagramme se trouvent les entités et les interfaces de l’application. Juste après vers l’extérieur, mais toujours dans la couche Noyau de l’application, viennent les services de domaine, qui implémentent généralement les interfaces définies dans le cercle central. À l’extérieur de la couche Noyau de l’application, il y a les couches Interface utilisateur et Infrastructure. Ces deux couches dépendent de la couche Noyau de l’application, mais elles n’ont pas de dépendances entre elles (obligatoirement).

La figure 5-X montre une représentation horizontale des couches plus classique, qui reflète mieux la dépendance entre la couche Interface utilisateur et les autres couches.

![](./media/image5-8.png)

**Figure 5-8.** Architecture propre ; représentation horizontale des couches

Notez que les flèches pleines représentent les dépendances à la compilation, tandis que la flèche en pointillé représente une dépendance à l’exécution uniquement. Dans une architecture propre, la couche Interface utilisateur interagit avec les interfaces définies dans la couche Noyau de l’application au moment de la compilation. Dans l’idéal, elle ne doit pas avoir connaissance des types d’implémentation définis dans la couche Infrastructure. Au moment de l’exécution, toutefois, ces types d’implémentation sont nécessaires pour exécuter l’application. Ils doivent donc être définis et transmis jusqu’aux interfaces de la couche Noyau de l’application au moyen de l’injection de dépendances.

La figure 5-9 est une représentation plus détaillée de l’architecture d’une application ASP.NET Core conçue selon ces recommandations.

![Architecture ASPNET Core](./media/image5-9.png)

**Figure 5-9**. Diagramme d’une architecture ASP.NET Core propre.

Étant donné que la couche Noyau de l’application ne dépend pas de la couche Infrastructure, il est très facile d’écrire des tests unitaires automatisés pour cette couche. Les figures 5-10 et 5-11 montrent comment les tests s’intègrent à cette architecture.

![UnitTestCore](./media/image5-10.png)

**Figure 5-10.** Tests unitaires, couche Noyau de l’application isolée.

![IntegrationTests](./media/image5-11.png)

**Figure 5-11.** Tests d’intégration, implémentations dans Infrastructure avec des dépendances externes.

Comme la couche Interface utilisateur n’a pas de dépendance directe sur les types définis dans le projet Infrastructure, il est également très facile de permuter les implémentations, pour les besoins de test ou en réponse à des changements dans les exigences de l’application. Grâce à la prise en charge et à l’utilisation intégrée de l’injection de dépendances dans une application ASP.NET Core, cette architecture est la plus performante pour organiser des applications monolithiques non triviales.

Dans les applications monolithiques, les projets Noyau de l’application, Infrastructure et Interface utilisateur sont tous exécutés comme une seule application. La figure 5-12 illustre un exemple d’architecture d’exécution d’une application.

![Architecture ASPNET Core 2](./media/image5-12.png)

**Figure 5-12.** Exemple d’architecture d’exécution d’une application ASP.NET Core.

### <a name="organizing-code-in-clean-architecture"></a>Organisation du code dans une architecture propre

Dans une architecture propre, les responsabilités de chaque projet sont clairement établies. Comme certains types sont communs à chaque projet, vous trouverez souvent plusieurs dossiers correspondant à ces types dans le projet en question.

La couche Noyau de l’application contient le modèle métier, qui définit les entités, les services et les interfaces. Ces interfaces renferment les abstractions des opérations à effectuer dans la couche Infrastructure, comme l’accès aux données, les accès au système de fichiers, les appels réseau, etc. Les services ou interfaces définis dans cette couche doivent parfois interagir avec des types qui ne sont pas des entités et qui n’ont pas de dépendance sur les couches Interface utilisateur ou Infrastructure. Ils peuvent alors être définis comme objets de transfert de données (DTO).

> ### <a name="application-core-types"></a>Types de base dans une application
> -   Entités (classes persistantes du modèle métier)
> -   Interfaces
> -   Services
> -   Objets DTO

Le projet Infrastructure inclut généralement les implémentations de l’accès aux données. Dans une application web ASP.NET Core conventionnelle, ce projet contient la classe DbContext d’Entity Framework, les migrations d’EF Core qui ont été définies, ainsi que les classes d’implémentation de l’accès aux données. La méthode la plus courante pour abstraire le code d’implémentation de l’accès aux données est d’utiliser le [modèle de conception de référentiel](http://deviq.com/repository-pattern/).

En plus des implémentations de l’accès aux données, le projet Infrastructure doit contenir les implémentations des services qui interagissent avec les préoccupations de l’infrastructure. Ces services doivent implémenter les interfaces définies dans la couche Noyau de l’application, et la couche Infrastructure doit donc référencer le projet Noyau de l’application.

> ### <a name="infrastructure-types"></a>Types de la couche Infrastructure
> -   Types EF Core (DbContext, migrations)
> -   Types d’implémentation de l’accès aux données (référentiels)
> -   Services spécifiques de la couche Infrastructure (FileLogger, SmtpNotifier, etc.)

Dans une application ASP.NET Core MVC, la couche Interface utilisateur est le point d’entrée de l’application et constitue un projet ASP.NET Core MVC. Ce projet doit référencer le projet Noyau de l’application, et ses types doivent interagir avec l’infrastructure uniquement par le biais des interfaces définies dans la couche Noyau de l’application. Les instanciations directes des types de la couche Infrastructure (ou les appels statiques à ces types) ne doivent pas être autorisées dans la couche Interface utilisateur.

> ### <a name="ui-layer-types"></a>Types de la couche Interface utilisateur
> -   Contrôleurs
> -   Filtres
> -   Affichages
> -   ViewModels
> -   Démarrage

La classe Démarrage est responsable de la configuration de l’application, mais aussi de la transmission des types d’implémentation jusqu’aux interfaces, pour permettre le fonctionnement correct de l’injection de dépendances au moment de l’exécution.

> [!NOTE]
> Pour configurer l’injection de dépendances dans la section ConfigureServices du fichier Startup.cs associé au projet Interface utilisateur, celui-ci doit référencer le projet Infrastructure. Cette dépendance peut très facilement être supprimée en utilisant un conteneur d’injection de dépendances personnalisé. Dans cet exemple, l’approche la plus simple est d’autoriser le projet Interface utilisateur à référencer le projet Infrastructure.

## <a name="monolithic-applications-and-containers"></a>Conteneurs et applications monolithiques 

Vous pouvez créer une application (ou service) web unique et monolithique, et la déployer en tant que conteneur. En interne, l’application peut ne pas être monolithique, mais être organisée en bibliothèques, composants ou couches. D’un point de vue externe, l’application est considérée comme un conteneur unique, de la même façon qu’un processus, une application web ou un service unique.

Pour gérer ce modèle, vous déployez un seul conteneur pour représenter l’application. Pour effectuer une mise à l’échelle, vous ajoutez simplement des copies supplémentaires avec un équilibreur de charge en frontal. Cette simplicité provient de la gestion d’un seul déploiement dans un seul conteneur ou une seule machine virtuelle.

![](./media/image5-13.png)

Vous pouvez inclure plusieurs couches internes, composants ou bibliothèques dans chaque conteneur, comme illustré à la figure 5-X. Cependant, d’après le principe des conteneurs selon lequel « *un conteneur fait une chose et la fait dans un seul processus* », ce modèle monolithique peut être en conflit.

Cette approche présente des inconvénients si/quand l’application grandit, nécessitant sa mise à l’échelle. Si l’application entière est mise à l’échelle, ce n’est pas vraiment un problème. Toutefois, dans la plupart des cas, la mise à l’échelle est nécessaire pour quelques parties de l’application seulement, mais elle est inutile pour d’autres composants moins utilisés.

Dans l’exemple classique du commerce électronique, c’est probablement le composant des informations produit qui a le plus besoin d’être mis à l’échelle. Les clients qui recherchent des produits sont beaucoup plus nombreux que ceux qui en achètent. Plus de clients utilisent leur panier d’achat que ceux qui utilisent le pipeline de paiement. Moins de clients ajoutent des commentaires ou consultent leur historique d’achat. De même, seule une poignée d’employés, d’une seule région, doivent généralement gérer le contenu et les campagnes marketing. La mise à l’échelle de la conception monolithique déploie tout le code plusieurs fois.

En plus du problème de la mise à l’échelle globale, quand des modifications sont apportées à un seul composant, il faut refaire un test complet de l’application entière et redéployer intégralement toutes les instances.

L’approche architecturale monolithique est fréquemment choisie pour le développement dans les organisations. Beaucoup de ces organisations sont satisfaites des résultats obtenus, mais certaines se heurtent aux limites de ce modèle d’architecture. Les organisations ont souvent conçu leurs applications d’après ce modèle, car les outils et l’infrastructure étaient trop complexes pour concevoir des architectures orientées services (SOA). Par ailleurs, elles ne voyaient pas le besoin de changer de modèle tant que leur application ne grossissait pas trop. Si vous vous heurtez aux limites de l’approche monolithique, la prochaine étape logique pour vous est peut-être de scinder votre application pour mieux tirer parti des conteneurs et microservices.

![](./media/image5-14.png)

Le déploiement d’applications monolithiques dans Microsoft Azure est possible en utilisant des machines virtuelles dédiées pour chaque instance. Avec [Azure VM Scale Sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/), vous pouvez facilement mettre à l’échelle les machines virtuelles. [Azure App Service](https://azure.microsoft.com/services/app-service/) peut également exécuter des applications monolithiques et facilement mettre à l’échelle des instances sans nécessiter une gestion des machines virtuelles. Azure App Service peut également exécuter des instances uniques de conteneurs Docker, ce qui simplifie le déploiement. Avec Docker, vous pouvez déployer une seule machine virtuelle comme hôte Docker et exécuter plusieurs instances. Vous pouvez gérer la mise à l’échelle à l’aide de l’équilibreur de charge Azure, comme indiqué dans la figure 5-14.

Le déploiement sur les différents hôtes peut être géré avec les techniques de déploiement traditionnelles. Les hôtes Docker peuvent être gérés à l’aide de commandes exécutées manuellement, telles que **docker run**, ou de manière automatisée, comme les pipelines de livraison continue.

### <a name="monolithic-application-deployed-as-a-container"></a>Application monolithique déployée comme conteneur

L’utilisation de conteneurs pour gérer les déploiements d’applications monolithiques présente des avantages. La mise à l’échelle des instances des conteneurs est beaucoup plus rapide et facile que le déploiement de machines virtuelles supplémentaires. Même si vous utilisez VM Scale Sets pour mettre à l’échelle des machines virtuelles, leur instanciation prend du temps. Quand une machine virtuelle est déployée en tant qu’instance de l’application, la configuration de l’application est gérée en interne par la machine virtuelle.

Le déploiement de mises à jour comme images Docker est beaucoup plus rapide et efficace du point de vue du réseau. Les images Docker démarrent généralement en quelques secondes, ce qui accélère les lancements. La suppression d’une instance Docker se fait simplement en exécutant une commande **docker stop**. Cette opération prend normalement moins d’une seconde.

Comme les conteneurs sont immuables de par leur conception même, il n’y a pas de risques d’endommagement des machines virtuelles, au contraire des scripts de mise à jour qui peuvent oublier de prendre en compte une configuration ou un fichier spécifique sur le disque.

L’utilisation de Docker peut être utile pour les applications monolithiques, mais le fait de scinder une application monolithique en sous-systèmes qui peuvent être mis à l’échelle, développés et déployés individuellement, peut constituer votre point d’entrée dans le domaine des microservices.

> ### <a name="references--common-web-architectures"></a>Informations de référence sur les architectures web courantes
> - **L’architecture propre**  
> <https://8thlight.com/blog/uncle-bob/2012/08/13/the-clean-architecture.html>
> - **L’architecture en oignon**  
> <http://jeffreypalermo.com/blog/the-onion-architecture-part-1/>
> - **Le modèle référentiel**  
> <http://deviq.com/repository-pattern/>
> - **Exemple d’une solution d’architecture propre**  
> <https://github.com/ardalis/cleanarchitecture>
> - **Architecting Microservices (livre électronique)** <http://aka.ms/MicroservicesEbook>

>[!div class="step-by-step"]
[Previous] (architectural-principles.md) [Next] (common-client-side-web-technologies.md)
