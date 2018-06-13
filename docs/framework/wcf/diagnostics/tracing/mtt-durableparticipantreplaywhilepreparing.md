---
title: Microsoft.Transactions.TransactionBridge.DurableParticipantReplayWhilePreparing
ms.date: 03/30/2017
ms.assetid: 10ef3876-6f8e-4d4e-8444-f47847b64795
ms.openlocfilehash: fe88e70ab4955305d78baa1158cd73a93ba2ed2c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33476318"
---
# <a name="microsofttransactionstransactionbridgedurableparticipantreplaywhilepreparing"></a><span data-ttu-id="c0013-102">Microsoft.Transactions.TransactionBridge.DurableParticipantReplayWhilePreparing</span><span class="sxs-lookup"><span data-stu-id="c0013-102">Microsoft.Transactions.TransactionBridge.DurableParticipantReplayWhilePreparing</span></span>
<span data-ttu-id="c0013-103">Le service de protocole WS-AT a reçu un message Replay d'un participant durable n'ayant pas répondu au message Prepared.</span><span class="sxs-lookup"><span data-stu-id="c0013-103">The WS-AT protocol service received a Replay message from a durable participant, which did not respond to Prepare.</span></span> <span data-ttu-id="c0013-104">Par conséquent, la transaction a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="c0013-104">Consequently, the transaction was aborted.</span></span>  
  
## <a name="description"></a><span data-ttu-id="c0013-105">Description</span><span class="sxs-lookup"><span data-stu-id="c0013-105">Description</span></span>  
 <span data-ttu-id="c0013-106">Un suivi est généré si un message Replay est reçu lorsqu'un participant durable est encore en cours de préparation.</span><span class="sxs-lookup"><span data-stu-id="c0013-106">Traced if a Replay message is received while a Durable participant is still Preparing.</span></span> <span data-ttu-id="c0013-107">Il s'agit d'un message illégal pour cet état et la transaction va être abandonnée.</span><span class="sxs-lookup"><span data-stu-id="c0013-107">This is an illegal message for this state and the transaction is going to be aborted.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="c0013-108">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="c0013-108">Troubleshooting</span></span>  
 <span data-ttu-id="c0013-109">Recevoir ce message d’erreur peut indiquer que la défaillance du participant durable (notamment d’un gestionnaire de transactions subalterne) est à présent résolue. Cependant, le résultat de la transaction étant incertain, une requête de statut est envoyée.</span><span class="sxs-lookup"><span data-stu-id="c0013-109">Receiving this error can indiate that a Durable participant (including Subordinate TransactionManagers) has recovered from failure, however it is unsure of the transaction outcome and request its status.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0013-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0013-110">See Also</span></span>  
 [<span data-ttu-id="c0013-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="c0013-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [<span data-ttu-id="c0013-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="c0013-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [<span data-ttu-id="c0013-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="c0013-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
