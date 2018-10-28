---
title: Sécurisation des services et des clients
ms.date: 03/30/2017
helpviewer_keywords:
- message security [WCF]
ms.assetid: e681f3bd-0c09-4a58-b0e4-0ecbdf1aa6c7
ms.openlocfilehash: 05dc9c810d2e8ba64c4dcf21d83e91f8a61225a1
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50190877"
---
# <a name="securing-services-and-clients"></a><span data-ttu-id="45c26-102">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="45c26-102">Securing Services and Clients</span></span>
<span data-ttu-id="45c26-103">Les informations contenues dans cette section se concentre sur la programmation de la sécurité dans Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="45c26-103">The information in this section focuses on programming security in Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="45c26-104">En général, l’opération inclut la sélection d’une liaison appropriée fournie par le système, la définition des propriétés de l’élément de sécurité, puis la définition des propriétés des comportements du service qui déterminent la manière dont les informations d’identification sont récupérées pour être utilisées par le service ou le client.</span><span class="sxs-lookup"><span data-stu-id="45c26-104">Generally, this includes selecting an appropriate system-provided binding, setting the properties of the security element, and then setting properties of the service behaviors that govern how credentials are retrieved for use by either the service or the client.</span></span> <span data-ttu-id="45c26-105">Ces techniques couvrent les exigences de sécurité de la plupart des utilisateurs pour la plupart des scénarios, comme indiqué dans [scénarios de sécurité courants](../../../../docs/framework/wcf/feature-details/common-security-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="45c26-105">These techniques cover the security requirements of most users for most scenarios, as shown in [Common Security Scenarios](../../../../docs/framework/wcf/feature-details/common-security-scenarios.md).</span></span> <span data-ttu-id="45c26-106">Si votre scénario requiert des fonctionnalités supplémentaires, consultez tout d’abord [fonctionnalités de sécurité avec les liaisons personnalisées](../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md); si une solution n’est pas évident, consultez [extension de sécurité](../../../../docs/framework/wcf/extending/extending-security.md).</span><span class="sxs-lookup"><span data-stu-id="45c26-106">If your scenario requires more capabilities, first see [Security Capabilities with Custom Bindings](../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md); if a solution is not apparent, see [Extending Security](../../../../docs/framework/wcf/extending/extending-security.md).</span></span> <span data-ttu-id="45c26-107">Si vous créez (ou interopération avec) un système qui utilise des revendications riches, consultez les rubriques de [autorisation](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md).</span><span class="sxs-lookup"><span data-stu-id="45c26-107">If you are creating (or interoperating with) a system that uses rich claims, see the topics in [Authorization](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="45c26-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="45c26-108">In This Section</span></span>  
 [<span data-ttu-id="45c26-109">Programmation de la sécurité dans WCF</span><span class="sxs-lookup"><span data-stu-id="45c26-109">Programming WCF Security</span></span>](../../../../docs/framework/wcf/feature-details/programming-wcf-security.md)  
 <span data-ttu-id="45c26-110">Vue d'ensemble du modèle de programmation utilisé pour sécuriser des messages.</span><span class="sxs-lookup"><span data-stu-id="45c26-110">An overview of the programming model used to secure messages.</span></span>  
  
 [<span data-ttu-id="45c26-111">Vue d’ensemble de la sécurité de transport</span><span class="sxs-lookup"><span data-stu-id="45c26-111">Transport Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/transport-security-overview.md)  
 <span data-ttu-id="45c26-112">Vue d'ensemble de la sécurisation des messages par le biais de la couche transport.</span><span class="sxs-lookup"><span data-stu-id="45c26-112">An overview of how to secure messages through the transport layer.</span></span>  
  
 [<span data-ttu-id="45c26-113">Sécurité de message</span><span class="sxs-lookup"><span data-stu-id="45c26-113">Message Security</span></span>](../../../../docs/framework/wcf/feature-details/message-security-in-wcf.md)  
 <span data-ttu-id="45c26-114">Récapitule les raisons d’utiliser la sécurité au niveau du message dans Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="45c26-114">Summarizes reasons for using message-level security in Windows Communication Foundation (WCF).</span></span>  
  
 [<span data-ttu-id="45c26-115">Sessions sécurisées</span><span class="sxs-lookup"><span data-stu-id="45c26-115">Secure Sessions</span></span>](../../../../docs/framework/wcf/feature-details/secure-sessions.md)  
 <span data-ttu-id="45c26-116">Présentation des considérations nécessaires lors de la sécurisation d’une session WCF.</span><span class="sxs-lookup"><span data-stu-id="45c26-116">A discussion of the considerations required when securing a WCF session.</span></span>  
  
 [<span data-ttu-id="45c26-117">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="45c26-117">Working with Certificates</span></span>](../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 <span data-ttu-id="45c26-118">Explication de quelques-unes des tâches courantes requises lors de l’utilisation de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="45c26-118">An explanation of some of the common tasks required when using X.509 certificates.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="45c26-119">Référence</span><span class="sxs-lookup"><span data-stu-id="45c26-119">Reference</span></span>  
 <xref:System.ServiceModel>  
  
 <xref:System.ServiceModel.Channels>  
  
 <xref:System.ServiceModel.Security>  
  
## <a name="related-sections"></a><span data-ttu-id="45c26-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45c26-120">Related Sections</span></span>  
 [<span data-ttu-id="45c26-121">Concepts relatifs à la sécurité</span><span class="sxs-lookup"><span data-stu-id="45c26-121">Security Concepts</span></span>](../../../../docs/framework/wcf/feature-details/security-concepts.md)  
  
 [<span data-ttu-id="45c26-122">Extension de la sécurité</span><span class="sxs-lookup"><span data-stu-id="45c26-122">Extending Security</span></span>](../../../../docs/framework/wcf/extending/extending-security.md)  
  
 [<span data-ttu-id="45c26-123">Scénarios de sécurité courants</span><span class="sxs-lookup"><span data-stu-id="45c26-123">Common Security Scenarios</span></span>](../../../../docs/framework/wcf/feature-details/common-security-scenarios.md)  
  
 [<span data-ttu-id="45c26-124">Liaisons et sécurité</span><span class="sxs-lookup"><span data-stu-id="45c26-124">Bindings and Security</span></span>](../../../../docs/framework/wcf/feature-details/bindings-and-security.md)  
  
 [<span data-ttu-id="45c26-125">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="45c26-125">Security Capabilities with Custom Bindings</span></span>](../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)  
  
 [<span data-ttu-id="45c26-126">Extension de la sécurité</span><span class="sxs-lookup"><span data-stu-id="45c26-126">Extending Security</span></span>](../../../../docs/framework/wcf/extending/extending-security.md)  
  
 [<span data-ttu-id="45c26-127">Autorisation</span><span class="sxs-lookup"><span data-stu-id="45c26-127">Authorization</span></span>](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md)  
  
## <a name="see-also"></a><span data-ttu-id="45c26-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45c26-128">See Also</span></span>  
 [<span data-ttu-id="45c26-129">Programmation WCF de base</span><span class="sxs-lookup"><span data-stu-id="45c26-129">Basic WCF Programming</span></span>](../../../../docs/framework/wcf/basic-wcf-programming.md)  
 [<span data-ttu-id="45c26-130">Modèle de sécurité pour Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="45c26-130">Security Model for Windows Server App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
