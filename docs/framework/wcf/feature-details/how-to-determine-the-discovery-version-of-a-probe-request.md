---
title: "Procédure : déterminer la version de découverte d'une demande Probe"
ms.date: 03/30/2017
ms.assetid: b3c4e2e2-2957-4074-ae6a-776a5ca84278
ms.openlocfilehash: 356ddd76bdee0698fa446d830791f702af5742b9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54595121"
---
# <a name="how-todetermine-the-discovery-version-of-a-probe-request"></a><span data-ttu-id="50b97-102">Procédure : déterminer la version de découverte d'une demande Probe</span><span class="sxs-lookup"><span data-stu-id="50b97-102">How to:Determine the Discovery Version of a Probe Request</span></span>
<span data-ttu-id="50b97-103">Un proxy de découverte peut exposer plusieurs points de terminaison de découverte à l'aide de différentes versions de découverte.</span><span class="sxs-lookup"><span data-stu-id="50b97-103">A discovery proxy may expose multiple discovery endpoints using different discovery versions.</span></span> <span data-ttu-id="50b97-104">Lorsqu'une demande UDP multicast Probe arrive au proxy, celui-ci doit répondre avec un message de suppression de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="50b97-104">When a UDP multicast Probe request arrives at the proxy the proxy should respond with a multicast suppression message.</span></span> <span data-ttu-id="50b97-105">Pour cela, il doit connaître la version de découverte de la demande.</span><span class="sxs-lookup"><span data-stu-id="50b97-105">In order to do this it would have to know the discovery version of the request.</span></span>  
  
### <a name="to-determine-the-discovery-version-of-a-probe-request"></a><span data-ttu-id="50b97-106">Pour déterminer la version de découverte d'une demande Probe</span><span class="sxs-lookup"><span data-stu-id="50b97-106">To Determine the Discovery Version of a Probe Request</span></span>  
  
1.  <span data-ttu-id="50b97-107">Dans la méthode qui répond à une demande Probe (par exemple <xref:System.ServiceModel.Discovery.DiscoveryProxy.OnBeginFind%2A>) utilisez la propriété <xref:System.ServiceModel.OperationContext.Current%2A> statique pour rechercher un <xref:System.ServiceModel.Discovery.DiscoveryOperationContextExtension> comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="50b97-107">In the method that responds to a Probe request (for example <xref:System.ServiceModel.Discovery.DiscoveryProxy.OnBeginFind%2A>) use the static <xref:System.ServiceModel.OperationContext.Current%2A> property to search for a <xref:System.ServiceModel.Discovery.DiscoveryOperationContextExtension> as shown in the following code.</span></span>  
  
    ```  
    DiscoveryOperationContextExtension doce = OperationContext.Current.Extensions.Find<DiscoveryOperationContextExtension>();  
    // Access the discovery version from the DiscoveryOperationContextExtension  
    doce.DiscoveryVersion;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="50b97-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50b97-108">See also</span></span>

- <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion%2A>
- [<span data-ttu-id="50b97-109">Implémentation d’un proxy de découverte</span><span class="sxs-lookup"><span data-stu-id="50b97-109">Implementing a Discovery Proxy</span></span>](../../../../docs/framework/wcf/feature-details/implementing-a-discovery-proxy.md)
