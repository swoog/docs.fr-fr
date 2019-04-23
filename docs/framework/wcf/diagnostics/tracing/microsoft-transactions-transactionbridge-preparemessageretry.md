---
title: Microsoft.Transactions.TransactionBridge.PrepareMessageRetry
ms.date: 03/30/2017
ms.assetid: ada4baa5-b60d-46b8-ad46-4d69f8d8a9fa
ms.openlocfilehash: 02e275fa212128c65beda4bc3703949e75ea5092
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59220888"
---
# <a name="microsofttransactionstransactionbridgepreparemessageretry"></a><span data-ttu-id="1f35c-102">Microsoft.Transactions.TransactionBridge.PrepareMessageRetry</span><span class="sxs-lookup"><span data-stu-id="1f35c-102">Microsoft.Transactions.TransactionBridge.PrepareMessageRetry</span></span>
<span data-ttu-id="1f35c-103">Une nouvelle tentative de message prepare a été envoyée à un participant qui ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="1f35c-103">A prepare message retry was sent to an unresponsive participant.</span></span>  
  
## <a name="description"></a><span data-ttu-id="1f35c-104">Description</span><span class="sxs-lookup"><span data-stu-id="1f35c-104">Description</span></span>  
 <span data-ttu-id="1f35c-105">Tracé si le gestionnaire de transactions local a dû renvoyer un message prepare à un participant subalterne parce qu’il n’a pas reçu de réponse dans une délai donné.</span><span class="sxs-lookup"><span data-stu-id="1f35c-105">Traced if the local Transaction Manager needed to resend a Prepare message to a subordinate participant because it did not receive a response in a given amount of time.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="1f35c-106">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="1f35c-106">Troubleshooting</span></span>  
 <span data-ttu-id="1f35c-107">Recherchez d'éventuels problèmes liés au réseau ou au produit pouvant empêcher la réponse d'être remise à temps.</span><span class="sxs-lookup"><span data-stu-id="1f35c-107">Investigate potential network or product issues that prevent the response from being delivered on time.</span></span>  <span data-ttu-id="1f35c-108">Si un nombre élevé de ces messages apparaissent, cela peut indiquer des problèmes d'infrastructure ou des délais de réponse anormalement longs.</span><span class="sxs-lookup"><span data-stu-id="1f35c-108">If many of these messages are seen, it can indicate infrastructure problems or abnormally long response times.</span></span> <span data-ttu-id="1f35c-109">Ces deux problèmes peuvent réduire considérablement le débit des transactions au sein du système.</span><span class="sxs-lookup"><span data-stu-id="1f35c-109">Both issues can drastically reduce the throughput of transactions within the system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1f35c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f35c-110">See also</span></span>

- [<span data-ttu-id="1f35c-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="1f35c-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="1f35c-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="1f35c-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="1f35c-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="1f35c-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
