---
title: System.ServiceModel.MessageProcessingPaused
ms.date: 03/30/2017
ms.assetid: 36b5302a-93cc-478a-9bb2-8a1601fba1df
ms.openlocfilehash: ac1dacef94d6446aa407e4a390b9561d033af1bb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59087468"
---
# <a name="systemservicemodelmessageprocessingpaused"></a><span data-ttu-id="e1fb2-102">System.ServiceModel.MessageProcessingPaused</span><span class="sxs-lookup"><span data-stu-id="e1fb2-102">System.ServiceModel.MessageProcessingPaused</span></span>
<span data-ttu-id="e1fb2-103">System.ServiceModel.MessageProcessingPaused</span><span class="sxs-lookup"><span data-stu-id="e1fb2-103">System.ServiceModel.MessageProcessingPaused</span></span>  
  
## <a name="description"></a><span data-ttu-id="e1fb2-104">Description</span><span class="sxs-lookup"><span data-stu-id="e1fb2-104">Description</span></span>  
 <span data-ttu-id="e1fb2-105">Les threads ont été basculés pendant le traitement d'un message.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-105">The threads were switched while processing a message.</span></span>  
  
 <span data-ttu-id="e1fb2-106">Le traitement des messages peut être suspendu pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1fb2-106">Message processing can be paused by the following reasons:</span></span>  
  
-   <span data-ttu-id="e1fb2-107">ConcurrencyMode est unique ou réentrant, et le service traite un autre message.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-107">ConcurrencyMode is single or reentrant, and the service is processing another message.</span></span>  
  
-   <span data-ttu-id="e1fb2-108">La transaction est activée et le service traite une autre transaction.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-108">Transaction is enabled and the service is processing another transaction.</span></span>  
  
-   <span data-ttu-id="e1fb2-109">Le contexte de synchronisation n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="e1fb2-109">Synchronization context is not current.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1fb2-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1fb2-110">See also</span></span>

- [<span data-ttu-id="e1fb2-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="e1fb2-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="e1fb2-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="e1fb2-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="e1fb2-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="e1fb2-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
