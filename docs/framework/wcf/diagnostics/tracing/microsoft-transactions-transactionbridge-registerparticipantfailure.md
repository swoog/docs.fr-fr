---
title: Microsoft.Transactions.TransactionBridge.RegisterParticipantFailure
ms.date: 03/30/2017
ms.assetid: 3a4ead79-8550-4037-84e3-fd70ff56e001
ms.openlocfilehash: b94c017f6ed3a76a6bc5ed2cb970877ad18ef9ea
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610420"
---
# <a name="microsofttransactionstransactionbridgeregisterparticipantfailure"></a><span data-ttu-id="ab457-102">Microsoft.Transactions.TransactionBridge.RegisterParticipantFailure</span><span class="sxs-lookup"><span data-stu-id="ab457-102">Microsoft.Transactions.TransactionBridge.RegisterParticipantFailure</span></span>
<span data-ttu-id="ab457-103">Le service de protocole WS-AT n'a pas pu inscrire un participant à un protocole de contrôle.</span><span class="sxs-lookup"><span data-stu-id="ab457-103">The WS-AT protocol service failed to register a participant for a control protocol.</span></span>  
  
## <a name="description"></a><span data-ttu-id="ab457-104">Description</span><span class="sxs-lookup"><span data-stu-id="ab457-104">Description</span></span>  
 <span data-ttu-id="ab457-105">Suivi lorsque MSDTC détecte une demande d'inscription non valide.</span><span class="sxs-lookup"><span data-stu-id="ab457-105">Traced if MSDTC detects an invalid Registration request.</span></span> <span data-ttu-id="ab457-106">Cela peut être provoqué par plusieurs demandes d'inscription pour achèvement et erreurs internes.</span><span class="sxs-lookup"><span data-stu-id="ab457-106">This can be caused by  multiple Completion registration requests and internal errors.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="ab457-107">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="ab457-107">Troubleshooting</span></span>  
 <span data-ttu-id="ab457-108">Ne procédez pas à plusieurs demandes d'inscription pour achèvement.</span><span class="sxs-lookup"><span data-stu-id="ab457-108">Do not try to Register for Completion more than once.</span></span>  <span data-ttu-id="ab457-109">Par ailleurs, inspectez la chaîne d'état dans le message de suivi pour déterminer la présence éventuelle d'éléments actionnables.</span><span class="sxs-lookup"><span data-stu-id="ab457-109">Also, inspect the status string within the trace message to determine if any actionable item exists.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab457-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab457-110">See also</span></span>
- [<span data-ttu-id="ab457-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="ab457-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="ab457-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="ab457-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="ab457-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="ab457-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
