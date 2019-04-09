---
title: System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort
ms.date: 03/30/2017
ms.assetid: 155c3203-2e17-4709-b896-2254e22da45e
ms.openlocfilehash: f84cc9336d6cce7d8c477a1feb6caf45b0662177
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59188472"
---
# <a name="systemservicemodeltxcompletionstatuscompletedforasyncabort"></a><span data-ttu-id="da0c5-102">System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort</span><span class="sxs-lookup"><span data-stu-id="da0c5-102">System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort</span></span>
<span data-ttu-id="da0c5-103">La transaction spécifiée pour l’opération indiquée s’est terminée en raison d’un abandon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="da0c5-103">The specified transaction for the specified operation was completed due to asynchronous abort.</span></span>  
  
## <a name="description"></a><span data-ttu-id="da0c5-104">Description</span><span class="sxs-lookup"><span data-stu-id="da0c5-104">Description</span></span>  
 <span data-ttu-id="da0c5-105">La transaction courante a été abandonnée car un autre participant a voté Abort, le délai a été dépassé et une autre erreur s’est produite à l’intérieur du participant d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="da0c5-105">The current transaction was aborted due to another participant voting for Abort, time-outs occurring, or another error inside the participant of a transaction.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="da0c5-106">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="da0c5-106">Troubleshooting</span></span>  
 <span data-ttu-id="da0c5-107">Si cet abandon est inattendu, vérifiez tous les journaux système afin de déterminer la véritable raison de l'abandon.</span><span class="sxs-lookup"><span data-stu-id="da0c5-107">If this abort is unexpected, check all system logs to determine the real reason for the abort.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da0c5-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da0c5-108">See also</span></span>

- [<span data-ttu-id="da0c5-109">Traçage</span><span class="sxs-lookup"><span data-stu-id="da0c5-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="da0c5-110">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="da0c5-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="da0c5-111">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="da0c5-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
