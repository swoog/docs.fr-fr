---
title: Application de modèles CQRS et DDD simplifiés dans un microservice
description: Architecture des microservices .NET pour les applications .NET en conteneur | Application de modèles CQRS et DDD simplifiés dans un microservice
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 4e30b4755af001f85649e611c9f1f976ed294cab
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="applying-simplified-cqrs-and-ddd-patterns-in-a-microservice"></a>Application de modèles CQRS et DDD simplifiés dans un microservice

CQRS est un modèle d’architecture qui sépare les modèles pour la lecture et l’écriture de données. Le terme connexe [CQS (séparation des commandes et des requêtes)](https://martinfowler.com/bliki/CommandQuerySeparation.html) a été initialement défini par Bertrand Meyer dans son livre *Object-Oriented Software Construction*. L’idée de base est que vous pouvez diviser les opérations d’un système en deux catégories nettement séparées :

-   Requêtes. Elles retournent un résultat, ne modifient pas l’état du système et ne présentent aucun effet secondaire.

-   Commandes. Elles modifient l’état d’un système.

CQS est un concept simple : il s’agit de méthodes du même objet qui sont soit des requêtes, soit des commandes. Chaque méthode retourne l’état ou transforme l’état, mais pas les deux. Même un seul objet de modèle de dépôt peut se conformer à CQS. L’approche CQS peut être considérée comme un principe fondamental de CQRS.

L’approche [CQRS (séparation des responsabilités dans les commandes et les requêtes)](https://martinfowler.com/bliki/CQRS.html), introduite par Greg Young, a été vivement plébiscitée par Udi Dahan et d’autres. Elle est basée sur le principe CQS, même si elle est plus détaillée. Elle peut être considérée comme un modèle basé sur les commandes et les événements, et éventuellement sur les messages asynchrones. Dans de nombreux cas, CQRS est lié à des scénarios plus avancés, comme disposer d’une base de données physique différente pour les lectures (requêtes) et pour les écritures (mises à jour). De plus, un système CQRS plus évolué peut implémenter la fonctionnalité d’[Event Sourcing ](http://codebetter.com/gregyoung/2010/02/20/why-use-event-sourcing/) (approvisionnement d’événements) pour votre base de données de mises à jour, de sorte que vous ne stockez que les événements du modèle de domaine au lieu de stocker les données d’état actuel. Toutefois, ce n’est pas l’approche utilisée dans ce guide. Nous utilisons l’approche CQRS la plus simple, qui consiste uniquement à séparer les requêtes des commandes.

L’aspect de séparation de CQRS est obtenu en regroupant les opérations de requête dans une couche et les commandes dans une autre couche. Chaque couche a son propre modèle de données (notez que nous disons « modèle », pas nécessairement une base de données différente) et est construite à l’aide de sa propre combinaison de modèles et de technologies. Plus important encore, les deux couches peuvent se trouver dans le même niveau ou microservice, comme dans l’exemple (microservice de commandes) utilisé dans ce guide. Elles peuvent également être implémentées sur des microservices ou processus différents afin de pouvoir être optimisées et adaptées séparément sans s’affecter mutuellement.

CQRS implique d’avoir deux objets pour une opération de lecture/écriture où, dans d’autres contextes, il y en a un. Il existe des raisons d’avoir une base de données de lectures dénormalisée, sur laquelle vous pouvez obtenir des informations dans une documentation CQRS plus avancée. Mais nous n’utilisons pas cette approche ici, où l’objectif est d’avoir plus de souplesse dans les requêtes, et non pas de limiter les requêtes avec des contraintes à partir de modèles DDD comme les agrégats.

Il peut s’agir, par exemple, du microservice de commandes de l’application de référence eShopOnContainers. Ce service implémente un microservice basé sur une approche CQRS simplifiée. Il utilise une seule source de données ou base de données, mais deux modèles logiques plus des modèles DDD pour le domaine transactionnel, comme illustré dans la figure 9-2.

![](./media/image2.png)

**Figure 9-2**. Microservice basé sur les modèles CQRS et DDD simplifiés

La couche Application peut être l’API web elle-même. Ici, l’aspect important de la conception est que le microservice a séparé les requêtes et les ViewModels (modèles de données spécialement créés pour les applications clientes) des commandes, du modèle de domaine et des transactions suivant le modèle CQRS. Avec cette approche, les requêtes restent indépendantes des restrictions et des contraintes provenant de modèles DDD qui conviennent uniquement pour les transactions et les mises à jour, comme expliqué dans des sections ultérieures.


>[!div class="step-by-step"]
[Précédent] (index.md) [Suivant] (eshoponcontainers-cqrs-ddd-microservice.md)
