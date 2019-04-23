---
title: Microsoft.Transactions.TransactionBridge.VolatileOutcomeTimeout
ms.date: 03/30/2017
ms.assetid: 2dbe34c5-57c7-4b64-9257-63021911d03c
ms.openlocfilehash: 22992b4dfad4b4867adda0fcbbd8ecc5eb67d87e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59160145"
---
# <a name="microsofttransactionstransactionbridgevolatileoutcometimeout"></a><span data-ttu-id="c9e36-102">Microsoft.Transactions.TransactionBridge.VolatileOutcomeTimeout</span><span class="sxs-lookup"><span data-stu-id="c9e36-102">Microsoft.Transactions.TransactionBridge.VolatileOutcomeTimeout</span></span>
<span data-ttu-id="c9e36-103">Le service du protocole WS-AT a dépassé le délai spécifié lors de l'attente d'une réponse à un message de résultat provenant d'un participant volatil.</span><span class="sxs-lookup"><span data-stu-id="c9e36-103">The WS-AT protocol service timed out waiting for a response to an outcome message from a volatile participant.</span></span> <span data-ttu-id="c9e36-104">Le résultat de la transaction peut s'avérer incertain si le participant retourne.</span><span class="sxs-lookup"><span data-stu-id="c9e36-104">The transaction outcome may be in doubt if the participant returns.</span></span>  
  
## <a name="description"></a><span data-ttu-id="c9e36-105">Description</span><span class="sxs-lookup"><span data-stu-id="c9e36-105">Description</span></span>  
 <span data-ttu-id="c9e36-106">Suivi lorsqu’un participant volatil a décidé de valider ou d’abandonner mais n’a pas répondu à une demande de validation ou de restauration dans un délai donné.</span><span class="sxs-lookup"><span data-stu-id="c9e36-106">Traced when a Volatile participant has decided to Commit or Abort but has not responded to a Commit or Rollback request within a given amount of time.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="c9e36-107">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="c9e36-107">Troubleshooting</span></span>  
 <span data-ttu-id="c9e36-108">Assurez-vous que tous les participants volatils sont en mesure de répondre dans le délai imparti.</span><span class="sxs-lookup"><span data-stu-id="c9e36-108">Ensure that all Volatile participants are able to respond within the given amount of time.</span></span> <span data-ttu-id="c9e36-109">Le délai par défaut est de 180 secondes.</span><span class="sxs-lookup"><span data-stu-id="c9e36-109">The default time period is 180 seconds.</span></span>  <span data-ttu-id="c9e36-110">S'il est insuffisant, augmentez le délai du minuteur `VolatileOutcomeDelay` de WS-AT.</span><span class="sxs-lookup"><span data-stu-id="c9e36-110">If this is insufficient, increase the `VolatileOutcomeDelay` timer policy for WS-AT.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9e36-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9e36-111">See also</span></span>

- [<span data-ttu-id="c9e36-112">Suivi</span><span class="sxs-lookup"><span data-stu-id="c9e36-112">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="c9e36-113">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="c9e36-113">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="c9e36-114">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="c9e36-114">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
