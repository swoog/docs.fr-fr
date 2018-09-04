---
title: Définition des services de données WCF
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, configuring
ms.assetid: 05006ff3-02dc-410e-831e-54ec3e7e24ef
ms.openlocfilehash: c0c9010a71877d2c9757a2c9cf2d5c1fec8aedf7
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43515535"
---
# <a name="defining-wcf-data-services"></a><span data-ttu-id="dea8e-102">Définition des services de données WCF</span><span class="sxs-lookup"><span data-stu-id="dea8e-102">Defining WCF Data Services</span></span>

<span data-ttu-id="dea8e-103">Cette section décrit comment créer et configurer les Services de données WCF pour exposer des données sous un [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] flux.</span><span class="sxs-lookup"><span data-stu-id="dea8e-103">This section describes how to create and configure WCF Data Services to expose data as an [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] feed.</span></span> <span data-ttu-id="dea8e-104">Pour plus d’informations sur les étapes de base requises pour créer un service de données, consultez [exposer vos données en tant que Service](../../../../docs/framework/data/wcf/exposing-your-data-as-a-service-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="dea8e-104">For more information about the basic steps required to create a data service, see [Exposing Your Data as a Service](../../../../docs/framework/data/wcf/exposing-your-data-as-a-service-wcf-data-services.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dea8e-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="dea8e-105">In This Section</span></span>

 [<span data-ttu-id="dea8e-106">Configuration du service de données</span><span class="sxs-lookup"><span data-stu-id="dea8e-106">Configuring the Data Service</span></span>](../../../../docs/framework/data/wcf/configuring-the-data-service-wcf-data-services.md)

 <span data-ttu-id="dea8e-107">Décrit les options de configuration de service de données fournies par WCF Data Services.</span><span class="sxs-lookup"><span data-stu-id="dea8e-107">Describes the data service configuration options provided by WCF Data Services.</span></span>

 [<span data-ttu-id="dea8e-108">Fournisseurs de services de données</span><span class="sxs-lookup"><span data-stu-id="dea8e-108">Data Services Providers</span></span>](../../../../docs/framework/data/wcf/data-services-providers-wcf-data-services.md)

 <span data-ttu-id="dea8e-109">Décrit les modèles de fournisseur pour l'exposition de données sous la forme d'un service de données.</span><span class="sxs-lookup"><span data-stu-id="dea8e-109">Describes the provider models for exposing data as a data service.</span></span>

 [<span data-ttu-id="dea8e-110">Opérations de service</span><span class="sxs-lookup"><span data-stu-id="dea8e-110">Service Operations</span></span>](../../../../docs/framework/data/wcf/service-operations-wcf-data-services.md)

 <span data-ttu-id="dea8e-111">Décrit comment définir des opérations de service qui exposent des méthodes sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="dea8e-111">Describes how to define service operations that expose methods on the server.</span></span>

 [<span data-ttu-id="dea8e-112">Personnalisation des flux</span><span class="sxs-lookup"><span data-stu-id="dea8e-112">Feed Customization</span></span>](../../../../docs/framework/data/wcf/feed-customization-wcf-data-services.md)

 <span data-ttu-id="dea8e-113">Décrit comment créer un mappage entre les entités du modèle de données défini par le fournisseur de services de données et les éléments du flux de données.</span><span class="sxs-lookup"><span data-stu-id="dea8e-113">Describes how to create a mapping between entities in the data model defined by the data service provider and elements in the data feed.</span></span>

 [<span data-ttu-id="dea8e-114">Intercepteurs</span><span class="sxs-lookup"><span data-stu-id="dea8e-114">Interceptors</span></span>](../../../../docs/framework/data/wcf/interceptors-wcf-data-services.md)

 <span data-ttu-id="dea8e-115">Décrit comment définir des méthodes d'intercepteur pour appliquer une logique métier personnalisée sur des requêtes au service de données.</span><span class="sxs-lookup"><span data-stu-id="dea8e-115">Describes how to define interceptor methods to perform custom business logic on requests to the data service.</span></span>

 [<span data-ttu-id="dea8e-116">Développement et déploiement de WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="dea8e-116">Developing and Deploying WCF Data Services</span></span>](../../../../docs/framework/data/wcf/developing-and-deploying-wcf-data-services.md)

 <span data-ttu-id="dea8e-117">Explique comment développer et déployer un service de données à l'aide de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="dea8e-117">Describes how to develop and deploy a data service by using Visual Studio.</span></span>

 [<span data-ttu-id="dea8e-118">Sécurisation de WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="dea8e-118">Securing WCF Data Services</span></span>](../../../../docs/framework/data/wcf/securing-wcf-data-services.md)

 <span data-ttu-id="dea8e-119">Décrit l'authentification et l'autorisation du service de données et fournit des considérations sur la sécurité.</span><span class="sxs-lookup"><span data-stu-id="dea8e-119">Describes authentication and authorization for the data service and other security considerations.</span></span>

 [<span data-ttu-id="dea8e-120">Hébergement du service de données</span><span class="sxs-lookup"><span data-stu-id="dea8e-120">Hosting the Data Service</span></span>](../../../../docs/framework/data/wcf/hosting-the-data-service-wcf-data-services.md)

 <span data-ttu-id="dea8e-121">Décrit comment sélectionner un hôte pour votre service de données.</span><span class="sxs-lookup"><span data-stu-id="dea8e-121">Describes how to select a host for your data service.</span></span>

 [<span data-ttu-id="dea8e-122">Gestion de version d’un service de données</span><span class="sxs-lookup"><span data-stu-id="dea8e-122">Data Service Versioning</span></span>](../../../../docs/framework/data/wcf/data-service-versioning-wcf-data-services.md)

 <span data-ttu-id="dea8e-123">Décrit comment travailler avec différentes versions d’OData.</span><span class="sxs-lookup"><span data-stu-id="dea8e-123">Describes how to work with different versions of the OData.</span></span>

 [<span data-ttu-id="dea8e-124">Détails relatifs à l’implémentation du protocole WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="dea8e-124">WCF Data Services Protocol Implementation Details</span></span>](../../../../docs/framework/data/wcf/wcf-data-services-protocol-implementation-details.md)

 <span data-ttu-id="dea8e-125">Décrit les fonctionnalités facultatives du protocole OData qui ne sont pas actuellement implémentées par WCF Data Services.</span><span class="sxs-lookup"><span data-stu-id="dea8e-125">Describes optional functionalities of the OData protocol that are not currently implemented by WCF Data Services.</span></span>

## <a name="see-also"></a><span data-ttu-id="dea8e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dea8e-126">See Also</span></span>

- [<span data-ttu-id="dea8e-127">Bibliothèque cliente WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="dea8e-127">WCF Data Services Client Library</span></span>](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)
- [<span data-ttu-id="dea8e-128">Accès aux ressources d’un service de données</span><span class="sxs-lookup"><span data-stu-id="dea8e-128">Accessing Data Service Resources</span></span>](../../../../docs/framework/data/wcf/accessing-data-service-resources-wcf-data-services.md)
- [<span data-ttu-id="dea8e-129">Prise en main</span><span class="sxs-lookup"><span data-stu-id="dea8e-129">Getting Started</span></span>](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md)
