---
title: Conception de la couche Application de microservices et de l’API web
description: Architecture des microservices .NET pour les applications .NET en conteneur | Conception de la couche Application de microservices et de l’API web
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 12/12/2017
ms.openlocfilehash: 77e0556e4b6d9a22cf76a79ec86d744d9009a39f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="designing-the-microservice-application-layer-and-web-api"></a>Conception de la couche Application de microservices et de l’API web

## <a name="using-solid-principles-and-dependency-injection"></a>Utilisation des principes SOLID et de l’injection de dépendances

Les principes SOLID sont des techniques essentielles à utiliser dans les applications modernes et stratégiques, notamment dans le développement d’un microservice avec des modèles DDD. SOLID est un acronyme qui regroupe cinq principes fondamentaux :

-   Principe de responsabilité unique (Single responsibility)

-   Principe ouvert/fermé (Open/closed)

-   Principe de substitution de Liskov (Liskov substitution)

-   Principe de ségrégation des interfaces (Interface segregation)

-   Principe d’inversion de dépendances (Dependency inversion)

SOLID a plus trait à la façon dont vous concevez votre application ou vos couches internes de microservices et au découplage des dépendances entre elles. Ce principe n’est pas lié au domaine, mais à la conception technique de l’application. Le dernier principe, celui de l’inversion de dépendances, vous permet de découpler la couche d’infrastructure du reste des couches, ce qui permet une implémentation mieux découplée des couches DDD.

L’inversion de dépendances est une façon d’implémenter le principe éponyme. Il s’agit d’une technique de couplage faible entre des objets et leurs dépendances. Au lieu d’instancier directement des collaborateurs ou d’utiliser des références statiques, les objets dont a besoin une classe pour effectuer ses opérations sont fournis à la classe (ou injectés dans la classe). Le plus souvent, les classes déclarent leurs dépendances par le biais de leur constructeur, ce qui leur permet de suivre le principe des dépendances explicites. L’inversion de dépendances se base généralement sur des conteneurs d’inversion de contrôle (IoC) spécifiques. ASP.NET Core fournit un simple conteneur IoC intégré, mais vous pouvez également utiliser votre conteneur IoC favori, comme Autofac ou Ninject.

En suivant les principes SOLID, vos classes ont naturellement tendance à être petites, bien factorisées et facilement testées. Mais comment savoir si trop de dépendances sont injectées dans vos classes ? Si vous utilisez l’inversion de dépendances par le biais du constructeur, vous pouvez facilement le détecter rien qu’en examinant le nombre de paramètres pour votre constructeur. S’il y a trop de dépendances, c’est généralement le signe (un [code smell](http://deviq.com/code-smells/)) que votre classe essaie d’en faire trop et qu’elle enfreint probablement le principe de responsabilité unique.

Un autre guide serait nécessaire pour couvrir les principes SOLID de façon approfondie. C’est pourquoi le présent guide exige que vous ayez un minimum de connaissances à ce sujet.

#### <a name="additional-resources"></a>Ressources supplémentaires

-   **SOLID: Fundamental OOP Principles**
    [*http://deviq.com/solid/*](http://deviq.com/solid/%20)

-   **Inversion of Control Containers and the Dependency Injection pattern**
    [*https://martinfowler.com/articles/injection.html*](https://martinfowler.com/articles/injection.html)

-   **Steve Smith. New is Glue**
    [*https://ardalis.com/new-is-glue*](https://ardalis.com/new-is-glue)


>[!div class="step-by-step"]
[Précédent] (nosql-database-persistence-infrastructure.md) [Suivant] (microservice-application-layer-implementation-web-api.md)
