---
title: System.ServiceModel.Channels.FailedAcceptFromPool
ms.date: 03/30/2017
ms.assetid: d535b1b5-ee58-45e8-b400-7d9570f4eb9a
ms.openlocfilehash: de0bdd9e5ab922b09249bf550fde745042be8e58
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59156479"
---
# <a name="systemservicemodelchannelsfailedacceptfrompool"></a><span data-ttu-id="8e404-102">System.ServiceModel.Channels.FailedAcceptFromPool</span><span class="sxs-lookup"><span data-stu-id="8e404-102">System.ServiceModel.Channels.FailedAcceptFromPool</span></span>
<span data-ttu-id="8e404-103">Échec de la tentative de réutilisation d'une connexion en groupe.</span><span class="sxs-lookup"><span data-stu-id="8e404-103">An attempt to reuse a pooled connection failed.</span></span> <span data-ttu-id="8e404-104">Une autre tentative est effectuée dans le délai d'attente spécifié.</span><span class="sxs-lookup"><span data-stu-id="8e404-104">Another attempt is made within the specified timeout period.</span></span>  
  
## <a name="description"></a><span data-ttu-id="8e404-105">Description</span><span class="sxs-lookup"><span data-stu-id="8e404-105">Description</span></span>  
 <span data-ttu-id="8e404-106">Ce suivi d'informations indique qu'une erreur s'est produite lors de la tentative de réutilisation d'une connexion en groupe.</span><span class="sxs-lookup"><span data-stu-id="8e404-106">This informational trace indicates that an error has occurred while attempting to reuse a pooled connection.</span></span> <span data-ttu-id="8e404-107">Cela peut se produire si la connexion en groupe n'est pas compatible, prête ou toujours active.</span><span class="sxs-lookup"><span data-stu-id="8e404-107">This could happen because the pooled connection was not compatible, ready, or still active.</span></span> <span data-ttu-id="8e404-108">Toute tentative supplémentaire pour réutiliser une autre connexion en groupe est effectuée au cours d'un délai d'expiration donné et une nouvelle connexion est créée si aucune connexion utilisable n'est trouvée.</span><span class="sxs-lookup"><span data-stu-id="8e404-108">Additional attempts to reuse other pooled connection are made within a given timeout and a new connection is created in case no usable connections are found.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8e404-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e404-109">See also</span></span>

- [<span data-ttu-id="8e404-110">Suivi</span><span class="sxs-lookup"><span data-stu-id="8e404-110">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="8e404-111">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="8e404-111">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="8e404-112">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="8e404-112">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
