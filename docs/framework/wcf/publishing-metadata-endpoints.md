---
title: Publication de points de terminaison de métadonnées
ms.date: 03/30/2017
ms.assetid: 29cd8a60-dfb7-460c-bf5a-c2b31b782671
ms.openlocfilehash: 143a46ce18a0d9dee89bbbffac9be9a467e951df
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59121730"
---
# <a name="publishing-metadata-endpoints"></a><span data-ttu-id="53361-102">Publication de points de terminaison de métadonnées</span><span class="sxs-lookup"><span data-stu-id="53361-102">Publishing Metadata Endpoints</span></span>
<span data-ttu-id="53361-103">Services Windows Communication Foundation (WCF) publient les métadonnées en publiant un ou plusieurs points de terminaison de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="53361-103">Windows Communication Foundation (WCF) services publish metadata by publishing one or more metadata endpoints.</span></span> <span data-ttu-id="53361-104">La publication de métadonnées de service permet d'accéder à celles-ci à l'aide de protocoles standardisés, tels que WS-MetadataExchange (MEX) et les requêtes HTTP/GET.</span><span class="sxs-lookup"><span data-stu-id="53361-104">Publishing service metadata makes the metadata available using standardized protocols, such as WS-MetadataExchange (MEX) and HTTP/GET requests.</span></span> <span data-ttu-id="53361-105">Les points de terminaison de métadonnées sont semblables aux autres points de terminaison de service dans le sens où ils ont une adresse, une liaison et un contrat, et qu’ils peuvent être ajoutés à un hôte de service via la configuration ou dans du code.</span><span class="sxs-lookup"><span data-stu-id="53361-105">Metadata endpoints are similar to other service endpoints in that they have an address, a binding, and a contract, and they can be added to a service host through configuration or in code.</span></span> <span data-ttu-id="53361-106">Pour activer la publication de points de terminaison de métadonnées, vous devez ajouter le comportement de service <xref:System.ServiceModel.Description.ServiceMetadataBehavior> au service.</span><span class="sxs-lookup"><span data-stu-id="53361-106">To enable publishing metadata endpoints, you must add the <xref:System.ServiceModel.Description.ServiceMetadataBehavior> service behavior to the service.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="53361-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="53361-107">In This Section</span></span>  
 [<span data-ttu-id="53361-108">Procédure : publier des métadonnées pour un service à l’aide d’un fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="53361-108">How to: Publish Metadata for a Service Using a Configuration File</span></span>](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)  
 <span data-ttu-id="53361-109">Montre comment configurer un service WCF pour publier les métadonnées afin que les clients peuvent récupérer les métadonnées à l’aide d’un échange WS-MetadataExchange ou une requête HTTP/GET en utilisant le `?wsdl` chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="53361-109">Demonstrates how to configure a WCF service to publish metadata so that clients can retrieve the metadata using a WS-MetadataExchange or an HTTP/GET request using the `?wsdl` query string.</span></span>  
  
 [<span data-ttu-id="53361-110">Procédure : publier des métadonnées pour un service à l’aide de code</span><span class="sxs-lookup"><span data-stu-id="53361-110">How to: Publish Metadata for a Service Using Code</span></span>](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-code.md)  
 <span data-ttu-id="53361-111">Montre comment activer la publication de métadonnées pour un service WCF dans le code afin que les clients peuvent récupérer les métadonnées à l’aide d’un échange WS-MetadataExchange ou une requête HTTP/GET en utilisant le `?wsdl` chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="53361-111">Demonstrates how to enable metadata publishing for a WCF service in code so that clients can retrieve the metadata using a WS-MetadataExchange or an HTTP/GET request using the `?wsdl` query string.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53361-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53361-112">See also</span></span>

- [<span data-ttu-id="53361-113">Publication de métadonnées</span><span class="sxs-lookup"><span data-stu-id="53361-113">Publishing Metadata</span></span>](../../../docs/framework/wcf/feature-details/publishing-metadata.md)
