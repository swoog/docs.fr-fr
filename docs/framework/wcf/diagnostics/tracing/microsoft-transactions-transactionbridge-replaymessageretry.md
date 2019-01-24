---
title: Microsoft.Transactions.TransactionBridge.ReplayMessageRetry
ms.date: 03/30/2017
ms.assetid: e5b820ae-504d-405a-926a-9effa41d2369
ms.openlocfilehash: bb7f6fcf95d1ff253fa0e2963610bee2b65ef3c2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54597110"
---
# <a name="microsofttransactionstransactionbridgereplaymessageretry"></a><span data-ttu-id="d9283-102">Microsoft.Transactions.TransactionBridge.ReplayMessageRetry</span><span class="sxs-lookup"><span data-stu-id="d9283-102">Microsoft.Transactions.TransactionBridge.ReplayMessageRetry</span></span>
<span data-ttu-id="d9283-103">Une nouvelle tentative de message Replay a été envoyée à un coordinateur qui ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="d9283-103">A replay message retry was sent to an unresponsive coordinator.</span></span>  
  
## <a name="description"></a><span data-ttu-id="d9283-104">Description</span><span class="sxs-lookup"><span data-stu-id="d9283-104">Description</span></span>  
 <span data-ttu-id="d9283-105">Suivi si le gestionnaire de transactions local a dû renvoyer un message Replay à un coordinateur supérieur parce qu'il n'a pas reçu de réponse dans un délai donné.</span><span class="sxs-lookup"><span data-stu-id="d9283-105">Traced if the local Transaction Manager needed to resend a Replay message to a superior coordinator because it did not receive a response in a given amount of time.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="d9283-106">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="d9283-106">Troubleshooting</span></span>  
 <span data-ttu-id="d9283-107">Recherchez d'éventuels problèmes liés au réseau ou au produit pouvant empêcher la réponse d'être remise à temps.</span><span class="sxs-lookup"><span data-stu-id="d9283-107">Investigate potential network or product issues that prevent the response from being delivered on time.</span></span>  <span data-ttu-id="d9283-108">Si un nombre élevé de ces messages apparaissent, cela peut indiquer des problèmes d'infrastructure ou des délais de réponse anormalement longs.</span><span class="sxs-lookup"><span data-stu-id="d9283-108">If many of these messages are seen, it can indicate infrastructure problems or abnormally long response times.</span></span> <span data-ttu-id="d9283-109">Ces deux problèmes réduiront considérablement le débit des transactions au sein du système.</span><span class="sxs-lookup"><span data-stu-id="d9283-109">Both issues will drastically reduce the throughput of transactions within the system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9283-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9283-110">See also</span></span>
- [<span data-ttu-id="d9283-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="d9283-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="d9283-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="d9283-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="d9283-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="d9283-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
