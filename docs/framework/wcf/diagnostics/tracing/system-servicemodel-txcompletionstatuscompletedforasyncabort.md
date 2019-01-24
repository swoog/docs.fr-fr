---
title: System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort
ms.date: 03/30/2017
ms.assetid: 155c3203-2e17-4709-b896-2254e22da45e
ms.openlocfilehash: 3d43524b7141a134b9560e92da66ef2349b8119a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631283"
---
# <a name="systemservicemodeltxcompletionstatuscompletedforasyncabort"></a><span data-ttu-id="b4e3d-102">System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort</span><span class="sxs-lookup"><span data-stu-id="b4e3d-102">System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort</span></span>
<span data-ttu-id="b4e3d-103">La transaction spécifiée pour l’opération indiquée s’est terminée en raison d’un abandon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b4e3d-103">The specified transaction for the specified operation was completed due to asynchronous abort.</span></span>  
  
## <a name="description"></a><span data-ttu-id="b4e3d-104">Description</span><span class="sxs-lookup"><span data-stu-id="b4e3d-104">Description</span></span>  
 <span data-ttu-id="b4e3d-105">La transaction courante a été abandonnée car un autre participant a voté Abort, le délai a été dépassé et une autre erreur s'est produite à l'intérieur du participant d'une transaction.</span><span class="sxs-lookup"><span data-stu-id="b4e3d-105">The current transaction was aborted due to another participant voting for Abort, time-outs occurring, or another error inside the participant of a transaction.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="b4e3d-106">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="b4e3d-106">Troubleshooting</span></span>  
 <span data-ttu-id="b4e3d-107">Si cet abandon est inattendu, vérifiez tous les journaux système afin de déterminer la véritable raison de l'abandon.</span><span class="sxs-lookup"><span data-stu-id="b4e3d-107">If this abort is unexpected, check all system logs to determine the real reason for the abort.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b4e3d-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4e3d-108">See also</span></span>
- [<span data-ttu-id="b4e3d-109">Suivi</span><span class="sxs-lookup"><span data-stu-id="b4e3d-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="b4e3d-110">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="b4e3d-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="b4e3d-111">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="b4e3d-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
