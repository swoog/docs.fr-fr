---
title: System.ServiceModel.TxCompletionStatusAbortedOnSessionClose
ms.date: 03/30/2017
ms.assetid: 7e142e9d-e81b-4309-974a-02e9cc064ea0
ms.openlocfilehash: 7b1f6a2f4a344b566c76d0095942b84a8a4e76f6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61991625"
---
# <a name="systemservicemodeltxcompletionstatusabortedonsessionclose"></a><span data-ttu-id="20602-102">System.ServiceModel.TxCompletionStatusAbortedOnSessionClose</span><span class="sxs-lookup"><span data-stu-id="20602-102">System.ServiceModel.TxCompletionStatusAbortedOnSessionClose</span></span>
<span data-ttu-id="20602-103">La transaction spécifiée a été abandonnée car elle était inachevée lorsque la session a été fermée et le OperationBehaviorAttribute TransactionAutoCompleteOnSessionClose a été défini à false.</span><span class="sxs-lookup"><span data-stu-id="20602-103">The specified transaction was aborted because it was uncompleted when the session was closed and the TransactionAutoCompleteOnSessionClose OperationBehaviorAttribute was set to false.</span></span>  
  
## <a name="description"></a><span data-ttu-id="20602-104">Description</span><span class="sxs-lookup"><span data-stu-id="20602-104">Description</span></span>  
 <span data-ttu-id="20602-105">Suivi si la session active actuelle a été fermée, que la transaction n'a pas été achevée et que TransactionAutoCompleteOnSessionClose a la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="20602-105">Traced if the current active session was closed, and the transaction was not completed, and TransactionAutoCompleteOnSessionClose is set to `false`.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="20602-106">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="20602-106">Troubleshooting</span></span>  
 <span data-ttu-id="20602-107">Cette trace indique un bogue d'application potentiel qui doit être étudié.</span><span class="sxs-lookup"><span data-stu-id="20602-107">This trace indicates a potential application bug that should be investigated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20602-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20602-108">See also</span></span>

- [<span data-ttu-id="20602-109">Suivi</span><span class="sxs-lookup"><span data-stu-id="20602-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="20602-110">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="20602-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="20602-111">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="20602-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
