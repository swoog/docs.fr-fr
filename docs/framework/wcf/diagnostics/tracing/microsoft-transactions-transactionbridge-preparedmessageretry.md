---
title: Microsoft.Transactions.TransactionBridge.PreparedMessageRetry
ms.date: 03/30/2017
ms.assetid: 2194292d-bf5f-4aef-9336-cd3c4795cb71
ms.openlocfilehash: ba35f948143aff3de575e966aaec87f32f6f14b4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33473774"
---
# <a name="microsofttransactionstransactionbridgepreparedmessageretry"></a><span data-ttu-id="18ebd-102">Microsoft.Transactions.TransactionBridge.PreparedMessageRetry</span><span class="sxs-lookup"><span data-stu-id="18ebd-102">Microsoft.Transactions.TransactionBridge.PreparedMessageRetry</span></span>
<span data-ttu-id="18ebd-103">Une nouvelle tentative de message Prepared a été envoyée à un coordinateur qui ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="18ebd-103">A prepared message retry was sent to an unresponsive coordinator.</span></span>  
  
## <a name="description"></a><span data-ttu-id="18ebd-104">Description</span><span class="sxs-lookup"><span data-stu-id="18ebd-104">Description</span></span>  
 <span data-ttu-id="18ebd-105">Suivi lorsque le gestionnaire de transactions local a dû renvoyer un message Prepared à un coordinateur supérieur parce qu’il n’a pas reçu de réponse dans un délai donné.</span><span class="sxs-lookup"><span data-stu-id="18ebd-105">Traced if the local Transaction Manager needed to resend a Prepared message to a superior coordinator because it did not receive a response in a given amount of time/</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="18ebd-106">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="18ebd-106">Troubleshooting</span></span>  
 <span data-ttu-id="18ebd-107">Recherchez d'éventuels problèmes liés au réseau ou au produit pouvant empêcher la réponse d'être remise à temps.</span><span class="sxs-lookup"><span data-stu-id="18ebd-107">Investigate potential network or product issues that prevent the response from being delivered on time.</span></span>  <span data-ttu-id="18ebd-108">Si un nombre élevé de ces messages apparaissent, cela peut indiquer des problèmes d'infrastructure ou des délais de réponse anormalement longs.</span><span class="sxs-lookup"><span data-stu-id="18ebd-108">If many of these messages are seen, it can indicate infrastructure problems or abnormally long response times.</span></span> <span data-ttu-id="18ebd-109">Ces deux problèmes réduiront considérablement le débit des transactions au sein du système.</span><span class="sxs-lookup"><span data-stu-id="18ebd-109">Both issues will drastically reduce the throughput of transactions within the system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="18ebd-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18ebd-110">See Also</span></span>  
 [<span data-ttu-id="18ebd-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="18ebd-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [<span data-ttu-id="18ebd-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="18ebd-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [<span data-ttu-id="18ebd-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="18ebd-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
