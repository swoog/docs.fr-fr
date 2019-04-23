---
title: Microsoft.Transactions.TransactionBridge.EnlistTransactionFailure
ms.date: 03/30/2017
ms.assetid: 1b9f5139-e122-4716-9ef7-2f38e1813993
ms.openlocfilehash: 93c96d94aaeddeb7e7b04ea80645b8de95b0343e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59143323"
---
# <a name="microsofttransactionstransactionbridgeenlisttransactionfailure"></a><span data-ttu-id="eb587-102">Microsoft.Transactions.TransactionBridge.EnlistTransactionFailure</span><span class="sxs-lookup"><span data-stu-id="eb587-102">Microsoft.Transactions.TransactionBridge.EnlistTransactionFailure</span></span>
<span data-ttu-id="eb587-103">Le service du protocole WS-AT a échoué l'enrôlement sur une transaction en utilisant le contexte de coordination fourni.</span><span class="sxs-lookup"><span data-stu-id="eb587-103">The WS-AT protocol service failed to enlist on a transaction using the provided coordination context.</span></span>  
  
## <a name="description"></a><span data-ttu-id="eb587-104">Description</span><span class="sxs-lookup"><span data-stu-id="eb587-104">Description</span></span>  
 <span data-ttu-id="eb587-105">Suivi lorsque MSDTC ne peut pas enrôler sur une transaction pour un protocole 2PC donné.</span><span class="sxs-lookup"><span data-stu-id="eb587-105">Traced when MSDTC is unable to enlist on a transaction for a given 2pc protocol.</span></span>  <span data-ttu-id="eb587-106">Cela peut être dû au fait que la transaction n'existe plus, que l'enrôlement n'est plus autorisé, ou qu'un trop grand nombre d'enrôlements sont déjà présents.</span><span class="sxs-lookup"><span data-stu-id="eb587-106">This can happen because the transaction no longer exists, enlisting is no longer allowed, or too many enlistments are already present.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="eb587-107">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="eb587-107">Troubleshooting</span></span>  
 <span data-ttu-id="eb587-108">Inspectez la chaîne d'état dans le message de suivi pour déterminer la présence éventuelle d'éléments actionnables.</span><span class="sxs-lookup"><span data-stu-id="eb587-108">Inspect the status string within the trace message to determine if any actionable item exists.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb587-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb587-109">See also</span></span>

- [<span data-ttu-id="eb587-110">Suivi</span><span class="sxs-lookup"><span data-stu-id="eb587-110">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="eb587-111">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="eb587-111">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="eb587-112">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="eb587-112">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
