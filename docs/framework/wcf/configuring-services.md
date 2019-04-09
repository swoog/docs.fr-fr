---
title: Configuration des services WCF
ms.date: 03/30/2017
helpviewer_keywords:
- configuration [WCF]
ms.assetid: beac771e-f28e-4f84-9ff1-ad9251c726d3
ms.openlocfilehash: 81727adbf985986a71cc9f9e2d42a1de0cb1fd76
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59156505"
---
# <a name="configuring-wcf-services"></a><span data-ttu-id="2997f-102">Configuration des services WCF</span><span class="sxs-lookup"><span data-stu-id="2997f-102">Configuring WCF services</span></span>

<span data-ttu-id="2997f-103">Une fois que vous avez conçu et implémenté votre contrat de service, vous êtes prêt à configurer votre service.</span><span class="sxs-lookup"><span data-stu-id="2997f-103">Once you have designed and implemented your service contract, you are ready to configure your service.</span></span> <span data-ttu-id="2997f-104">C'est à ce stade que vous définissez et personnalisez la manière dont votre service est exposé aux clients, notamment l'adresse de son emplacement, l'encodage du transport et du message qu'il utilise pour envoyer et recevoir des messages, et le type de sécurité qu'il nécessite.</span><span class="sxs-lookup"><span data-stu-id="2997f-104">This is where you define and customize how your service is exposed to clients, including specifying the address where it can be found, the transport and message encoding it uses to send and receive messages, and the type of security it requires.</span></span>  
  
 <span data-ttu-id="2997f-105">La configuration utilisée dans ce scénario comprend toutes les méthodes, de manière impérative dans le code ou à l'aide d'un fichier de configuration, permettant de définir et de personnaliser les divers aspects d'un service, tels que la spécification de ses adresses de point de terminaison, les transports utilisés et ses méthodes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2997f-105">Configuration as used here includes all the ways, imperatively in code or by using a configuration file, in which you can define and customize the various aspects of a service, such as specifying its endpoint addresses, the transports used, and its security schemes.</span></span> <span data-ttu-id="2997f-106">Dans la pratique, écriture de la configuration est des principales parties de la programmation d’applications WCF.</span><span class="sxs-lookup"><span data-stu-id="2997f-106">In practice, writing configuration is a major part of programming WCF applications.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2997f-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2997f-107">In This Section</span></span>  
 [<span data-ttu-id="2997f-108">Configuration simplifiée</span><span class="sxs-lookup"><span data-stu-id="2997f-108">Simplified Configuration</span></span>](../../../docs/framework/wcf/simplified-configuration.md)  
 <span data-ttu-id="2997f-109">En commençant par [!INCLUDE[netfx40_long](../../../includes/netfx40-long-md.md)], WCF est fourni avec un nouveau modèle de configuration par défaut qui simplifie les conditions requises de configuration WCF.</span><span class="sxs-lookup"><span data-stu-id="2997f-109">Starting with [!INCLUDE[netfx40_long](../../../includes/netfx40-long-md.md)], WCF comes with a new default configuration model that simplifies WCF configuration requirements.</span></span> <span data-ttu-id="2997f-110">Si vous ne fournissez pas de toute configuration de WCF pour un service particulier, le runtime configure automatiquement votre service avec les comportements, les liaisons et les points de terminaison par défaut.</span><span class="sxs-lookup"><span data-stu-id="2997f-110">If you do not provide any WCF configuration for a particular service, the runtime automatically configures your service with default endpoints, bindings, and behaviors.</span></span>  
  
 [<span data-ttu-id="2997f-111">Configuration des services à l'aide de fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="2997f-111">Configuring Services Using Configuration Files</span></span>](../../../docs/framework/wcf/configuring-services-using-configuration-files.md)  
 <span data-ttu-id="2997f-112">Un service Windows Communication Foundation (WCF) est configurable à l’aide du [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] configuration de la technologie.</span><span class="sxs-lookup"><span data-stu-id="2997f-112">A Windows Communication Foundation (WCF) service is configurable using the [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] configuration technology.</span></span> <span data-ttu-id="2997f-113">En règle générale, les éléments XML sont ajoutés au fichier Web.config pour un site Internet Information Services (IIS) qui héberge un service WCF.</span><span class="sxs-lookup"><span data-stu-id="2997f-113">Most commonly, XML elements are added to the Web.config file for an Internet Information Services (IIS) site that hosts a WCF service.</span></span> <span data-ttu-id="2997f-114">Les éléments vous permettent de modifier des détails, tels que les adresses de point de terminaison (les adresses réelles qui communiquent avec le service), à partir de chaque ordinateur individuel.</span><span class="sxs-lookup"><span data-stu-id="2997f-114">The elements allow you to change details, such as the endpoint addresses (the actual addresses used to communicate with the service) on a machine-by-machine basis.</span></span>  
  
 [<span data-ttu-id="2997f-115">Liaisons</span><span class="sxs-lookup"><span data-stu-id="2997f-115">Bindings</span></span>](../../../docs/framework/wcf/bindings.md)  
 <span data-ttu-id="2997f-116">En outre, WCF inclut plusieurs configurations courantes fournies par le système sous la forme de liaisons qui vous permettent de sélectionner rapidement les principales fonctionnalités de base pour la manière dont un client / service communiquent, tels que les transports, sécurité et utilisé des encodages de message.</span><span class="sxs-lookup"><span data-stu-id="2997f-116">In addition, WCF includes several system-provided common configurations in the form of bindings that allow you to quickly select the most basic features for how a client and service communicate, such as the transports, security, and message encodings used.</span></span>  
  
 [<span data-ttu-id="2997f-117">Points de terminaison</span><span class="sxs-lookup"><span data-stu-id="2997f-117">Endpoints</span></span>](../../../docs/framework/wcf/endpoints.md)  
 <span data-ttu-id="2997f-118">Toutes les communications avec un service WCF s’effectue via le *points de terminaison* du service.</span><span class="sxs-lookup"><span data-stu-id="2997f-118">All communication with a WCF service occurs through the *endpoints* of the service.</span></span> <span data-ttu-id="2997f-119">Les points de terminaison contiennent le contrat, les informations de configuration spécifiées dans les liaisons, et les adresses qui indiquent où rechercher le service ou comment obtenir des informations sur le service.</span><span class="sxs-lookup"><span data-stu-id="2997f-119">Endpoints contain the contract, the configuration information that is specified in the bindings, and the addresses that indicate where to find the service or where to obtain information about the service.</span></span>  
  
 [<span data-ttu-id="2997f-120">Sécurisation de services</span><span class="sxs-lookup"><span data-stu-id="2997f-120">Securing Services</span></span>](../../../docs/framework/wcf/securing-services.md)  
 <span data-ttu-id="2997f-121">À l’aide de WCF et qui n’existe des mécanismes de sécurité, vous pouvez implémenter la confidentialité, intégrité, l’authentification et autorisation dans n’importe quel service.</span><span class="sxs-lookup"><span data-stu-id="2997f-121">Using WCF and existing security mechanisms, you can implement confidentiality, integrity, authentication, and authorization into any service.</span></span> <span data-ttu-id="2997f-122">Vous pouvez aussi auditer les succès et les défaillances de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="2997f-122">You can also audit for security successes and failures.</span></span>  
  
 [<span data-ttu-id="2997f-123">Création de services pouvant interagir avec le profil Basic Profile 1.1 de WS-I</span><span class="sxs-lookup"><span data-stu-id="2997f-123">Creating WS-I Basic Profile 1.1 Interoperable Services</span></span>](../../../docs/framework/wcf/creating-ws-i-basic-profile-1-1-interoperable-services.md)  
 <span data-ttu-id="2997f-124">Les exigences pour déployer un service interopérable avec les services et les clients sur n’importe quelle autre plateforme ou système d’exploitation sont définies dans la spécification WS-I Basic Profile 1.1.</span><span class="sxs-lookup"><span data-stu-id="2997f-124">The requirements for deploying a service that is interoperable with services and clients on any other platform or operating system are outlined in the WS-I Basic Profile 1.1 specification.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="2997f-125">Référence</span><span class="sxs-lookup"><span data-stu-id="2997f-125">Reference</span></span>  
 <xref:System.ServiceModel>  
  
 <xref:System.ServiceModel.Channels>  
  
 <xref:System.ServiceModel.Description>  
  
## <a name="related-sections"></a><span data-ttu-id="2997f-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2997f-126">Related Sections</span></span>  
 [<span data-ttu-id="2997f-127">Cycle de vie de la programmation de base</span><span class="sxs-lookup"><span data-stu-id="2997f-127">Basic Programming Lifecycle</span></span>](../../../docs/framework/wcf/basic-programming-lifecycle.md)  
  
 [<span data-ttu-id="2997f-128">Conception et implémentation de services</span><span class="sxs-lookup"><span data-stu-id="2997f-128">Designing and Implementing Services</span></span>](../../../docs/framework/wcf/designing-and-implementing-services.md)  
  
 [<span data-ttu-id="2997f-129">Hébergement de services</span><span class="sxs-lookup"><span data-stu-id="2997f-129">Hosting Services</span></span>](../../../docs/framework/wcf/hosting-services.md)  
  
 [<span data-ttu-id="2997f-130">Génération de clients</span><span class="sxs-lookup"><span data-stu-id="2997f-130">Building Clients</span></span>](../../../docs/framework/wcf/building-clients.md)  
  
 [<span data-ttu-id="2997f-131">Introduction à l'extensibilité</span><span class="sxs-lookup"><span data-stu-id="2997f-131">Introduction to Extensibility</span></span>](../../../docs/framework/wcf/introduction-to-extensibility.md)  
  
 [<span data-ttu-id="2997f-132">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="2997f-132">Administration and Diagnostics</span></span>](../../../docs/framework/wcf/diagnostics/index.md)  
  
## <a name="see-also"></a><span data-ttu-id="2997f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2997f-133">See also</span></span>

- [<span data-ttu-id="2997f-134">Programmation WCF de base</span><span class="sxs-lookup"><span data-stu-id="2997f-134">Basic WCF Programming</span></span>](../../../docs/framework/wcf/basic-wcf-programming.md)
- [<span data-ttu-id="2997f-135">Vue d'ensemble conceptuelle</span><span class="sxs-lookup"><span data-stu-id="2997f-135">Conceptual Overview</span></span>](../../../docs/framework/wcf/conceptual-overview.md)
- [<span data-ttu-id="2997f-136">Informations détaillées sur les fonctionnalités de WCF</span><span class="sxs-lookup"><span data-stu-id="2997f-136">WCF Feature Details</span></span>](../../../docs/framework/wcf/feature-details/index.md)
