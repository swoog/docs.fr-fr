---
title: Microsoft.Transactions.TransactionBridge.RegisterParticipantFailure
ms.date: 03/30/2017
ms.assetid: 3a4ead79-8550-4037-84e3-fd70ff56e001
ms.openlocfilehash: e56a9ed1d837af27d481282e0e106d537ec41ee3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59164292"
---
# <a name="microsofttransactionstransactionbridgeregisterparticipantfailure"></a><span data-ttu-id="2033c-102">Microsoft.Transactions.TransactionBridge.RegisterParticipantFailure</span><span class="sxs-lookup"><span data-stu-id="2033c-102">Microsoft.Transactions.TransactionBridge.RegisterParticipantFailure</span></span>
<span data-ttu-id="2033c-103">Le service de protocole WS-AT n'a pas pu inscrire un participant à un protocole de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2033c-103">The WS-AT protocol service failed to register a participant for a control protocol.</span></span>  
  
## <a name="description"></a><span data-ttu-id="2033c-104">Description</span><span class="sxs-lookup"><span data-stu-id="2033c-104">Description</span></span>  
 <span data-ttu-id="2033c-105">Suivi lorsque MSDTC détecte une demande d'inscription non valide.</span><span class="sxs-lookup"><span data-stu-id="2033c-105">Traced if MSDTC detects an invalid Registration request.</span></span> <span data-ttu-id="2033c-106">Cela peut être provoqué par plusieurs demandes d'inscription pour achèvement et erreurs internes.</span><span class="sxs-lookup"><span data-stu-id="2033c-106">This can be caused by  multiple Completion registration requests and internal errors.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="2033c-107">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="2033c-107">Troubleshooting</span></span>  
 <span data-ttu-id="2033c-108">Ne procédez pas à plusieurs demandes d'inscription pour achèvement.</span><span class="sxs-lookup"><span data-stu-id="2033c-108">Do not try to Register for Completion more than once.</span></span>  <span data-ttu-id="2033c-109">Par ailleurs, inspectez la chaîne d'état dans le message de suivi pour déterminer la présence éventuelle d'éléments actionnables.</span><span class="sxs-lookup"><span data-stu-id="2033c-109">Also, inspect the status string within the trace message to determine if any actionable item exists.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2033c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2033c-110">See also</span></span>

- [<span data-ttu-id="2033c-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="2033c-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="2033c-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="2033c-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="2033c-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="2033c-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
