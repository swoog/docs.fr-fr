---
title: Microsoft.Transactions.TransactionBridge.CommitMessageRetry
ms.date: 03/30/2017
ms.assetid: 4abe01f0-6398-4fba-b2f3-c054b7f7e971
ms.openlocfilehash: 3c398aa13a8cd2b87068216d3c07fb29e1a27c3f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59168101"
---
# <a name="microsofttransactionstransactionbridgecommitmessageretry"></a><span data-ttu-id="94b9d-102">Microsoft.Transactions.TransactionBridge.CommitMessageRetry</span><span class="sxs-lookup"><span data-stu-id="94b9d-102">Microsoft.Transactions.TransactionBridge.CommitMessageRetry</span></span>
<span data-ttu-id="94b9d-103">Une nouvelle tentative de message de validation a été envoyée à un participant qui ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="94b9d-103">A commit message retry was sent to an unresponsive participant.</span></span>  
  
## <a name="description"></a><span data-ttu-id="94b9d-104">Description</span><span class="sxs-lookup"><span data-stu-id="94b9d-104">Description</span></span>  
 <span data-ttu-id="94b9d-105">Suivi lorsque le gestionnaire de transactions local a dû renvoyer un message de validation à un participant subalterne parce qu'il n'a pas reçu de réponse dans un délai donné.</span><span class="sxs-lookup"><span data-stu-id="94b9d-105">Traced if the local Transaction Manager needed to resend a Commit message to a subordinate participant because it did not receive a response in a given amount of time.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="94b9d-106">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="94b9d-106">Troubleshooting</span></span>  
 <span data-ttu-id="94b9d-107">Recherchez d'éventuels problèmes liés au réseau ou au produit pouvant empêcher la réponse d'être remise à temps.</span><span class="sxs-lookup"><span data-stu-id="94b9d-107">Investigate potential network or product issues that prevent the response from being delivered on time.</span></span>  <span data-ttu-id="94b9d-108">Si un nombre élevé de ces messages apparaissent, cela peut indiquer des problèmes d'infrastructure ou des délais de réponse anormalement longs.</span><span class="sxs-lookup"><span data-stu-id="94b9d-108">If many of these messages are seen, it can indicate infrastructure problems or abnormally long response times.</span></span> <span data-ttu-id="94b9d-109">Ces deux problèmes réduiront considérablement le débit des transactions au sein du système.</span><span class="sxs-lookup"><span data-stu-id="94b9d-109">Both issues will drastically reduce the throughput of transactions within the system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94b9d-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94b9d-110">See also</span></span>

- [<span data-ttu-id="94b9d-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="94b9d-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="94b9d-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="94b9d-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="94b9d-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="94b9d-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
