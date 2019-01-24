---
title: Microsoft.Transactions.TransactionBridge.PreparedMessageRetry
ms.date: 03/30/2017
ms.assetid: 2194292d-bf5f-4aef-9336-cd3c4795cb71
ms.openlocfilehash: e5735596f1b724e47cdaadd30f07629ea6b772eb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54585927"
---
# <a name="microsofttransactionstransactionbridgepreparedmessageretry"></a><span data-ttu-id="0828d-102">Microsoft.Transactions.TransactionBridge.PreparedMessageRetry</span><span class="sxs-lookup"><span data-stu-id="0828d-102">Microsoft.Transactions.TransactionBridge.PreparedMessageRetry</span></span>
<span data-ttu-id="0828d-103">Une nouvelle tentative de message Prepared a été envoyée à un coordinateur qui ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="0828d-103">A prepared message retry was sent to an unresponsive coordinator.</span></span>  
  
## <a name="description"></a><span data-ttu-id="0828d-104">Description</span><span class="sxs-lookup"><span data-stu-id="0828d-104">Description</span></span>  
 <span data-ttu-id="0828d-105">Suivi lorsque le gestionnaire de transactions local a dû renvoyer un message Prepared à un coordinateur supérieur parce qu’il n’a pas reçu de réponse dans un délai donné.</span><span class="sxs-lookup"><span data-stu-id="0828d-105">Traced if the local Transaction Manager needed to resend a Prepared message to a superior coordinator because it did not receive a response in a given amount of time/</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="0828d-106">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="0828d-106">Troubleshooting</span></span>  
 <span data-ttu-id="0828d-107">Recherchez d'éventuels problèmes liés au réseau ou au produit pouvant empêcher la réponse d'être remise à temps.</span><span class="sxs-lookup"><span data-stu-id="0828d-107">Investigate potential network or product issues that prevent the response from being delivered on time.</span></span>  <span data-ttu-id="0828d-108">Si un nombre élevé de ces messages apparaissent, cela peut indiquer des problèmes d'infrastructure ou des délais de réponse anormalement longs.</span><span class="sxs-lookup"><span data-stu-id="0828d-108">If many of these messages are seen, it can indicate infrastructure problems or abnormally long response times.</span></span> <span data-ttu-id="0828d-109">Ces deux problèmes réduiront considérablement le débit des transactions au sein du système.</span><span class="sxs-lookup"><span data-stu-id="0828d-109">Both issues will drastically reduce the throughput of transactions within the system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0828d-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0828d-110">See also</span></span>
- [<span data-ttu-id="0828d-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="0828d-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="0828d-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="0828d-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="0828d-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="0828d-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
