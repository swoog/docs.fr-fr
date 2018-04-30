---
title: Communication directe de client à microservice et modèle de passerelle d’API
description: Architecture de microservices .NET pour les applications .NET en conteneur | Communication directe de client à microservice et modèle de passerelle d’API
keywords: Docker, Microservices, ASP.NET, Conteneur, Passerelle d’API
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: fa3f4bb97cf942ee7698b1efa1dcd09b3f2ca571
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="direct-client-to-microservice-communication-versus-the-api-gateway-pattern"></a>Communication directe de client à microservice et modèle de passerelle d’API

Dans une architecture de microservices, chaque microservice expose un ensemble de points de terminaison (généralement) très ciblés. Ceci peut affecter la communication de client à microservice, comme expliqué dans cette section.

## <a name="direct-client-to-microservice-communication"></a>Communication directe de client à microservice

Une approche possible consiste à utiliser une architecture de communication directe de client à microservice. Dans cette approche, une application cliente peut envoyer des demandes directement à certains des microservices, comme le montre la figure 4-12.

![](./media/image12.png)

**Figure 4-12**. Utilisation d’une architecture de communication directe de client à microservice

Dans cette approche, chaque microservice a un point de terminaison public, parfois avec un port TCP différent pour chaque microservice. Voici un exemple d’URL pour un service particulier dans Azure :

<http://eshoponcontainers.westus.cloudapp.azure.com:88/>

Dans un environnement de production basé sur un cluster, cette URL serait mappée à l’équilibreur de charge utilisé dans le cluster, qui à son tour distribue les demandes entre les microservices. Dans les environnements de production, vous pouvez avoir un contrôleur de livraison d’application comme [Azure Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-introduction) entre vos microservices et Internet. Ceci fonctionne comme un niveau transparent qui non seulement effectue l’équilibrage de charge, mais permet aussi de sécuriser vos services en offrant un processus de terminaison SSL. Ceci allège la charge de vos hôtes en transférant à Azure Application Gateway les processus de terminaison SSL et d’autres tâches de routage qui consomment une grande quantité de ressources de l’UC. Dans tous les cas, un équilibreur de charge et un contrôleur de livraison d’application sont transparents du point de vue de l’architecture logique d’une application.

Une architecture de communication directe de client à microservice peut être suffisante pour une petite application basée sur des microservices, surtout si l’application cliente est une application web côté serveur, comme une application ASP.NET MVC. Cependant, quand vous créez des applications basées sur les microservices de grande taille et complexes (par exemple quand vous gérez des dizaines de types de microservice), et en particulier quand les applications clientes sont des applications mobiles distantes ou des applications web SPA, cette approche doit faire face à quelques problèmes.

Quand vous développez une application de grande taille basée sur les microservices, considérez les questions suivantes :

-   *Comment les applications clientes peuvent-elles minimiser le nombre de demandes envoyées au backend et réduire le volume important des communications avec plusieurs microservices ?*

Interagir avec plusieurs microservices pour créer un seul écran de l’interface utilisateur augmente le nombre d’allers-retours sur Internet. Ceci accroît la latence et la complexité du côté de l’interface utilisateur. Dans l’idéal, les réponses doivent être agrégées de façon efficace côté serveur : ceci réduit la latence, car plusieurs éléments de données reviennent en parallèle et certaines parties de l’interface utilisateur peuvent afficher les données dès qu’elles sont prêtes.

-   *Comment pouvez-vous gérer des problèmes transversaux comme l’autorisation, les transformations de données et la distribution des requêtes dynamiques ?*

L’implémentation de la sécurité et de problèmes transversaux, comme la sécurité et l’autorisation, sur chaque microservice peut nécessiter un travail de développement considérable. Une approche possible consiste à avoir ces services au sein de l’hôte Docker ou du cluster interne, de façon à limiter leur l’accès direct depuis l’extérieur et à implémenter ces problèmes transversaux à un emplacement centralisé, comme une passerelle d’API.

-   *Comment les applications clientes peuvent-elles communiquer avec des services qui utilisent des protocoles non adaptés à Internet ?*

Les protocoles utilisés du côté serveur (par exemple AMQP ou des protocoles binaires) ne sont généralement pas pris en charge dans les applications clientes. Ainsi, les requêtes doivent être exécutées via des protocoles comme HTTP/HTTPS et être traduites après cela pour les autres protocoles. Une approche par *intercepteur* peut aider dans cette situation.

-   *Comment pouvez-vous mettre en forme une façade spécialement conçue pour les applications mobiles ?*

L’API de plusieurs microservices peut ne pas être bien conçue pour les besoins de différentes applications clientes. Par exemple, les besoins d’une application mobile peuvent être différents de ceux d’une application web. Pour les applications mobiles, une optimisation supplémentaire peut être nécessaire pour rendre les réponses des données plus efficaces. Vous pouvez faire cela en agrégeant les données de plusieurs microservices et en retournant un seul jeu de données, et parfois en éliminant de la réponse les données qui ne sont pas nécessaires pour l’application mobile. Bien sûr, vous pouvez aussi compresser les données. Là encore, une façade ou une API entre l’application mobile et les microservices peut être pratique pour ce scénario.

## <a name="using-an-api-gateway"></a>Utilisation d’une passerelle d’API

Quand vous concevez et que vous créez des applications de grande taille ou complexes basées sur des microservices avec plusieurs applications clientes, une [passerelle d’API](https://microservices.io/patterns/apigateway.html) peut être une bonne approche à considérer. Il s’agit d’un service qui fournit un point d’entrée unique pour certains groupes de microservices. Il est similaire au [modèle Façade](https://en.wikipedia.org/wiki/Facade_pattern) de la conception orientée objet, mais dans ce cas, il fait partie d’un système distribué. Le modèle Passerelle d’API est également parfois appelé « backend for frontend » [(BFF)](https://samnewman.io/patterns/architectural/bff/), car vous le créez en pensant aux besoins de l’application cliente.

La figure 4-13 montre comment une passerelle d’API personnalisée peut s’intégrer dans une architecture basée sur les microservices.
Il est important de souligner que dans ce diagramme, vous utilisez un seul service de passerelle d’API personnalisée faisant face à plusieurs applications clientes différentes. Ceci peut présenter un risque important, car votre service de passerelle d’API va croître et évoluer en fonction des nombreuses exigences différentes des applications clientes. Au final, il deviendra trop étendu en raison de ces différents besoins et sera effectivement très similaire à une application monolithique ou à un service monolithique. C’est pourquoi il est vivement recommandé de diviser la passerelle d’API en plusieurs services ou en plusieurs passerelles d’API plus petites, par exemple une par type de facteur de forme.

![](./media/image13.png)

**Figure 4-13**. Utilisation d’une passerelle d’API implémentée comme service d’API web personnalisé

Dans cet exemple, la passerelle d’API doit être implémentée comme un service d’API web personnalisé s’exécutant en tant que conteneur.

Comme cela a été mentionné, vous devez implémenter plusieurs passerelles d’API, afin d’avoir une façade différente pour les besoins de chaque application cliente. Chaque passerelle d’API peut fournir une API différente adaptée à chaque application cliente, voire même en fonction du facteur de forme du client en implémentant le code d’un adaptateur spécifique qui appelle plusieurs microservices internes de façon sous-jacente.

Comme une passerelle d’API personnalisée est généralement un agrégateur de données, vous devez être prudent avec celle-ci. Il n’est en général pas judicieux d’avoir une seule passerelle d’API agrégeant tous les microservices internes de votre application. Dans ce cas, elle se comporte comme un agrégateur ou un orchestrateur monolithique, et contrevient au principe d’autonomie des microservices en couplant tous les microservices. Par conséquent, les passerelles d’API doivent être séparées en fonction des limites métier et ne pas agir comme un agrégateur pour toute l’application.

Parfois, une passerelle d’API granulaire peut également être un microservice par elle-même, et même avoir un nom de domaine ou un nom métier, ainsi que les données qui s’y rapportent. Le fait que les limites de la passerelle d’API soient dictées par le métier ou le domaine vous aide à obtenir une meilleure conception.

Une granularité au niveau de la passerelle d’API peut être particulièrement utile pour les applications avec des interfaces utilisateur composites plus avancées basées sur des microservices, car le concept d’une passerelle d’API très ciblée est similaire à un service de composition d’interface utilisateur. Nous abordons cela plus loin dans la section [Création d’une interface utilisateur composite basée sur des microservices](#creating-composite-ui-based-on-microservices-including-visual-ui-shape-and-layout-generated-by-multiple-microservices).

Ainsi, pour de nombreuses applications de moyenne et de grande taille, l’utilisation d’une passerelle d’API personnalisée est généralement une bonne approche, mais pas comme agrégateur monolithique ni comme passerelle d’API centrale personnalisée unique.

Une autre approche consiste à utiliser un produit comme [Gestion des API Azure](https://azure.microsoft.com/services/api-management/), comme le montre la figure 4-14. Cette approche non seulement solutionne les besoins de votre passerelle d’API, mais fournit aussi des fonctionnalités comme la collecte d’informations auprès de vos API. Si vous utilisez une solution de gestion des API, une passerelle d’API est seulement un composant au sein de cette solution globale de gestion des API.

![](./media/image14.png)

**Figure 4-14**. Utilisation de Gestion des API Azure pour votre passerelle d’API

Dans ce cas, lors l’utilisation d’un produit comme Gestion des API Azure, le fait d’avoir une seule passerelle d’API n’est pas si risqué, car ces types de passerelles d’API sont « plus fins », ce qui veut dire que vous n’implémentez pas de code C# personnalisé susceptible d’évoluer vers un composant monolithique. 

Ce type de produit agit plus comme un proxy inverse pour la communication en entrée, où vous pouvez aussi filtrer les API des microservices internes et appliquer une autorisation aux API publiées dans ce niveau unique.

Les informations disponibles provenant d’un système de gestion des API vous aident à comprendre comment vos API sont utilisées et comment elles fonctionnent. Ils font cela en vous permettant de voir des rapports d’analyse quasi en temps réel et en identifiant les tendances qui peuvent avoir un impact sur votre activité. De plus, vous pouvez avoir des journaux sur l’activité des demandes et des réponses, que vous pouvez alors analyser de façon plus approfondie en ligne et hors connexion.

Avec Gestion des API Azure, vous pouvez sécuriser vos API avec une clé, un jeton et un filtrage des adresses IP. Ces fonctionnalités vous permettent d’appliquer des quotas et des limites de débit de façon souple et précise, de modifier la forme et le comportement de vos API avec des stratégies, et d’améliorer les performances avec la mise en cache des réponses.

Dans ce guide et dans l’exemple d’application de référence (eShopOnContainers), nous limitons l’architecture à une architecture en conteneurs plus simple et personnalisée, de façon à mettre l’accent sur des conteneurs ordinaires sans utiliser de produits PaaS comme Gestion des API Azure. Cependant, pour les applications de grande taille basées sur des microservices qui sont déployées sur Microsoft Azure, nous vous encourageons à examiner et à adopter Gestion des API Azure comme base pour vos passerelles d’API.

## <a name="drawbacks-of-the-api-gateway-pattern"></a>Inconvénients du modèle Passerelle d’API

-   L’inconvénient plus important est que, quand vous implémentez une passerelle d’API, vous couplez ce niveau avec les microservices internes. Un tel couplage peut introduire de graves difficultés pour votre application. Clemens Vaster, architecte de l’équipe Azure Service Bus, parle de cette difficulté potentielle comme de « la nouvelle ESB » dans sa session « [Messaging and Microservices](https://www.youtube.com/watch?v=rXi5CLjIQ9k) » à GOTO 2016.

-   L’utilisation d’une passerelle d’API de microservices crée un possible point de défaillance unique supplémentaire.

-   Une passerelle d’API peut introduire des temps de réponse accrus en raison de l’appel réseau supplémentaire. Cependant, cet appel supplémentaire a généralement moins d’impact qu’un client de l’interface qui émet trop de communications en appelant directement les microservices internes.

-   Si elle n’est pas montée pas en charge correctement, la passerelle d’API peut devenir un goulot d’étranglement.

-   Une passerelle d’API nécessite des coûts de développement supplémentaires et une maintenance ultérieure si elle inclut une logique personnalisée et effectue une agrégation des données. Les développeurs doivent mettre à jour la passerelle d’API pour pouvoir exposer les points de terminaison de chaque microservice. En outre, les changements d’implémentation dans les microservices internes peuvent entraîner des modifications du code au niveau de la passerelle d’API. Cependant, si la passerelle d’API applique simplement la sécurité, la journalisation et la gestion des versions (comme quand vous utilisez Gestion des API Azure), ces coûts de développement supplémentaires peuvent ne pas s’appliquer.

-   Si la passerelle d’API est développée par une même équipe, il peut y avoir un goulot d’étranglement en matière de développement. Ceci est une autre raison pour laquelle il est préférable d’avoir plusieurs passerelles d’API plus ciblées qui répondent aux besoins des différents clients. Vous pouvez aussi diviser la passerelle d’API en interne en plusieurs parties ou couches, affectées chacune aux différentes équipes travaillant sur les microservices internes.

## <a name="additional-resources"></a>Ressources supplémentaires

-   **Charles Richardson. Modèle : Passerelle /backend d’API pour serveur frontal**
    [*https://microservices.io/patterns/apigateway.html*](https://microservices.io/patterns/apigateway.html)

-   **Gestion des API Azure**
    [*https://azure.microsoft.com/services/api-management/*](https://azure.microsoft.com/services/api-management/)

-   **Udi Dahan. Service Oriented Composition**\
    [*http://udidahan.com/2014/07/30/service-oriented-composition-with-video/*](http://udidahan.com/2014/07/30/service-oriented-composition-with-video/)

-   **Clemens Vasters. Messaging and Microservices at GOTO 2016** (vidéo) [*https://www.youtube.com/watch?v=rXi5CLjIQ9k*](https://www.youtube.com/watch?v=rXi5CLjIQ9k)


>[!div class="step-by-step"]
[Précédent] (identify-microservice-domain-model-boundaries.md) [Suivant] (communication-in-microservice-architecture.md)
