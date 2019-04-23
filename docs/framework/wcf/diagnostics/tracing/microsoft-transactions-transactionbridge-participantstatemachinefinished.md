---
title: Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished
ms.date: 03/30/2017
ms.assetid: 54b677f7-03ad-40f2-9c5d-297a8ad9bf90
ms.openlocfilehash: 7f37cb5d9ee3d2d9d56519f785388f278b3333b9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59170727"
---
# <a name="microsofttransactionstransactionbridgeparticipantstatemachinefinished"></a><span data-ttu-id="7724e-102">Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished</span><span class="sxs-lookup"><span data-stu-id="7724e-102">Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished</span></span>
<span data-ttu-id="7724e-103">La machine à états pour un enrôlement de participant est passée à l'état Finished.</span><span class="sxs-lookup"><span data-stu-id="7724e-103">The state machine for a participant enlistment entered the finished state.</span></span>  
  
## <a name="description"></a><span data-ttu-id="7724e-104">Description</span><span class="sxs-lookup"><span data-stu-id="7724e-104">Description</span></span>  
 <span data-ttu-id="7724e-105">Suivi lorsqu'un enrôlement de participant subalterne a terminé le traitement 2PC.</span><span class="sxs-lookup"><span data-stu-id="7724e-105">Traced when a subordinate participant enlistment has completed 2pc processing.</span></span> <span data-ttu-id="7724e-106">Le résultat peut être Committed ou Aborted.</span><span class="sxs-lookup"><span data-stu-id="7724e-106">The outcome for the enlistment can be Committed or Aborted.</span></span> <span data-ttu-id="7724e-107">Il est également suivi lorsque les participants votent ReadOnly pendant la préparation.</span><span class="sxs-lookup"><span data-stu-id="7724e-107">It is also traced if any participant votes ReadOnly during Prepare.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7724e-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7724e-108">See also</span></span>

- [<span data-ttu-id="7724e-109">Suivi</span><span class="sxs-lookup"><span data-stu-id="7724e-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="7724e-110">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="7724e-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="7724e-111">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="7724e-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
