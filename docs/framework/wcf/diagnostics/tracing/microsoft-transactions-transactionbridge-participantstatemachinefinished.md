---
title: Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished
ms.date: 03/30/2017
ms.assetid: 54b677f7-03ad-40f2-9c5d-297a8ad9bf90
ms.openlocfilehash: 56eb40d4e8b2580ba094e67552872cf558c8a617
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642293"
---
# <a name="microsofttransactionstransactionbridgeparticipantstatemachinefinished"></a><span data-ttu-id="f083b-102">Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished</span><span class="sxs-lookup"><span data-stu-id="f083b-102">Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished</span></span>
<span data-ttu-id="f083b-103">La machine à états pour un enrôlement de participant est passée à l'état Finished.</span><span class="sxs-lookup"><span data-stu-id="f083b-103">The state machine for a participant enlistment entered the finished state.</span></span>  
  
## <a name="description"></a><span data-ttu-id="f083b-104">Description</span><span class="sxs-lookup"><span data-stu-id="f083b-104">Description</span></span>  
 <span data-ttu-id="f083b-105">Suivi lorsqu'un enrôlement de participant subalterne a terminé le traitement 2PC.</span><span class="sxs-lookup"><span data-stu-id="f083b-105">Traced when a subordinate participant enlistment has completed 2pc processing.</span></span> <span data-ttu-id="f083b-106">Le résultat peut être Committed ou Aborted.</span><span class="sxs-lookup"><span data-stu-id="f083b-106">The outcome for the enlistment can be Committed or Aborted.</span></span> <span data-ttu-id="f083b-107">Il est également suivi lorsque les participants votent ReadOnly pendant la préparation.</span><span class="sxs-lookup"><span data-stu-id="f083b-107">It is also traced if any participant votes ReadOnly during Prepare.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f083b-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f083b-108">See also</span></span>
- [<span data-ttu-id="f083b-109">Suivi</span><span class="sxs-lookup"><span data-stu-id="f083b-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="f083b-110">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="f083b-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="f083b-111">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="f083b-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
