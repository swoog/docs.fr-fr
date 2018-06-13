---
title: Intégration à des applications COM
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Communication Foundation, COM integration
- COM [WCF], Windows Communication Foundation integration
- WCF, reusing code
- Windows Communication Foundation, reusing code
- COM [WCF]
- WCF, COM integration
ms.assetid: c98bda3e-6779-419e-8e6d-9aa94053026d
ms.openlocfilehash: 292892ef572bd63fff055aeed88073573fadb934
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33491840"
---
# <a name="integrating-with-com-applications"></a><span data-ttu-id="9535f-102">Intégration à des applications COM</span><span class="sxs-lookup"><span data-stu-id="9535f-102">Integrating with COM Applications</span></span>
<span data-ttu-id="9535f-103">Les services Windows Communication Foundation (WCF) peuvent être intégrés directement dans votre code existant à l’aide du moniker de service WCF.</span><span class="sxs-lookup"><span data-stu-id="9535f-103">Windows Communication Foundation (WCF) services can be integrated directly into your existing code by using the WCF service moniker.</span></span> <span data-ttu-id="9535f-104">Le moniker de service peut être utilisé à partir d'une large gamme d'environnements de développement COM, tels qu'Office VBA, Visual Basic 6.0 ou Visual C++ 6.0.</span><span class="sxs-lookup"><span data-stu-id="9535f-104">The service moniker can be used from a wide range of COM-based development environments, such as Office VBA, Visual Basic 6.0, or Visual C++ 6.0.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="9535f-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9535f-105">In This Section</span></span>  
 [<span data-ttu-id="9535f-106">Vue d’ensemble de l’intégration à des applications COM</span><span class="sxs-lookup"><span data-stu-id="9535f-106">Integrating with COM Applications Overview</span></span>](../../../../docs/framework/wcf/feature-details/integrating-with-com-applications-overview.md)  
 <span data-ttu-id="9535f-107">Fournit une vue d'ensemble des principales phases du processus d'intégration.</span><span class="sxs-lookup"><span data-stu-id="9535f-107">Gives an overview of the major parts of the integration process.</span></span>  
  
 [<span data-ttu-id="9535f-108">Guide pratique pour inscrire et configurer un moniker de service</span><span class="sxs-lookup"><span data-stu-id="9535f-108">How to: Register and Configure a Service Moniker</span></span>](../../../../docs/framework/wcf/feature-details/how-to-register-and-configure-a-service-moniker.md)  
 <span data-ttu-id="9535f-109">Pour utiliser le moniker de service WCF dans une application COM, inscrivez les types attribués requis avec COM et configurer l’application COM et le moniker avec la configuration de liaison requise.</span><span class="sxs-lookup"><span data-stu-id="9535f-109">To use the WCF service moniker within a COM application, register the required attributed types with COM, and configure the COM application and the moniker with the required binding configuration.</span></span>  
  
 [<span data-ttu-id="9535f-110">Guide pratique pour utiliser le moniker de service Windows Communication Foundation sans inscription</span><span class="sxs-lookup"><span data-stu-id="9535f-110">How to: Use the Windows Communication Foundation Service Moniker without Registration</span></span>](../../../../docs/framework/wcf/feature-details/use-the-wcf-service-moniker-without-registration.md)  
 <span data-ttu-id="9535f-111">Explique comment obtenir la définition du contrat sous la forme d'un document WSDL (Web Services Definition Language) ou à partir d'un point de terminaison WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="9535f-111">Explains how to obtain the definition of the contract in the form of a Web Services Definition Language (WSDL) document or from a WS-MetadataExchange endpoint.</span></span>  
  
 [<span data-ttu-id="9535f-112">Guide pratique pour utiliser un moniker de service avec des contrats WSDL</span><span class="sxs-lookup"><span data-stu-id="9535f-112">How to: Use a Service Moniker with WSDL Contracts</span></span>](../../../../docs/framework/wcf/feature-details/how-to-use-a-service-moniker-with-wsdl-contracts.md)  
 <span data-ttu-id="9535f-113">Décrit comment appeler un exemple WCF à l’aide d’un moniker WCF WSDL.</span><span class="sxs-lookup"><span data-stu-id="9535f-113">Describes how to call a WCF sample using a WCF WSDL moniker.</span></span>  
  
 [<span data-ttu-id="9535f-114">Guide pratique pour utiliser un moniker de service avec des contrats d’échange de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9535f-114">How to: Use a Service Moniker with Metadata Exchange Contracts</span></span>](../../../../docs/framework/wcf/feature-details/how-to-use-a-service-moniker-with-metadata-exchange-contracts.md)  
 <span data-ttu-id="9535f-115">Décrit comment appeler un exemple WCF à l’aide d’un moniker WCF qui spécifie un point de terminaison Mex.</span><span class="sxs-lookup"><span data-stu-id="9535f-115">Describes how to call a WCF sample using a WCF moniker that specifies a Mex endpoint.</span></span>  
  
 [<span data-ttu-id="9535f-116">Guide pratique pour spécifier des informations d’identification pour la sécurité des canaux</span><span class="sxs-lookup"><span data-stu-id="9535f-116">How to: Specify Channel Security Credentials</span></span>](../../../../docs/framework/wcf/feature-details/how-to-specify-channel-security-credentials.md)  
 <span data-ttu-id="9535f-117">Le moniker de service WCF prend en charge la `IChannelCredentials` interface qui autorise une plage d’autres méthodes permettant de spécifier les informations d’identification de canal.</span><span class="sxs-lookup"><span data-stu-id="9535f-117">The WCF service moniker supports the `IChannelCredentials` interface that allows a range of alternate methods for specifying channel credentials.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="9535f-118">Référence</span><span class="sxs-lookup"><span data-stu-id="9535f-118">Reference</span></span>  
 <xref:System.ServiceModel>  
  
## <a name="see-also"></a><span data-ttu-id="9535f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9535f-119">See Also</span></span>  
 [<span data-ttu-id="9535f-120">Intégration à des applications COM+</span><span class="sxs-lookup"><span data-stu-id="9535f-120">Integrating with COM+ Applications</span></span>](../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)
