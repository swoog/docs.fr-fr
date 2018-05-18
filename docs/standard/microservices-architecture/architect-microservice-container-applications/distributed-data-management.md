---
title: Problématiques et solutions pour la gestion des données distribuées
description: Architecture de microservices .NET pour les applications .NET en conteneur | Problématiques et solutions pour la gestion des données distribuées
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 7d173133ab7c803c7ab48b39c50b02ee4f3b1721
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="challenges-and-solutions-for-distributed-data-management"></a>Problématiques et solutions pour la gestion des données distribuées

## <a name="challenge-1-how-to-define-the-boundaries-of-each-microservice"></a>Problématique \#1 : Comment définir les limites de chaque microservice

Définir les limites d’un microservice est sans doute la première problématique à laquelle tout le monde est confronté. Chaque microservice doit être un composant de votre application et chaque microservice doit être autonome, avec tous les avantages et les défis induits. Mais comment identifier ces limites ?

Vous devez d’abord vous concentrer sur les modèles de domaine logique de l’application et ses données associées. Vous devez essayer d’identifier les éléments isolés découplés dans les données et les différents contextes au sein de la même application. Chaque contexte peut avoir un langage métier différent (des termes métier différents). Les contextes doivent être définis et gérés indépendamment. Les termes et les entités utilisés dans ces différents contextes peuvent sembler similaires, mais vous pouvez découvrir que dans un contexte spécifique, un concept métier d’un contexte est utilisé à des fins différentes dans un autre contexte, et qu’il peut même porter un autre nom. Par exemple, un utilisateur peut s’appeler un utilisateur dans un contexte d’identité ou d’appartenance, un client dans un contexte de gestion de la relation clientèle, un acheteur dans un contexte de prise de commande, etc.

La façon dont vous identifiez les limites entre plusieurs contextes d’application avec un domaine différent pour chaque contexte correspond exactement à la façon dont vous pouvez identifier les limites pour chaque microservice métier, et son modèle de domaine et ses données associés. Vous essayez toujours de minimiser le couplage entre ces microservices. Ce guide présente plus en détails cette identification et cette conception du modèle de domaine plus loin dans la section [Identification des limites du modèle de domaine pour chaque microservice](#identifying-domain-model-boundaries-for-each-microservice).

## <a name="challenge-2-how-to-create-queries-that-retrieve-data-from-several-microservices"></a>Problématique \#2 : Comment créer des requêtes qui extraient des données de plusieurs microservices

Une deuxième problématique est la façon d’implémenter des requêtes qui extraient des données de plusieurs microservices, tout en évitant des communication intensives entre les microservices et les applications clientes distantes. Un exemple est un écran d’une application mobile qui a besoin d’afficher les informations d’un utilisateur qui sont détenues par des microservices distincts gérant respectivement le panier d’achat, le catalogue et l’identité des utilisateurs. Un autre exemple est un rapport complexe impliquant plusieurs tables qui se trouvent dans plusieurs microservices. La bonne solution dépend de la complexité des requêtes. Dans tous les cas cependant, il vous faut un moyen d’agréger les informations si vous voulez améliorer l’efficacité des communications dans votre système. Les solutions les plus répandues sont les suivantes :

**Passerelle d’API**. Pour une agrégation de données simples provenant de plusieurs microservices qui ont des bases de données différentes, l’approche recommandée est un microservice d’agrégation, connu sous le nom de passerelle d’API. Vous devez cependant être prudent dans l’implémentation de ce modèle, car il peut être un goulot d’étranglement dans votre système, et il peut violer le principe d’autonomie des microservices. Pour limiter cette possibilité, vous pouvez avoir plusieurs passerelles d’API réduites, chacune étant consacrée à une « tranche » verticale ou un secteur métier du système. Le modèle de passerelle d’API est expliqué plus en détails plus loin dans la section Utilisation d’une passerelle d’API.

**CQRS (Command Query Responsibility Segregation) avec des tables de requête/lectures**. Une autre solution pour agréger des données provenant de plusieurs microservices est le [modèle de vue matérialisée](https://docs.microsoft.com/azure/architecture/patterns/materialized-view). Dans cette approche, vous générez à l’avance (vous préparez des données dénormalisées avant que les requêtes réelles ne soient effectuées) une table en lecture seule avec les données détenues par plusieurs microservices. La table a un format adapté aux besoins de l’application cliente.

Considérons par exemple l’écran d’une application mobile. Si vous avez une seule base de données, vous pouvez extraire en une seule fois les données pour cet écran en utilisant une requête SQL qui effectue une jointure complexe impliquant plusieurs tables. Cependant, quand vous avez plusieurs bases de données et que chaque base de données est détenue par un microservice différent, vous ne pouvez pas interroger ces bases de données et créer une jointure SQL. Votre requête complexe devient un vrai défi. Vous pouvez traiter ce problème en utilisant une approche CQRS : vous créez une table dénormalisée dans une autre base de données, utilisée seulement pour les requêtes. La table peut être conçue spécifiquement pour les données dont vous avez besoin pour la requête complexe, avec une relation un à un entre les champs nécessaires à l’écran de votre application et les colonnes dans la table de requête. Elle peut également servir pour la création de rapports.

Cette approche résout non seulement le problème d’origine (comment faire des requêtes et des jointures entre des microservices), mais elle améliore également considérablement les performances en comparaison d’une jointure complexe, car vous avez déjà les données nécessaires à l’application dans la table de requête. Bien sûr, l’utilisation de CQRS (Command and Query Responsibility Segregation) avec des tables de requête/lectures signifie davantage de travail de développement et l’application d’une cohérence à terme. Néanmoins, des exigences en matière de performances et de haute scalabilité dans des [scénarios collaboratifs](http://udidahan.com/2011/10/02/why-you-should-be-using-cqrs-almost-everywhere/) (ou des scénarios de concurrence, selon le point de vue) doivent vous inciter à appliquer CQRS avec plusieurs bases de données.

**« Données froides » dans des bases de données centrales**. Pour des rapports et des requêtes complexes ne nécessitant pas de données en temps réel, une approche courante consiste à exporter vos « données chaudes » (les données transactionnelles des microservices) en tant que « données froides » dans des bases de données volumineuses qui sont utilisées seulement pour les rapports. Ce système de base de données centrale peut être un système basé sur le Big Data, comme Hadoop, un entrepôt de données par exemple basé sur Azure SQL Data Warehouse, ou même une base de données SQL utilisée seulement pour les rapports (si la taille n’est pas un problème).

Gardez à l’esprit que cette base de données centralisée doit être utilisée seulement pour les requêtes et les rapports qui n’ont pas besoin de données en temps réel. Les mises à jour et les transactions d’origine, qui constituent votre source de référence, doivent être effectuées dans les données de vos microservices. Vous allez synchroniser les données via une communication pilotée par les événements (traitée dans les sections suivantes) ou via d’autres outils d’importation/exportation de l’infrastructure de base de données. Si vous utilisez une communication pilotée par les événements, ce processus d’intégration est similaire à la façon dont vous propagez les données comme cela a été décrit précédemment pour les tables de requête CQRS.

Cependant, si la conception de votre application implique d’agréger constamment les informations provenant de plusieurs microservices pour des requêtes complexes, cela peut être le symptôme d’une conception incorrecte : un microservice doit être aussi isolé que possible des autres microservices. (Ceci exclut les rapports/analyses qui doivent toujours utiliser des bases de données centrales contenant des données froides.) Le fait que ce problème se pose souvent peut être une raison pour fusionner des microservices. Vous devez équilibrer l’autonomie de l’évolution et du déploiement de chaque microservice avec des dépendances fortes, la cohésion et l’agrégation des données.

## <a name="challenge-3-how-to-achieve-consistency-across-multiple-microservices"></a>Problématique \#3 : Comment garantir la cohérence entre plusieurs microservices

Comme indiqué précédemment, les données détenues par chaque microservice sont privées pour ce microservice et sont accessibles seulement via son API de microservice. Ainsi, le problème est de savoir comment implémenter des processus métier de bout en bout tout en conservant la cohérence entre plusieurs microservices.

Pour analyser ce problème, considérons un exemple de [l’application de référence eShopOnContainers](http://aka.ms/eshoponcontainers). Le microservice Catalog (Catalogue) gère les informations sur tous les produits, notamment leur niveau de stock. Le microservice Ordering gère les commandes et doit vérifier qu’une nouvelle commande n’excède pas le stock disponible du produit dans le catalogue. (Le scénario peut impliquer une logique qui gère les produits en cours d’approvisionnement.) Dans une hypothétique version monolithique de cette application, le sous-système de commande pourrait simplement utiliser une transaction ACID pour vérifier le stock disponible, créer la commande dans la table Orders (Commandes) et mettre à jour le stock disponible dans la table Products (Produits).

Cependant, dans une application basée sur des microservices, les tables Order et Product appartiennent à leurs microservices respectifs. Aucun microservice ne doit jamais inclure des bases de données appartenant à un autre microservice dans ses propres transactions ou ses requêtes, comme le montre la figure 4-9.

![](./media/image9.PNG)

**Figure 4-9**. Un microservice ne peut pas accéder directement à une table dans un autre microservice

Le microservice Ordering ne doit pas mettre à jour directement la table Products, car celle-ci est détenue par le microservice Catalog. Pour effectuer une mise à jour au niveau du microservice Catalog, le microservice Ordering doit toujours utiliser des communications asynchrones, comme des événements d’intégration (communication basée sur des messages et des événements). Voici comment l’application de référence [eShopOnContainers](http://aka.ms/eshoponcontainers) effectue ce type de mise à jour.

Comme le montre le [théorème CAP](https://en.wikipedia.org/wiki/CAP_theorem), vous devez choisir entre la disponibilité et la cohérence forte d’ACID. La plupart des scénarios basés sur des microservices demandent la disponibilité et une haute scalabilité, plutôt qu’une cohérence forte. Les applications critiques doivent rester opérationnelles, et les développeurs peuvent contourner les problèmes liés à la cohérence forte en utilisant des techniques permettant de travailler avec une cohérence faible ou à terme. Il s’agit de l’approche adoptée par la plupart des architectures basée sur les microservices.

En outre, les transactions de style ACID ou avec validation en deux phases ne sont pas seulement en opposition avec les principes des microservices : la plupart des bases de données NoSQL (comme Azure Cosmos DB, MongoDB, etc.) ne prennent pas en charge les transactions avec validation en deux phases. Cependant, conserver la cohérence des données entre les services et les bases de données est fondamental. Cette problématique concerne aussi la façon de propager les modifications entre plusieurs microservices quand certaines données doivent être redondantes, par exemple quand vous devez avoir le nom ou la description du produit dans le microservice Catalog et dans le microservice Basket.

Une bonne solution pour résoudre ce problème est d’utiliser la cohérence à terme entre les microservices, articulée autour d’une communication pilotée par les événements et d’un système de publication-abonnement. Ces rubriques sont traitées dans la section [Communication asynchrone pilotée par les événements](#async_event_driven_communication) plus loin dans ce guide.

## <a name="challenge-4-how-to-design-communication-across-microservice-boundaries"></a>Problématique \#4 : Comment concevoir la communication entre les limites des microservices

La communication entre les limites des microservices est une vraie problématique. Dans ce contexte, la communication ne concerne pas le protocole que vous devez utiliser (HTTP et REST, AMQP, messagerie, etc.). Au lieu de cela, elle concerne le style de communication que vous devez utiliser, et en particulier comment vos microservices doivent être couplés. Selon le niveau de couplage, l’impact d’une défaillance sur votre système varie considérablement.

Dans un système distribué comme une application basée sur des microservices, avec un si grand nombre d’artefacts concernés et avec des services distribués sur plusieurs serveurs ou plusieurs hôtes, certains composants finissent à leur tour par connaître une défaillance. Une défaillance partielle ou même des indisponibilités plus importantes se produisent alors : vous devez donc concevoir vos microservices et la communication entre ceux-ci en prenant en compte les risques courants dans ce type de système distribué.

Une approche courante consiste à implémenter des microservices basés sur HTTP (REST), en raison de leur simplicité. Une approche basée sur HTTP est parfaitement acceptable ; le problème est ici la façon dont vous l’utilisez. Si vous utilisez des requêtes et des réponses HTTP simplement pour interagir avec vos microservices à partir d’applications clientes ou de passerelles d’API, cela convient. Mais si vous créez de longues chaînes d’appels HTTP synchrones entre des microservices, en communiquant entre leurs limites comme si les microservices étaient des objets dans une application monolithique, votre application finira par rencontrer des problèmes.

Par exemple, supposons que votre application cliente effectue un appel d’API HTTP à un microservice individuel, comme le microservice Ordering. Si le microservice Ordering appelle à son tour d’autres microservices en utilisant HTTP au sein du même cycle de demande/réponse, vous créez une chaîne d’appels HTTP. Cela peut initialement sembler raisonnable. Des points importants sont cependant à prendre en compte si vous suivez cette voie :

-   Blocage et faibles performances. En raison de la nature synchrone de HTTP, la requête d’origine n’obtiendra pas de réponse tant que tous les appels HTTP internes ne sont pas terminés. Imaginez dès lors que le nombre de ces appels augmente considérablement et qu’en même temps, un des appels HTTP intermédiaires à un microservice soit bloqué. Le résultat est que les performances sont impactées et que la scalabilité globale est affectée de façon exponentielle avec l’augmentation du nombre de requêtes HTTP.

-   Couplage des microservices avec HTTP. Un microservice métier ne doit pas être couplé avec d’autres microservices métier. Dans l’idéal, ils ne doivent rien « connaître » de l’existence d’autres microservices. Si votre application s’appuie sur le couplage de microservices comme dans l’exemple, parvenir à une autonomie des microservices est pratiquement impossible.

-   Défaillance dans un des microservices. Si vous avez implémenté une chaîne de microservices liés par des appels HTTP, quand un des microservices connaît une défaillance (et ce sera le cas pour tous au final), la chaîne entière des microservices échoue. Un système basé sur des microservices doit être conçu pour continuer à fonctionner aussi bien que possible en cas de défaillances partielles. Même si vous implémentez une logique de client qui utilise des nouvelles tentatives avec des mécanismes d’interruption exponentielle ou de disjoncteur, plus les chaînes d’appels HTTP sont complexes, plus l’implémentation d’une stratégie de défaillance basée sur HTTP est complexe.

En fait, si vos microservices internes communiquent en créant des chaînes de requêtes HTTP comme nous l’avons décrit, il peut se dire que vous avez une application monolithique, mais une application basée sur HTTP entre les processus et non pas sur des mécanismes de communication intraprocessus.

Par conséquent, pour atteindre à l’autonomie des microservices et avoir une meilleure résilience, vous devez minimiser l’utilisation de chaînes de communication de demande/réponse entre les microservices. Il est recommandé d’utiliser seulement une interaction asynchrone pour la communication entre les microservices, via une communication asynchrone basée sur des messages et des événements, ou via des interrogations HTTP indépendantes du cycle de demande/réponse HTTP d’origine.

L’utilisation d’une communication asynchrone est expliquée plus en détails plus loin dans ce guide, dans les sections [L’intégration de microservices asynchrones permet d’atteindre l’autonomie des microservices](#asynchronous-microservice-integration-enforce-microservices-autonomy) et [Communication asynchrone basée sur des messages](#asynchronous-message-based-communication).

## <a name="additional-resources"></a>Ressources supplémentaires

-   **CAP theorem**
    [*https://en.wikipedia.org/wiki/CAP\_theorem*](https://en.wikipedia.org/wiki/CAP_theorem)

-   **Eventual consistency**
    [*https://en.wikipedia.org/wiki/Eventual\_consistency*](https://en.wikipedia.org/wiki/Eventual_consistency)

-   **Data Consistency Primer**
    [*https://msdn.microsoft.com/library/dn589800.aspx*](https://msdn.microsoft.com/library/dn589800.aspx)

-   **Martin Fowler. CQRS (Command and Query Responsibility Segregation)**
    [*https://martinfowler.com/bliki/CQRS.html*](https://martinfowler.com/bliki/CQRS.html)

-   **Vue matérialisée**
    [*https://docs.microsoft.com/azure/architecture/patterns/materialized-view*](https://docs.microsoft.com/azure/architecture/patterns/materialized-view)

-   **Charles Row. ACID vs. BASE: The Shifting pH of Database Transaction Processing**
    [*http://www.dataversity.net/acid-vs-base-the-shifting-ph-of-database-transaction-processing/*](http://www.dataversity.net/acid-vs-base-the-shifting-ph-of-database-transaction-processing/)

-   **Transaction de compensation**
    [*https://docs.microsoft.com/azure/architecture/patterns/compensating-transaction*](https://docs.microsoft.com/azure/architecture/patterns/compensating-transaction)

-   **Udi Dahan. Service Oriented Composition**
    [*http://udidahan.com/2014/07/30/service-oriented-composition-with-video/*](http://udidahan.com/2014/07/30/service-oriented-composition-with-video/)


>[!div class="step-by-step"]
[Précédent] (logical-versus-physical-architecture.md) [Suivant] (identify-microservice-domain-model-boundaries.md)
