---
title: System.ServiceModel.MessageProcessingPaused
ms.date: 03/30/2017
ms.assetid: 36b5302a-93cc-478a-9bb2-8a1601fba1df
ms.openlocfilehash: ac1dacef94d6446aa407e4a390b9561d033af1bb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61927021"
---
# <a name="systemservicemodelmessageprocessingpaused"></a><span data-ttu-id="5e9d8-102">System.ServiceModel.MessageProcessingPaused</span><span class="sxs-lookup"><span data-stu-id="5e9d8-102">System.ServiceModel.MessageProcessingPaused</span></span>
<span data-ttu-id="5e9d8-103">System.ServiceModel.MessageProcessingPaused</span><span class="sxs-lookup"><span data-stu-id="5e9d8-103">System.ServiceModel.MessageProcessingPaused</span></span>  
  
## <a name="description"></a><span data-ttu-id="5e9d8-104">Description</span><span class="sxs-lookup"><span data-stu-id="5e9d8-104">Description</span></span>  
 <span data-ttu-id="5e9d8-105">Les threads ont été basculés pendant le traitement d'un message.</span><span class="sxs-lookup"><span data-stu-id="5e9d8-105">The threads were switched while processing a message.</span></span>  
  
 <span data-ttu-id="5e9d8-106">Le traitement des messages peut être suspendu pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="5e9d8-106">Message processing can be paused by the following reasons:</span></span>  
  
- <span data-ttu-id="5e9d8-107">ConcurrencyMode est unique ou réentrant, et le service traite un autre message.</span><span class="sxs-lookup"><span data-stu-id="5e9d8-107">ConcurrencyMode is single or reentrant, and the service is processing another message.</span></span>  
  
- <span data-ttu-id="5e9d8-108">La transaction est activée et le service traite une autre transaction.</span><span class="sxs-lookup"><span data-stu-id="5e9d8-108">Transaction is enabled and the service is processing another transaction.</span></span>  
  
- <span data-ttu-id="5e9d8-109">Le contexte de synchronisation n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="5e9d8-109">Synchronization context is not current.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e9d8-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e9d8-110">See also</span></span>

- [<span data-ttu-id="5e9d8-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="5e9d8-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="5e9d8-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="5e9d8-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="5e9d8-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="5e9d8-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
