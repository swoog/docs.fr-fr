---
title: Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished
ms.date: 03/30/2017
ms.assetid: 54b677f7-03ad-40f2-9c5d-297a8ad9bf90
ms.openlocfilehash: 85b8cc4e5044cc7c87ea784e09c160cc527dddaa
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33473530"
---
# <a name="microsofttransactionstransactionbridgeparticipantstatemachinefinished"></a><span data-ttu-id="a9dd3-102">Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished</span><span class="sxs-lookup"><span data-stu-id="a9dd3-102">Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished</span></span>
<span data-ttu-id="a9dd3-103">La machine à états pour un enrôlement de participant est passée à l'état Finished.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-103">The state machine for a participant enlistment entered the finished state.</span></span>  
  
## <a name="description"></a><span data-ttu-id="a9dd3-104">Description</span><span class="sxs-lookup"><span data-stu-id="a9dd3-104">Description</span></span>  
 <span data-ttu-id="a9dd3-105">Suivi lorsqu'un enrôlement de participant subalterne a terminé le traitement 2PC.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-105">Traced when a subordinate participant enlistment has completed 2pc processing.</span></span> <span data-ttu-id="a9dd3-106">Le résultat peut être Committed ou Aborted.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-106">The outcome for the enlistment can be Committed or Aborted.</span></span> <span data-ttu-id="a9dd3-107">Il est également suivi lorsque les participants votent ReadOnly pendant la préparation.</span><span class="sxs-lookup"><span data-stu-id="a9dd3-107">It is also traced if any participant votes ReadOnly during Prepare.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9dd3-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9dd3-108">See Also</span></span>  
 [<span data-ttu-id="a9dd3-109">Suivi</span><span class="sxs-lookup"><span data-stu-id="a9dd3-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [<span data-ttu-id="a9dd3-110">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="a9dd3-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [<span data-ttu-id="a9dd3-111">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="a9dd3-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
