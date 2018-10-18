---
title: Approches d’architecture - applications sans serveur
description: Introduction à l’architecture approches pour créer des applications d’entreprise basée sur le cloud, à partir des architectures multicouches pour sans serveur.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: 21e191f17e7d0b4f2d64454fb14c46a4831a8375
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "49370019"
---
# <a name="architecture-approaches"></a><span data-ttu-id="59ce1-103">Approches de l’architecture</span><span class="sxs-lookup"><span data-stu-id="59ce1-103">Architecture approaches</span></span>

<span data-ttu-id="59ce1-104">Présentation des approches existantes à l’architecture des applications d’entreprise vous aide à clarifier le rôle joué par sans serveur.</span><span class="sxs-lookup"><span data-stu-id="59ce1-104">Understanding existing approaches to architecting enterprise apps helps clarify the role played by serverless.</span></span> <span data-ttu-id="59ce1-105">Il existe plusieurs approches et modèles évolué au fil des décennies de développement logiciel et que tous ont leurs propres avantages et inconvénients.</span><span class="sxs-lookup"><span data-stu-id="59ce1-105">There are many approaches and patterns that evolved over decades of software development, and all have their own pros and cons.</span></span> <span data-ttu-id="59ce1-106">Dans de nombreux cas, la solution ultime pas, vous devrez choisir une approche unique, mais peut intégrer plusieurs approches.</span><span class="sxs-lookup"><span data-stu-id="59ce1-106">In many cases, the ultimate solution may not involve deciding on a single approach but may integrate several approaches.</span></span> <span data-ttu-id="59ce1-107">Scénarios de migration impliquent souvent un décalage à partir de l’approche d’une architecture à un autre via une approche hybride.</span><span class="sxs-lookup"><span data-stu-id="59ce1-107">Migration scenarios often involve shifting from one architecture approach to another through a hybrid approach.</span></span>

<span data-ttu-id="59ce1-108">Ce chapitre fournit une vue d’ensemble de ces deux modèles d’architecture logique et physique pour les applications d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="59ce1-108">This chapter provides an overview of both logical and physical architecture patterns for enterprise applications.</span></span>

## <a name="architecture-patterns"></a><span data-ttu-id="59ce1-109">Modèles d’architecture</span><span class="sxs-lookup"><span data-stu-id="59ce1-109">Architecture patterns</span></span>

<span data-ttu-id="59ce1-110">Les applications métier modernes suivent une variété de modèles d’architecture.</span><span class="sxs-lookup"><span data-stu-id="59ce1-110">Modern business applications follow a variety of architecture patterns.</span></span> <span data-ttu-id="59ce1-111">Cette section représente une enquête des modèles courants.</span><span class="sxs-lookup"><span data-stu-id="59ce1-111">This section represents a survey of common patterns.</span></span> <span data-ttu-id="59ce1-112">Les modèles répertoriés ici ne sont pas nécessairement toutes les meilleures pratiques, mais illustrent différentes approches.</span><span class="sxs-lookup"><span data-stu-id="59ce1-112">The patterns listed here aren't necessarily all best practices, but illustrate different approaches.</span></span>

<span data-ttu-id="59ce1-113">Pour plus d’informations, consultez [guide d’architecture Azure application](https://docs.microsoft.com/azure/architecture/guide/).</span><span class="sxs-lookup"><span data-stu-id="59ce1-113">For more information, see [Azure application architecture guide](https://docs.microsoft.com/azure/architecture/guide/).</span></span>

## <a name="monoliths"></a><span data-ttu-id="59ce1-114">Monolithes</span><span class="sxs-lookup"><span data-stu-id="59ce1-114">Monoliths</span></span>

<span data-ttu-id="59ce1-115">De nombreuses applications métier suivent un modèle de MONOLITHE.</span><span class="sxs-lookup"><span data-stu-id="59ce1-115">Many business applications follow a monolith pattern.</span></span> <span data-ttu-id="59ce1-116">Les applications héritées sont souvent implémentées comme des monolithes.</span><span class="sxs-lookup"><span data-stu-id="59ce1-116">Legacy applications are often implemented as monoliths.</span></span> <span data-ttu-id="59ce1-117">Dans le modèle d’application monolithique, tous les problèmes d’application sont contenus dans un déploiement unique.</span><span class="sxs-lookup"><span data-stu-id="59ce1-117">In the monolith pattern, all application concerns are contained in a single deployment.</span></span> <span data-ttu-id="59ce1-118">Tous les éléments à partir de l’interface utilisateur pour les appels de base de données sont inclus dans la même base de code.</span><span class="sxs-lookup"><span data-stu-id="59ce1-118">Everything from user interface to database calls is included in the same codebase.</span></span>

![Architecture de l’application monolithique](./media/monolith-architecture.png)

<span data-ttu-id="59ce1-120">Il existe plusieurs avantages à l’approche monolithique.</span><span class="sxs-lookup"><span data-stu-id="59ce1-120">There are several advantages to the monolith approach.</span></span> <span data-ttu-id="59ce1-121">Il est souvent facile extraire une seule base de code et commencer à travailler.</span><span class="sxs-lookup"><span data-stu-id="59ce1-121">It's often easy to pull down a single code base and start working.</span></span> <span data-ttu-id="59ce1-122">Temps d’accélération peut être inférieur et création d’environnements de test est aussi simple que de fournir une nouvelle copie.</span><span class="sxs-lookup"><span data-stu-id="59ce1-122">Ramp up time may be less, and creating test environments is as simple as providing a new copy.</span></span> <span data-ttu-id="59ce1-123">Au modèle monolithique peut être conçu pour inclure plusieurs composants et applications.</span><span class="sxs-lookup"><span data-stu-id="59ce1-123">The monolith may be designed to include multiple components and applications.</span></span>

<span data-ttu-id="59ce1-124">Malheureusement, le modèle MONOLITHE tend à décomposer à grande échelle.</span><span class="sxs-lookup"><span data-stu-id="59ce1-124">Unfortunately, the monolith pattern tends to break down at scale.</span></span> <span data-ttu-id="59ce1-125">Principaux inconvénients de l’approche monolithique :</span><span class="sxs-lookup"><span data-stu-id="59ce1-125">Major disadvantages of the monolith approach include:</span></span>

* <span data-ttu-id="59ce1-126">Il est difficile de travailler en parallèle dans le même code base.</span><span class="sxs-lookup"><span data-stu-id="59ce1-126">Difficult to work in parallel in the same code base.</span></span>
* <span data-ttu-id="59ce1-127">Toute modification, quelle que soit la façon dont trivial, requiert le déploiement d’une nouvelle version de l’application entière.</span><span class="sxs-lookup"><span data-stu-id="59ce1-127">Any change, no matter how trivial, requires deploying a new version of the entire application.</span></span>
* <span data-ttu-id="59ce1-128">Refactorisation potentiellement a un impact sur l’application entière.</span><span class="sxs-lookup"><span data-stu-id="59ce1-128">Refactoring potentially impacts the entire application.</span></span>
* <span data-ttu-id="59ce1-129">Souvent la seule solution à l’échelle consiste à créer plusieurs copies gourmandes en ressources du modèle monolithique.</span><span class="sxs-lookup"><span data-stu-id="59ce1-129">Often the only solution to scale is to create multiple, resource-intensive copies of the monolith.</span></span>
* <span data-ttu-id="59ce1-130">Développez des systèmes ou d’autres systèmes sont acquis, intégration peut être difficile.</span><span class="sxs-lookup"><span data-stu-id="59ce1-130">As systems expand or other systems are acquired, integration can be difficult.</span></span>
* <span data-ttu-id="59ce1-131">Il peut être difficile à tester en raison de la nécessité de configurer le MONOLITHE entière.</span><span class="sxs-lookup"><span data-stu-id="59ce1-131">It may be difficult to test due to the need to configure the entire monolith.</span></span>
* <span data-ttu-id="59ce1-132">Il est difficile de réutilisation du code et autres applications finissent souvent leurs propres copies de code.</span><span class="sxs-lookup"><span data-stu-id="59ce1-132">Code reuse is challenging and often other apps end up having their own copies of code.</span></span>

<span data-ttu-id="59ce1-133">De nombreuses entreprises rechercher vers le cloud comme une opportunité de migration d’applications de MONOLITHE et en même temps les refactoriser à davantage de modèles utilisables.</span><span class="sxs-lookup"><span data-stu-id="59ce1-133">Many businesses look to the cloud as an opportunity to migrate monolith applications and at the same time refactor them to more usable patterns.</span></span> <span data-ttu-id="59ce1-134">Il est courant de séparer les applications individuelles et les composants pour leur permettre d’être conservées, déployés et mis à l’échelle séparément.</span><span class="sxs-lookup"><span data-stu-id="59ce1-134">It's common to break out the individual applications and components to allow them to be maintained, deployed, and scaled separately.</span></span>

## <a name="n-layer-applications"></a><span data-ttu-id="59ce1-135">Applications de couche N</span><span class="sxs-lookup"><span data-stu-id="59ce1-135">N-Layer applications</span></span>

<span data-ttu-id="59ce1-136">Logique d’application partition N couches application en couches spécifiques.</span><span class="sxs-lookup"><span data-stu-id="59ce1-136">N-layer application partition application logic into specific layers.</span></span> <span data-ttu-id="59ce1-137">Les couches plus courantes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="59ce1-137">The most common layers include:</span></span>

* <span data-ttu-id="59ce1-138">Interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="59ce1-138">User interface</span></span>
* <span data-ttu-id="59ce1-139">logique métier</span><span class="sxs-lookup"><span data-stu-id="59ce1-139">Business logic</span></span>
* <span data-ttu-id="59ce1-140">Accès aux données</span><span class="sxs-lookup"><span data-stu-id="59ce1-140">Data access</span></span>

<span data-ttu-id="59ce1-141">Autres couches peuvent inclure intergiciel (middleware), traitement par lots et API.</span><span class="sxs-lookup"><span data-stu-id="59ce1-141">Other layers may include middleware, batch processing, and API.</span></span> <span data-ttu-id="59ce1-142">Il est important de noter que les couches sont logiques.</span><span class="sxs-lookup"><span data-stu-id="59ce1-142">It's important to note the layers are logical.</span></span> <span data-ttu-id="59ce1-143">Même si elles sont développées de manière isolée, ils peuvent tous être déployés à la même plateforme cible.</span><span class="sxs-lookup"><span data-stu-id="59ce1-143">Although they're developed in isolation, they may all be deployed to the same target platform.</span></span>

![Architecture de couche N](./media/n-layer-architecture.png)

<span data-ttu-id="59ce1-145">Il existe plusieurs avantages à l’approche à N couches, y compris :</span><span class="sxs-lookup"><span data-stu-id="59ce1-145">There are several advantages to the N-Layer approach, including:</span></span>

* <span data-ttu-id="59ce1-146">La refactorisation est isolée sur une couche.</span><span class="sxs-lookup"><span data-stu-id="59ce1-146">Refactoring is isolated to a layer.</span></span>
* <span data-ttu-id="59ce1-147">Indépendamment, équipes peuvent créer, tester, déployer et maintenir des couches distinctes.</span><span class="sxs-lookup"><span data-stu-id="59ce1-147">Teams can independently build, test, deploy, and maintain separate layers.</span></span>
* <span data-ttu-id="59ce1-148">Couches peuvent être échangées, par exemple la couche données peut accéder à plusieurs bases de données sans nécessiter de modifications de la couche d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="59ce1-148">Layers can be swapped out, for example the data layer may access multiple databases without requiring changes to the UI layer.</span></span>

<span data-ttu-id="59ce1-149">Sans serveur peut servir à implémenter une ou plusieurs couches.</span><span class="sxs-lookup"><span data-stu-id="59ce1-149">Serverless may be used to implement one or more layers.</span></span>

## <a name="microservices"></a><span data-ttu-id="59ce1-150">Microservices</span><span class="sxs-lookup"><span data-stu-id="59ce1-150">Microservices</span></span>

<span data-ttu-id="59ce1-151">**[Microservices](https://docs.microsoft.com/azure/architecture/guide/architecture-styles/microservices)**  architectures contiennent des caractéristiques communes qui incluent :</span><span class="sxs-lookup"><span data-stu-id="59ce1-151">**[Microservices](https://docs.microsoft.com/azure/architecture/guide/architecture-styles/microservices)** architectures contain common characteristics that include:</span></span>

* <span data-ttu-id="59ce1-152">Les applications sont composées de plusieurs petits services.</span><span class="sxs-lookup"><span data-stu-id="59ce1-152">Applications are composed of several small services.</span></span>
* <span data-ttu-id="59ce1-153">Chaque service s’exécute dans son propre processus.</span><span class="sxs-lookup"><span data-stu-id="59ce1-153">Each service runs in its own process.</span></span>
* <span data-ttu-id="59ce1-154">Les services sont alignées autour des domaines d’activité.</span><span class="sxs-lookup"><span data-stu-id="59ce1-154">Services are aligned around business domains.</span></span>
* <span data-ttu-id="59ce1-155">Services communiquent via des API légères, généralement à l’aide de HTTP comme transport.</span><span class="sxs-lookup"><span data-stu-id="59ce1-155">Services communicate over lightweight APIs, typically using HTTP as the transport.</span></span>
* <span data-ttu-id="59ce1-156">Services peuvent être déployés et mis à niveau indépendamment.</span><span class="sxs-lookup"><span data-stu-id="59ce1-156">Services can be deployed and upgraded independently.</span></span>
* <span data-ttu-id="59ce1-157">Services ne sont pas dépendants sur un seul magasin de données.</span><span class="sxs-lookup"><span data-stu-id="59ce1-157">Services aren't dependent on a single data store.</span></span>
* <span data-ttu-id="59ce1-158">Le système est conçu par un échec à l’esprit, et l’application peut toujours s’exécuter même si certains services échouent.</span><span class="sxs-lookup"><span data-stu-id="59ce1-158">The system is designed with failure in mind, and the app may still run even when certain services fail.</span></span>

<span data-ttu-id="59ce1-159">Microservices n’êtes pas obligé d’être mutuellement exclusifs aux autres approches d’architecture.</span><span class="sxs-lookup"><span data-stu-id="59ce1-159">Microservices don't have to be mutually exclusive to other architecture approaches.</span></span> <span data-ttu-id="59ce1-160">Par exemple, une architecture multiniveau peut utiliser des microservices pour la couche intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="59ce1-160">For example, an N-Tier architecture may use microservices for the middle tier.</span></span> <span data-ttu-id="59ce1-161">Il est également possible d’implémenter des microservices de plusieurs façons, à partir de répertoires virtuels sur les hôtes IIS aux conteneurs.</span><span class="sxs-lookup"><span data-stu-id="59ce1-161">It's also possible to implement microservices in a variety of ways, from virtual directories on IIS hosts to containers.</span></span> <span data-ttu-id="59ce1-162">Caractéristiques des microservices idéales en particulier pour les implémentations sans serveur.</span><span class="sxs-lookup"><span data-stu-id="59ce1-162">The characteristics of microservices make them especially ideal for serverless implementations.</span></span>

![Architecture en microservices](./media/microservices-architecture.png)

<span data-ttu-id="59ce1-164">Les professionnels des architectures de microservices sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="59ce1-164">The pros of microservices architectures include:</span></span>

* <span data-ttu-id="59ce1-165">Il est souvent isolée sur un seul service de refactorisation.</span><span class="sxs-lookup"><span data-stu-id="59ce1-165">Refactoring is often isolated to a single service.</span></span>
* <span data-ttu-id="59ce1-166">Les services peuvent être mis à niveau indépendamment les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="59ce1-166">Services can be upgraded independently of each other.</span></span>
* <span data-ttu-id="59ce1-167">La résilience et l’élasticité peuvent être paramétrés pour les demandes de services individuels.</span><span class="sxs-lookup"><span data-stu-id="59ce1-167">Resiliency and elasticity can be tuned to the demands of individual services.</span></span>
* <span data-ttu-id="59ce1-168">Développement peut se produire en parallèle sur différentes plateformes et des équipes disparates.</span><span class="sxs-lookup"><span data-stu-id="59ce1-168">Development can happen in parallel across disparate teams and platforms.</span></span>
* <span data-ttu-id="59ce1-169">Il est plus facile d’écrire des tests complets pour les services isolés.</span><span class="sxs-lookup"><span data-stu-id="59ce1-169">It's easier to write comprehensive tests for isolated services.</span></span>

<span data-ttu-id="59ce1-170">Microservices sont fournis avec leurs propres problèmes, notamment :</span><span class="sxs-lookup"><span data-stu-id="59ce1-170">Microservices come with their own challenges, including:</span></span>

* <span data-ttu-id="59ce1-171">Déterminer quels services sont disponibles et comment les appeler.</span><span class="sxs-lookup"><span data-stu-id="59ce1-171">Determining what services are available and how to call them.</span></span>
* <span data-ttu-id="59ce1-172">La gestion du cycle de vie des services.</span><span class="sxs-lookup"><span data-stu-id="59ce1-172">Managing the lifecycle of services.</span></span>
* <span data-ttu-id="59ce1-173">Comprendre comment les services s’assemblent dans l’application globale.</span><span class="sxs-lookup"><span data-stu-id="59ce1-173">Understanding how services fit together in the overall application.</span></span>
* <span data-ttu-id="59ce1-174">Complète du système de test d’appels effectués entre des services disparates.</span><span class="sxs-lookup"><span data-stu-id="59ce1-174">Full system testing of calls made across disparate services.</span></span>

<span data-ttu-id="59ce1-175">En fin de compte il existe des solutions pour répondre à tous ces défis, y compris qui exploite les avantages de sans serveur qui sont décrits plus loin.</span><span class="sxs-lookup"><span data-stu-id="59ce1-175">Ultimately there are solutions to address all of these challenges, including tapping into the benefits of serverless that are discussed later.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="59ce1-176">[Précédent](index.md)
[Suivant](architecture-deployment-approaches.md)</span><span class="sxs-lookup"><span data-stu-id="59ce1-176">[Previous](index.md)
[Next](architecture-deployment-approaches.md)</span></span>
