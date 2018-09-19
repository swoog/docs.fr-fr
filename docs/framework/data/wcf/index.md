---
title: WCF Data Services 4.5
ms.date: 03/30/2017
helpviewer_keywords:
- Astoria
- WCF Data Services, getting started
ms.assetid: 73d2bec3-7c92-4110-b905-11bb0462357a
ms.openlocfilehash: 9ece2fe051855d0fd39556f56a4343ead2c437bc
ms.sourcegitcommit: f513a91160b3fec289dd06646d0d6f81f8fcf910
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46288129"
---
# <a name="wcf-data-services-45"></a><span data-ttu-id="cc199-102">WCF Data Services 4.5</span><span class="sxs-lookup"><span data-stu-id="cc199-102">WCF Data Services 4.5</span></span>

<span data-ttu-id="cc199-103">WCF Data Services (anciennement « ADO.NET Data Services ») est un composant du .NET Framework qui vous permet de créer des services qui utilisent le [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] pour exposer et consommer des données sur le Web ou l’intranet à l’aide de la sémantique de [ transfert d’état Representational (REST)](https://go.microsoft.com/fwlink/?LinkId=113919).</span><span class="sxs-lookup"><span data-stu-id="cc199-103">WCF Data Services (formerly known as "ADO.NET Data Services") is a component of the .NET Framework that enables you to create services that use the [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] to expose and consume data over the Web or intranet by using the semantics of [representational state transfer (REST)](https://go.microsoft.com/fwlink/?LinkId=113919).</span></span> <span data-ttu-id="cc199-104">OData expose les données sous forme de ressources adressables par des URI.</span><span class="sxs-lookup"><span data-stu-id="cc199-104">OData exposes data as resources that are addressable by URIs.</span></span> <span data-ttu-id="cc199-105">Les données sont accessibles et modifiables à l'aide des verbes HTTP standard GET, PUT, POST et DELETE.</span><span class="sxs-lookup"><span data-stu-id="cc199-105">Data is accessed and changed by using standard HTTP verbs of GET, PUT, POST, and DELETE.</span></span> <span data-ttu-id="cc199-106">OData utilise les conventions relation-entité de la [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md) pour exposer des ressources sous forme de jeux d’entités qui sont reliées par des associations.</span><span class="sxs-lookup"><span data-stu-id="cc199-106">OData uses the entity-relationship conventions of the [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md) to expose resources as sets of entities that are related by associations.</span></span>

<span data-ttu-id="cc199-107">WCF Data Services utilise le protocole OData pour l’adressage et la mise à jour des ressources.</span><span class="sxs-lookup"><span data-stu-id="cc199-107">WCF Data Services uses the OData protocol for addressing and updating resources.</span></span> <span data-ttu-id="cc199-108">De cette façon, vous pouvez accéder à ces services à partir de n’importe quel client qui prend en charge d’OData.</span><span class="sxs-lookup"><span data-stu-id="cc199-108">In this way, you can access these services from any client that supports OData.</span></span> <span data-ttu-id="cc199-109">OData vous permet de demander et écrire des données dans les ressources à l’aide de formats de transfert classiques : Atom, un ensemble de normes pour l’échange et la mise à jour des données en tant que XML et JavaScript Objet Notation (JSON), un format d’échange de données textuel utilisé largement dans AJAX application.</span><span class="sxs-lookup"><span data-stu-id="cc199-109">OData enables you to request and write data to resources by using well-known transfer formats: Atom, a set of standards for exchanging and updating data as XML, and JavaScript Object Notation (JSON), a text-based data exchange format used extensively in AJAX application.</span></span>

<span data-ttu-id="cc199-110">WCF Data Services peut exposer des données provenant de différentes sources en tant que flux OData.</span><span class="sxs-lookup"><span data-stu-id="cc199-110">WCF Data Services can expose data that originates from various sources as OData feeds.</span></span> <span data-ttu-id="cc199-111">Visual Studio tools facilitent la création d’un service OData à l’aide d’un modèle de données ADO.NET Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="cc199-111">Visual Studio tools make it easier for you to create an OData-based service by using an ADO.NET Entity Framework data model.</span></span> <span data-ttu-id="cc199-112">Vous pouvez également créer des flux OData en fonction des classes common language runtime (CLR) et les données même à liaison tardive ou non typées.</span><span class="sxs-lookup"><span data-stu-id="cc199-112">You can also create OData feeds based on common language runtime (CLR) classes and even late-bound or un-typed data.</span></span>

<span data-ttu-id="cc199-113">WCF Data Services inclut également un ensemble de bibliothèques clientes, un pour les applications clientes .NET Framework générales et un autre spécifique aux applications basées sur Silverlight.</span><span class="sxs-lookup"><span data-stu-id="cc199-113">WCF Data Services also includes a set of client libraries, one for general .NET Framework client applications and another specifically for Silverlight-based applications.</span></span> <span data-ttu-id="cc199-114">Ces bibliothèques clientes fournissent un modèle de programmation basé sur l’objet lorsque vous accédez à un flux OData depuis des environnements tels que .NET Framework et Silverlight.</span><span class="sxs-lookup"><span data-stu-id="cc199-114">These client libraries provide an object-based programming model when you access an OData feed from environments such as the .NET Framework and Silverlight.</span></span>

## <a name="where-should-i-start"></a><span data-ttu-id="cc199-115">Où est-ce que je dois démarrer ?</span><span class="sxs-lookup"><span data-stu-id="cc199-115">Where Should I Start?</span></span>

<span data-ttu-id="cc199-116">En fonction de vos centres d’intérêt, envisagez la mise en route avec les Services de données WCF dans une des rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc199-116">Depending on your interests, consider getting started with WCF Data Services in one of the following topics.</span></span>

<span data-ttu-id="cc199-117">Je veux rentrer dans le vif du sujet...</span><span class="sxs-lookup"><span data-stu-id="cc199-117">I want to jump right in...</span></span>

-   [<span data-ttu-id="cc199-118">Démarrage rapide</span><span class="sxs-lookup"><span data-stu-id="cc199-118">Quickstart</span></span>](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md)

-   [<span data-ttu-id="cc199-119">Prise en main</span><span class="sxs-lookup"><span data-stu-id="cc199-119">Getting Started</span></span>](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md)

-   [<span data-ttu-id="cc199-120">Démarrage rapide avec Silverlight</span><span class="sxs-lookup"><span data-stu-id="cc199-120">Silverlight Quickstart</span></span>](https://go.microsoft.com/fwlink/?LinkID=192782)

-   [<span data-ttu-id="cc199-121">Démarrage rapide avec Silverlight pour le développement de Windows Phone</span><span class="sxs-lookup"><span data-stu-id="cc199-121">Silverlight Quickstart for Windows Phone Development</span></span>](https://go.microsoft.com/fwlink/?LinkID=214535)

<span data-ttu-id="cc199-122">Montrez-moi du code...</span><span class="sxs-lookup"><span data-stu-id="cc199-122">Just show me some code...</span></span>

-   [<span data-ttu-id="cc199-123">Démarrage rapide</span><span class="sxs-lookup"><span data-stu-id="cc199-123">Quickstart</span></span>](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md)

-   [<span data-ttu-id="cc199-124">Comment : exécuter les requêtes de services de données</span><span class="sxs-lookup"><span data-stu-id="cc199-124">How to: Execute Data Service Queries</span></span>](../../../../docs/framework/data/wcf/how-to-execute-data-service-queries-wcf-data-services.md)

-   [<span data-ttu-id="cc199-125">Comment : lier les données aux éléments Windows Presentation Foundation</span><span class="sxs-lookup"><span data-stu-id="cc199-125">How to: Bind Data to Windows Presentation Foundation Elements</span></span>](../../../../docs/framework/data/wcf/bind-data-to-wpf-elements-wcf-data-services.md)

<span data-ttu-id="cc199-126">Je souhaite en savoir plus sur OData...</span><span class="sxs-lookup"><span data-stu-id="cc199-126">I want to know more about OData...</span></span>

 -   [<span data-ttu-id="cc199-127">Livre blanc : présentation d’OData</span><span class="sxs-lookup"><span data-stu-id="cc199-127">Whitepaper: Introducing OData</span></span>](https://go.microsoft.com/fwlink/?LinkId=220867)

-   [<span data-ttu-id="cc199-128">Site web Open Data Protocol</span><span class="sxs-lookup"><span data-stu-id="cc199-128">Open Data Protocol Web site</span></span>](https://go.microsoft.com/fwlink/?LinkID=184554)

-   [<span data-ttu-id="cc199-129">Kit de développement logiciel (SDK) OData</span><span class="sxs-lookup"><span data-stu-id="cc199-129">OData: SDK</span></span>](https://go.microsoft.com/fwlink/?LinkID=185248)

-   [<span data-ttu-id="cc199-130">OData : forum aux questions</span><span class="sxs-lookup"><span data-stu-id="cc199-130">OData: Frequently Asked Questions</span></span>](https://go.microsoft.com/fwlink/?LinkId=185867)

<span data-ttu-id="cc199-131">Je souhaite regarder des vidéos...</span><span class="sxs-lookup"><span data-stu-id="cc199-131">I want to watch some videos...</span></span>

-   [<span data-ttu-id="cc199-132">Guide du débutant sur WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="cc199-132">Beginner's Guide to WCF Data Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=220864)

-   [<span data-ttu-id="cc199-133">Vidéos du développeur WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="cc199-133">WCF Data Services Developer Videos</span></span>](https://go.microsoft.com/fwlink/?LinkId=220861)

-   [<span data-ttu-id="cc199-134">OData : site web développeurs</span><span class="sxs-lookup"><span data-stu-id="cc199-134">OData: Developers Web site</span></span>](https://go.microsoft.com/fwlink/?LinkId=185866)

<span data-ttu-id="cc199-135">Je souhaite consulter des exemples de bout en bout...</span><span class="sxs-lookup"><span data-stu-id="cc199-135">I want to see end-to-end samples...</span></span>

-   [<span data-ttu-id="cc199-136">Exemples de documentation WCF Data Services dans la galerie d’exemples MSDN</span><span class="sxs-lookup"><span data-stu-id="cc199-136">WCF Data Services Documentation Samples on MSDN Samples Gallery</span></span>](https://go.microsoft.com/fwlink/?LinkID=220865)

-   [<span data-ttu-id="cc199-137">Autres exemples WCF Data Services dans la galerie d’exemples MSDN</span><span class="sxs-lookup"><span data-stu-id="cc199-137">Other WCF Data Services Samples on MSDN Samples Gallery</span></span>](https://go.microsoft.com/fwlink/?LinkId=220866)

-   [<span data-ttu-id="cc199-138">Kit de développement logiciel (SDK) OData</span><span class="sxs-lookup"><span data-stu-id="cc199-138">OData: SDK</span></span>](https://go.microsoft.com/fwlink/?LinkID=185248)

<span data-ttu-id="cc199-139">Qu'en est-il de l'intégration avec Visual Studio ?</span><span class="sxs-lookup"><span data-stu-id="cc199-139">How does it integrate with Visual Studio?</span></span>

-   [<span data-ttu-id="cc199-140">Génération de la bibliothèque cliente du service de données</span><span class="sxs-lookup"><span data-stu-id="cc199-140">Generating the Data Service Client Library</span></span>](../../../../docs/framework/data/wcf/generating-the-data-service-client-library-wcf-data-services.md)

-   [<span data-ttu-id="cc199-141">Création du service de données</span><span class="sxs-lookup"><span data-stu-id="cc199-141">Creating the Data Service</span></span>](../../../../docs/framework/data/wcf/creating-the-data-service.md)

-   [<span data-ttu-id="cc199-142">Fournisseur Entity Framework</span><span class="sxs-lookup"><span data-stu-id="cc199-142">Entity Framework Provider</span></span>](../../../../docs/framework/data/wcf/entity-framework-provider-wcf-data-services.md)

<span data-ttu-id="cc199-143">Comment puis-je l'utiliser ?</span><span class="sxs-lookup"><span data-stu-id="cc199-143">What can I do with it?</span></span>

-   [<span data-ttu-id="cc199-144">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="cc199-144">Overview</span></span>](../../../../docs/framework/data/wcf/wcf-data-services-overview.md)

-   [<span data-ttu-id="cc199-145">Livre blanc : présentation d’OData</span><span class="sxs-lookup"><span data-stu-id="cc199-145">Whitepaper: Introducing OData</span></span>](https://go.microsoft.com/fwlink/?LinkId=220867)

-   [<span data-ttu-id="cc199-146">Scénarios d’application</span><span class="sxs-lookup"><span data-stu-id="cc199-146">Application Scenarios</span></span>](../../../../docs/framework/data/wcf/application-scenarios-wcf-data-services.md)

<span data-ttu-id="cc199-147">Je souhaite utiliser Silverlight...</span><span class="sxs-lookup"><span data-stu-id="cc199-147">I want to use Silverlight...</span></span>

-   [<span data-ttu-id="cc199-148">Démarrage rapide avec Silverlight</span><span class="sxs-lookup"><span data-stu-id="cc199-148">Silverlight Quickstart</span></span>](https://go.microsoft.com/fwlink/?LinkID=192782)

-   [<span data-ttu-id="cc199-149">WCF Data Services (Silverlight)</span><span class="sxs-lookup"><span data-stu-id="cc199-149">WCF Data Services (Silverlight)</span></span>](https://go.microsoft.com/fwlink/?LinkID=143149)

-   [<span data-ttu-id="cc199-150">Prise en main de Silverlight</span><span class="sxs-lookup"><span data-stu-id="cc199-150">Getting Started with Silverlight</span></span>](https://go.microsoft.com/fwlink/?LinkId=148366)

<span data-ttu-id="cc199-151">Je souhaite utiliser LINQ...</span><span class="sxs-lookup"><span data-stu-id="cc199-151">I want to use LINQ...</span></span>

-   [<span data-ttu-id="cc199-152">Interrogation du service de données</span><span class="sxs-lookup"><span data-stu-id="cc199-152">Querying the Data Service</span></span>](../../../../docs/framework/data/wcf/querying-the-data-service-wcf-data-services.md)

-   [<span data-ttu-id="cc199-153">Considérations sur LINQ</span><span class="sxs-lookup"><span data-stu-id="cc199-153">LINQ Considerations</span></span>](../../../../docs/framework/data/wcf/linq-considerations-wcf-data-services.md)

-   [<span data-ttu-id="cc199-154">Comment : exécuter les requêtes de services de données</span><span class="sxs-lookup"><span data-stu-id="cc199-154">How to: Execute Data Service Queries</span></span>](../../../../docs/framework/data/wcf/how-to-execute-data-service-queries-wcf-data-services.md)

<span data-ttu-id="cc199-155">Toujours, j’ai besoin d’informations supplémentaires...</span><span class="sxs-lookup"><span data-stu-id="cc199-155">I still need some more information...</span></span>

-   [<span data-ttu-id="cc199-156">Blog de l’équipe WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="cc199-156">WCF Data Services Team Blog</span></span>](https://go.microsoft.com/fwlink/?LinkID=150511)

-   [<span data-ttu-id="cc199-157">Ressources</span><span class="sxs-lookup"><span data-stu-id="cc199-157">Resources</span></span>](../../../../docs/framework/data/wcf/wcf-data-services-resources.md)

-   [<span data-ttu-id="cc199-158">Centre de développement WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="cc199-158">WCF Data Services Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=220868)

-   [<span data-ttu-id="cc199-159">Site web Open Data Protocol</span><span class="sxs-lookup"><span data-stu-id="cc199-159">Open Data Protocol Web site</span></span>](https://go.microsoft.com/fwlink/?LinkID=184554)

## <a name="in-this-section"></a><span data-ttu-id="cc199-160">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="cc199-160">In This Section</span></span>

 [<span data-ttu-id="cc199-161">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="cc199-161">Overview</span></span>](../../../../docs/framework/data/wcf/wcf-data-services-overview.md)

 <span data-ttu-id="cc199-162">Fournit une vue d’ensemble des fonctionnalités et des fonctionnalités disponibles dans WCF Data Services.</span><span class="sxs-lookup"><span data-stu-id="cc199-162">Provides an overview of the features and functionality available in WCF Data Services.</span></span>

 [<span data-ttu-id="cc199-163">Nouveautés de WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="cc199-163">What's New in WCF Data Services</span></span>](https://msdn.microsoft.com/library/cf22cad5-b8d9-472b-8d7c-b863b64eaae8)

 <span data-ttu-id="cc199-164">Décrit les nouvelles fonctionnalités dans WCF Data Services et la prise en charge des nouvelles fonctionnalités OData.</span><span class="sxs-lookup"><span data-stu-id="cc199-164">Describes new functionality in WCF Data Services and support for new OData features.</span></span>

 [<span data-ttu-id="cc199-165">Prise en main</span><span class="sxs-lookup"><span data-stu-id="cc199-165">Getting Started</span></span>](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md)

 <span data-ttu-id="cc199-166">Décrit comment exposer et consommer des flux OData à l’aide de WCF Data Services.</span><span class="sxs-lookup"><span data-stu-id="cc199-166">Describes how to expose and consume OData feeds by using WCF Data Services.</span></span>

 [<span data-ttu-id="cc199-167">Définition de WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="cc199-167">Defining WCF Data Services</span></span>](../../../../docs/framework/data/wcf/defining-wcf-data-services.md)

 <span data-ttu-id="cc199-168">Décrit comment créer et configurer un service de données qui expose des flux OData.</span><span class="sxs-lookup"><span data-stu-id="cc199-168">Describes how to create and configure a data service that exposes OData feeds.</span></span>

 [<span data-ttu-id="cc199-169">Bibliothèque cliente WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="cc199-169">WCF Data Services Client Library</span></span>](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)

 <span data-ttu-id="cc199-170">Décrit comment utiliser les bibliothèques clientes pour consommer des flux OData à partir d’une application cliente .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="cc199-170">Describes how to use client libraries to consume OData feeds from a .NET Framework client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc199-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc199-171">See Also</span></span>

- [<span data-ttu-id="cc199-172">Representational State Transfer (REST)</span><span class="sxs-lookup"><span data-stu-id="cc199-172">Representational State Transfer (REST)</span></span>](https://go.microsoft.com/fwlink/?LinkId=113919)
