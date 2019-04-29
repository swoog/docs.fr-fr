---
title: Intégration d'AJAX et prise en charge de JSON
ms.date: 03/30/2017
helpviewer_keywords:
- AJAX integration and JSON support [WCF]
ms.assetid: 3851a8fc-d861-4ac1-873c-96af0343d3a7
ms.openlocfilehash: a3d9c29f3223624653f2d568bb351d90334a4318
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61781613"
---
# <a name="ajax-integration-and-json-support"></a><span data-ttu-id="883ca-102">Intégration d'AJAX et prise en charge de JSON</span><span class="sxs-lookup"><span data-stu-id="883ca-102">AJAX Integration and JSON Support</span></span>
<span data-ttu-id="883ca-103">La prise en charge de Windows Communication Foundation (WCF) pour ASP.NET Asynchronous JavaScript and XML (AJAX) et le format de données JavaScript Objet Notation (JSON) autoriser les services WCF d’exposer des opérations aux clients AJAX.</span><span class="sxs-lookup"><span data-stu-id="883ca-103">The Windows Communication Foundation (WCF) support for ASP.NET Asynchronous JavaScript and XML (AJAX) and the JavaScript Object Notation (JSON) data format allow WCF services to expose operations to AJAX clients.</span></span> <span data-ttu-id="883ca-104">Clients AJAX sont les pages Web code JavaScript en cours d’exécution et l’accès à ces services WCF à l’aide de requêtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="883ca-104">AJAX clients are Web pages running JavaScript code and accessing these WCF services using HTTP requests.</span></span> <span data-ttu-id="883ca-105">Les rubriques de cette section fournissent des informations sur cette prise en charge et sur la manière de l'implémenter.</span><span class="sxs-lookup"><span data-stu-id="883ca-105">The topics in this section provide information about this support and about how to implement it.</span></span>  
  
 <span data-ttu-id="883ca-106">Pour plus d’informations sur ASP.NET AJAX et son intégration avec ASP.NET 2.0, consultez [vue d’ensemble de ASP.NET AJAX](https://go.microsoft.com/fwlink/?LinkId=96725).</span><span class="sxs-lookup"><span data-stu-id="883ca-106">For more information about ASP.NET AJAX and its integration with ASP.NET 2.0, see [ASP.NET AJAX Overview](https://go.microsoft.com/fwlink/?LinkId=96725).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="883ca-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="883ca-107">In This Section</span></span>  
 [<span data-ttu-id="883ca-108">Création de services WCF pour ASP.NET AJAX</span><span class="sxs-lookup"><span data-stu-id="883ca-108">Creating WCF Services for ASP.NET AJAX</span></span>](../../../../docs/framework/wcf/feature-details/creating-wcf-services-for-aspnet-ajax.md)  
 <span data-ttu-id="883ca-109">Décrit comment un service WCF peut être exposé aux clients AJAX en ajoutant le point de terminaison AJAX approprié soit via la configuration ou à l’aide d’une fabrique d’hôte de service personnalisée pour générer un hôte de service qui configure le point de terminaison AJAX automatiquement.</span><span class="sxs-lookup"><span data-stu-id="883ca-109">Describes how an WCF service can be exposed to AJAX clients by adding the appropriate AJAX endpoint either through configuration or by using a service host factory customized to generate a service host that configures the AJAX endpoint automatically.</span></span>  
  
 [<span data-ttu-id="883ca-110">Création de services WCF AJAX sans ASP.NET</span><span class="sxs-lookup"><span data-stu-id="883ca-110">Creating WCF AJAX Services without ASP.NET</span></span>](../../../../docs/framework/wcf/feature-details/creating-wcf-ajax-services-without-aspnet.md)  
 <span data-ttu-id="883ca-111">Décrit comment créer un service WCF sans l’aide d’ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="883ca-111">Describes how to create an WCF service without using ASP.NET.</span></span>  
  
 [<span data-ttu-id="883ca-112">Prise en charge du format JSON et d’autres formats de transfert de données</span><span class="sxs-lookup"><span data-stu-id="883ca-112">Support for JSON and Other Data Transfer Formats</span></span>](../../../../docs/framework/wcf/feature-details/support-for-json-and-other-data-transfer-formats.md)  
 <span data-ttu-id="883ca-113">Décrit la prise en charge du format JSON utilisé en général (à la place de XML) pour la messagerie avec les services ASP.NET AJAX.</span><span class="sxs-lookup"><span data-stu-id="883ca-113">Describes the support of the JSON format typically used (instead of XML) for messaging with ASP.NET AJAX services.</span></span>  
  
 [<span data-ttu-id="883ca-114">Guide pratique pour Migrer les Services Web ASP.NET compatibles AJAX vers WCF</span><span class="sxs-lookup"><span data-stu-id="883ca-114">How to: Migrate AJAX-Enabled ASP.NET Web Services to WCF</span></span>](../../../../docs/framework/wcf/feature-details/how-to-migrate-ajax-enabled-aspnet-web-services-to-wcf.md)  
 <span data-ttu-id="883ca-115">Décrit comment migrer un service Web ASP.NET compatibles AJAX vers un service Web WCF.</span><span class="sxs-lookup"><span data-stu-id="883ca-115">Describes how to migrate an AJAX-enabled ASP.NET Web service to a WCF Web service.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="883ca-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="883ca-116">See also</span></span>

- <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory>
- [<span data-ttu-id="883ca-117">Modèle de programmation HTTP web WCF</span><span class="sxs-lookup"><span data-stu-id="883ca-117">WCF Web HTTP Programming Model</span></span>](../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md)
