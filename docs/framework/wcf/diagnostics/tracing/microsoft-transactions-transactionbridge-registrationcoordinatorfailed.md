---
title: Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFailed
ms.date: 03/30/2017
ms.assetid: 96474056-0418-41e4-8c75-bbc0a853eaba
ms.openlocfilehash: 5c8592ac34375445964b3dbcbbd4800c47e53850
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515048"
---
# <a name="microsofttransactionstransactionbridgeregistrationcoordinatorfailed"></a><span data-ttu-id="8c259-102">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFailed</span><span class="sxs-lookup"><span data-stu-id="8c259-102">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFailed</span></span>
<span data-ttu-id="8c259-103">Le service du protocole WS-AT a échoué l'envoi d'un message Register à son coordinateur</span><span class="sxs-lookup"><span data-stu-id="8c259-103">The WS-AT protocol service failed to send a Register message to its coordinator</span></span>  
  
## <a name="description"></a><span data-ttu-id="8c259-104">Description</span><span class="sxs-lookup"><span data-stu-id="8c259-104">Description</span></span>  
 <span data-ttu-id="8c259-105">Un suivi est effectué si le TransactionManager local n’est pas en mesure de s’inscrire auprès de son supérieur TransactionManager en raison de l’incapacité à envoyer un message.</span><span class="sxs-lookup"><span data-stu-id="8c259-105">Traced if the local TransactionManager is not able to Register with its superior TransactionManager due to the inability to send a message.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="8c259-106">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="8c259-106">Troubleshooting</span></span>  
 <span data-ttu-id="8c259-107">Inspectez le message de suivi pour l'exception qui provoque l'échec de l'envoi du message.</span><span class="sxs-lookup"><span data-stu-id="8c259-107">Inspect the trace message for the exception causing the message send failure</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8c259-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c259-108">See also</span></span>
- [<span data-ttu-id="8c259-109">Suivi</span><span class="sxs-lookup"><span data-stu-id="8c259-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="8c259-110">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="8c259-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="8c259-111">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="8c259-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
