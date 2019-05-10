---
title: Points de terminaison Windows Communication Foundation
ms.date: 03/30/2017
helpviewer_keywords:
- endpoints [WCF]
ms.assetid: bd0c310f-dd9f-4081-9be2-3db5909850b6
ms.openlocfilehash: 1a18e2ab31998b7759803e023151892694757119
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64613382"
---
# <a name="windows-communication-foundation-endpoints"></a><span data-ttu-id="fa74d-102">Points de terminaison Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="fa74d-102">Windows Communication Foundation Endpoints</span></span>
<span data-ttu-id="fa74d-103">Toutes les communications avec un service Windows Communication Foundation (WCF) s’effectue via le *points de terminaison* du service.</span><span class="sxs-lookup"><span data-stu-id="fa74d-103">All communication with a Windows Communication Foundation (WCF) service occurs through the *endpoints* of the service.</span></span> <span data-ttu-id="fa74d-104">Points de terminaison fournissent les clients à accéder aux fonctionnalités offertes par un service WCF.</span><span class="sxs-lookup"><span data-stu-id="fa74d-104">Endpoints provide clients access to the functionality that a WCF service offers.</span></span>  
  
 <span data-ttu-id="fa74d-105">Pour une vue d’ensemble sur la création d’un point de terminaison, consultez [vue d’ensemble de la création de point de terminaison](../../../docs/framework/wcf/endpoint-creation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fa74d-105">For an overview about how to create an endpoint, see [Endpoint Creation Overview](../../../docs/framework/wcf/endpoint-creation-overview.md).</span></span> <span data-ttu-id="fa74d-106">Chaque point de terminaison contient :</span><span class="sxs-lookup"><span data-stu-id="fa74d-106">Each endpoint contains:</span></span>  
  
- <span data-ttu-id="fa74d-107">Une adresse qui indique où rechercher le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="fa74d-107">An address that indicates where to find the endpoint.</span></span>  
  
- <span data-ttu-id="fa74d-108">Une liaison qui spécifie comment un client peut communiquer avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="fa74d-108">A binding that specifies how a client can communicate with the endpoint.</span></span>  
  
- <span data-ttu-id="fa74d-109">Un contrat qui identifie les méthodes disponibles.</span><span class="sxs-lookup"><span data-stu-id="fa74d-109">A contract that identifies the methods available.</span></span>  
  
 <span data-ttu-id="fa74d-110">Pour obtenir une description de la manière dont les parties individuelles d'un point de terminaison sont spécifiées, consultez :</span><span class="sxs-lookup"><span data-stu-id="fa74d-110">For descriptions about how to specify these individual parts of an endpoint, see:</span></span>  
  
- [<span data-ttu-id="fa74d-111">Spécification d’une adresse de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fa74d-111">Specifying an Endpoint Address</span></span>](../../../docs/framework/wcf/specifying-an-endpoint-address.md)  
  
- [<span data-ttu-id="fa74d-112">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="fa74d-112">Using Bindings to Configure Services and Clients</span></span>](../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
  
- [<span data-ttu-id="fa74d-113">Conception et implémentation de services</span><span class="sxs-lookup"><span data-stu-id="fa74d-113">Designing and Implementing Services</span></span>](../../../docs/framework/wcf/designing-and-implementing-services.md)  
  
## <a name="in-this-section"></a><span data-ttu-id="fa74d-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="fa74d-114">In This Section</span></span>  
 [<span data-ttu-id="fa74d-115">Vue d’ensemble de la création de points de terminaison</span><span class="sxs-lookup"><span data-stu-id="fa74d-115">Endpoint Creation Overview</span></span>](../../../docs/framework/wcf/endpoint-creation-overview.md)  
 <span data-ttu-id="fa74d-116">Décrit la structure d’un point de terminaison et explique comment définir un point de terminaison dans la configuration et dans le code, ainsi que la manière d’utiliser les points de terminaison par défaut, les liaisons et les comportements fournis par le runtime.</span><span class="sxs-lookup"><span data-stu-id="fa74d-116">Describes the structure of an endpoint and outlines how to define an endpoint in configuration and in code, as well as how to use the default endpoints, bindings, and behaviors provided by the runtime.</span></span>  
  
 [<span data-ttu-id="fa74d-117">Spécification d’une adresse de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fa74d-117">Specifying an Endpoint Address</span></span>](../../../docs/framework/wcf/specifying-an-endpoint-address.md)  
 <span data-ttu-id="fa74d-118">Décrit comment la communication avec un service WCF s’effectue via des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="fa74d-118">Describes how communication with a WCF service occurs through endpoints.</span></span>  
  
 [<span data-ttu-id="fa74d-119">Guide pratique pour Créer un point de terminaison de Service dans la Configuration</span><span class="sxs-lookup"><span data-stu-id="fa74d-119">How to: Create a Service Endpoint in Configuration</span></span>](../../../docs/framework/wcf/feature-details/how-to-create-a-service-endpoint-in-configuration.md)  
 <span data-ttu-id="fa74d-120">Montre comment créer un point de terminaison de service dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="fa74d-120">Demonstrates how to create a service endpoint in configuration.</span></span>  
  
 [<span data-ttu-id="fa74d-121">Guide pratique pour Créer un point de terminaison de Service dans le Code</span><span class="sxs-lookup"><span data-stu-id="fa74d-121">How to: Create a Service Endpoint in Code</span></span>](../../../docs/framework/wcf/feature-details/how-to-create-a-service-endpoint-in-code.md)  
 <span data-ttu-id="fa74d-122">Montre comment créer un point de terminaison de service dans le code.</span><span class="sxs-lookup"><span data-stu-id="fa74d-122">Demonstrates how to create a service endpoint in code.</span></span>  
  
 [<span data-ttu-id="fa74d-123">Publication de points de terminaison de métadonnées</span><span class="sxs-lookup"><span data-stu-id="fa74d-123">Publishing Metadata Endpoints</span></span>](../../../docs/framework/wcf/publishing-metadata-endpoints.md)  
 <span data-ttu-id="fa74d-124">Montre comment publier des métadonnées en publiant des points de terminaison de métadonnées dans la configuration et dans le code.</span><span class="sxs-lookup"><span data-stu-id="fa74d-124">Demonstrates how to publish metadata by publishing metadata endpoints in configuration and in code.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="fa74d-125">Référence</span><span class="sxs-lookup"><span data-stu-id="fa74d-125">Reference</span></span>  
 <xref:System.ServiceModel.EndpointAddress>  
  
## <a name="related-sections"></a><span data-ttu-id="fa74d-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa74d-126">Related Sections</span></span>  
 [<span data-ttu-id="fa74d-127">Cycle de vie de la programmation de base</span><span class="sxs-lookup"><span data-stu-id="fa74d-127">Basic Programming Lifecycle</span></span>](../../../docs/framework/wcf/basic-programming-lifecycle.md)
