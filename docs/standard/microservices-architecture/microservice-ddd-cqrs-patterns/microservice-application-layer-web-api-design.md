---
title: Conception de la couche Application de microservices et de l’API web
description: Architecture des microservices .NET pour les applications .NET en conteneur | Conception de la couche Application de microservices et de l’API web
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 12/12/2017
ms.openlocfilehash: e5c7e0acb0496aebce4d9cbe8cb51ced0c7166a2
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37106604"
---
# <a name="designing-the-microservice-application-layer-and-web-api"></a><span data-ttu-id="f4206-103">Conception de la couche Application de microservices et de l’API web</span><span class="sxs-lookup"><span data-stu-id="f4206-103">Designing the microservice application layer and Web API</span></span>

## <a name="using-solid-principles-and-dependency-injection"></a><span data-ttu-id="f4206-104">Utilisation des principes SOLID et de l’injection de dépendances</span><span class="sxs-lookup"><span data-stu-id="f4206-104">Using SOLID principles and Dependency Injection</span></span>

<span data-ttu-id="f4206-105">Les principes SOLID sont des techniques essentielles à utiliser dans les applications modernes et stratégiques, notamment dans le développement d’un microservice avec des modèles DDD.</span><span class="sxs-lookup"><span data-stu-id="f4206-105">SOLID principles are critical techniques to be used in any modern and mission-critical application, such as developing a microservice with DDD patterns.</span></span> <span data-ttu-id="f4206-106">SOLID est un acronyme qui regroupe cinq principes fondamentaux :</span><span class="sxs-lookup"><span data-stu-id="f4206-106">SOLID is an acronym that groups five fundamental principles:</span></span>

-   <span data-ttu-id="f4206-107">Principe de responsabilité unique (Single responsibility)</span><span class="sxs-lookup"><span data-stu-id="f4206-107">Single Responsibility principle</span></span>

-   <span data-ttu-id="f4206-108">Principe ouvert/fermé (Open/closed)</span><span class="sxs-lookup"><span data-stu-id="f4206-108">Open/closed principle</span></span>

-   <span data-ttu-id="f4206-109">Principe de substitution de Liskov (Liskov substitution)</span><span class="sxs-lookup"><span data-stu-id="f4206-109">Liskov substitution principle</span></span>

-   <span data-ttu-id="f4206-110">Principe de ségrégation des interfaces (Interface segregation)</span><span class="sxs-lookup"><span data-stu-id="f4206-110">Interface Segregation principle</span></span>

-   <span data-ttu-id="f4206-111">Principe d’inversion de dépendances (Dependency inversion)</span><span class="sxs-lookup"><span data-stu-id="f4206-111">Dependency Inversion principle</span></span>

<span data-ttu-id="f4206-112">SOLID a plus trait à la façon dont vous concevez votre application ou vos couches internes de microservices et au découplage des dépendances entre elles.</span><span class="sxs-lookup"><span data-stu-id="f4206-112">SOLID is more about how you design your application or microservice internal layers and about decoupling dependencies between them.</span></span> <span data-ttu-id="f4206-113">Ce principe n’est pas lié au domaine, mais à la conception technique de l’application.</span><span class="sxs-lookup"><span data-stu-id="f4206-113">It is not related to the domain, but to the application’s technical design.</span></span> <span data-ttu-id="f4206-114">Le dernier principe, celui de l’inversion de dépendances, vous permet de découpler la couche d’infrastructure du reste des couches, ce qui permet une implémentation mieux découplée des couches DDD.</span><span class="sxs-lookup"><span data-stu-id="f4206-114">The final principle, the Dependency Inversion (DI) principle, allows you to decouple the infrastructure layer from the rest of the layers, which allows a better decoupled implementation of the DDD layers.</span></span>

<span data-ttu-id="f4206-115">L’inversion de dépendances est une façon d’implémenter le principe éponyme.</span><span class="sxs-lookup"><span data-stu-id="f4206-115">DI is one way to implement the Dependency Inversion principle.</span></span> <span data-ttu-id="f4206-116">Il s’agit d’une technique de couplage faible entre des objets et leurs dépendances.</span><span class="sxs-lookup"><span data-stu-id="f4206-116">It is a technique for achieving loose coupling between objects and their dependencies.</span></span> <span data-ttu-id="f4206-117">Au lieu d’instancier directement des collaborateurs ou d’utiliser des références statiques, les objets dont a besoin une classe pour effectuer ses opérations sont fournis à la classe (ou injectés dans la classe).</span><span class="sxs-lookup"><span data-stu-id="f4206-117">Rather than directly instantiating collaborators, or using static references, the objects that a class needs in order to perform its actions are provided to (or "injected into") the class.</span></span> <span data-ttu-id="f4206-118">Le plus souvent, les classes déclarent leurs dépendances par le biais de leur constructeur, ce qui leur permet de suivre le principe des dépendances explicites.</span><span class="sxs-lookup"><span data-stu-id="f4206-118">Most often, classes will declare their dependencies via their constructor, allowing them to follow the Explicit Dependencies principle.</span></span> <span data-ttu-id="f4206-119">L’inversion de dépendances se base généralement sur des conteneurs d’inversion de contrôle (IoC) spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f4206-119">DI is usually based on specific Inversion of Control (IoC) containers.</span></span> <span data-ttu-id="f4206-120">ASP.NET Core fournit un simple conteneur IoC intégré, mais vous pouvez également utiliser votre conteneur IoC favori, comme Autofac ou Ninject.</span><span class="sxs-lookup"><span data-stu-id="f4206-120">ASP.NET Core provides a simple built-in IoC container, but you can also use your favorite IoC container, like Autofac or Ninject.</span></span>

<span data-ttu-id="f4206-121">En suivant les principes SOLID, vos classes ont naturellement tendance à être petites, bien factorisées et facilement testées.</span><span class="sxs-lookup"><span data-stu-id="f4206-121">By following the SOLID principles, your classes will tend naturally to be small, well-factored, and easily tested.</span></span> <span data-ttu-id="f4206-122">Mais comment savoir si trop de dépendances sont injectées dans vos classes ?</span><span class="sxs-lookup"><span data-stu-id="f4206-122">But how can you know if too many dependencies are being injected into your classes?</span></span> <span data-ttu-id="f4206-123">Si vous utilisez l’inversion de dépendances par le biais du constructeur, vous pouvez facilement le détecter rien qu’en examinant le nombre de paramètres pour votre constructeur.</span><span class="sxs-lookup"><span data-stu-id="f4206-123">If you use DI through the constructor, it will be easy to detect that by just looking at the number of parameters for your constructor.</span></span> <span data-ttu-id="f4206-124">S’il y a trop de dépendances, c’est généralement le signe (un [code smell](http://deviq.com/code-smells/)) que votre classe essaie d’en faire trop et qu’elle enfreint probablement le principe de responsabilité unique.</span><span class="sxs-lookup"><span data-stu-id="f4206-124">If there are too many dependencies, this is generally a sign (a [code smell](http://deviq.com/code-smells/)) that your class is trying to do too much, and is probably violating the Single Responsibility principle.</span></span>

<span data-ttu-id="f4206-125">Un autre guide serait nécessaire pour couvrir les principes SOLID de façon approfondie.</span><span class="sxs-lookup"><span data-stu-id="f4206-125">It would take another guide to cover SOLID in detail.</span></span> <span data-ttu-id="f4206-126">C’est pourquoi le présent guide exige que vous ayez un minimum de connaissances à ce sujet.</span><span class="sxs-lookup"><span data-stu-id="f4206-126">Therefore, this guide requires you to have only a minimum knowledge of these topics.</span></span>

#### <a name="additional-resources"></a><span data-ttu-id="f4206-127">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f4206-127">Additional resources</span></span>

-   <span data-ttu-id="f4206-128">**SOLID: Fundamental OOP Principles**
    [*http://deviq.com/solid/*](http://deviq.com/solid/%20)</span><span class="sxs-lookup"><span data-stu-id="f4206-128">**SOLID: Fundamental OOP Principles**
[*http://deviq.com/solid/*](http://deviq.com/solid/%20)</span></span>

-   <span data-ttu-id="f4206-129">**Inversion of Control Containers and the Dependency Injection pattern**
    [*https://martinfowler.com/articles/injection.html*](https://martinfowler.com/articles/injection.html)</span><span class="sxs-lookup"><span data-stu-id="f4206-129">**Inversion of Control Containers and the Dependency Injection pattern**
[*https://martinfowler.com/articles/injection.html*](https://martinfowler.com/articles/injection.html)</span></span>

-   <span data-ttu-id="f4206-130">**Steve Smith. New is Glue**
    [*https://ardalis.com/new-is-glue*](https://ardalis.com/new-is-glue)</span><span class="sxs-lookup"><span data-stu-id="f4206-130">**Steve Smith. New is Glue**
[*https://ardalis.com/new-is-glue*](https://ardalis.com/new-is-glue)</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="f4206-131">[Précédent](nosql-database-persistence-infrastructure.md)
[Suivant](microservice-application-layer-implementation-web-api.md)</span><span class="sxs-lookup"><span data-stu-id="f4206-131">[Previous](nosql-database-persistence-infrastructure.md)
[Next](microservice-application-layer-implementation-web-api.md)</span></span>
