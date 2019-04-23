---
title: System.ServiceModel.TxAsyncAbort
ms.date: 03/30/2017
ms.assetid: bce47ff2-abd0-4b58-8667-ebf1ef3580b8
ms.openlocfilehash: a6989da7b457e819a49d7c27e8732c7f33dc51b8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59133924"
---
# <a name="systemservicemodeltxasyncabort"></a><span data-ttu-id="519a2-102">System.ServiceModel.TxAsyncAbort</span><span class="sxs-lookup"><span data-stu-id="519a2-102">System.ServiceModel.TxAsyncAbort</span></span>
<span data-ttu-id="519a2-103">La transaction spécifiée a été abandonnée de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="519a2-103">The specified transaction was asynchronously aborted.</span></span>  
  
## <a name="description"></a><span data-ttu-id="519a2-104">Description</span><span class="sxs-lookup"><span data-stu-id="519a2-104">Description</span></span>  
 <span data-ttu-id="519a2-105">La transaction courante a été abandonnée car un autre participant a voté Abort, le délai a été dépassé et une autre erreur s’est produite à l’intérieur du participant d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="519a2-105">The current transaction was aborted due to another participant voting for Abort, time-outs occurring, or another error inside the participant of a transaction.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="519a2-106">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="519a2-106">Troubleshooting</span></span>  
 <span data-ttu-id="519a2-107">Vérifiez tous les journaux système si cet abandon est inattendu afin de déterminer la vraie raison de l'abandon.</span><span class="sxs-lookup"><span data-stu-id="519a2-107">Check all system logs if this abort is unexpected to determine the real reason for the abort.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="519a2-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="519a2-108">See also</span></span>

- [<span data-ttu-id="519a2-109">Suivi</span><span class="sxs-lookup"><span data-stu-id="519a2-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="519a2-110">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="519a2-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="519a2-111">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="519a2-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
