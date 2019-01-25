---
title: System.ServiceModel.Channels.MsmqMoveOrDeleteAttemptFailed
ms.date: 03/30/2017
ms.assetid: d75d39da-7502-4a6a-91b9-eaa05b8e24d5
ms.openlocfilehash: ade49ceb86a401cd27a9381b1ea5d0c1ad624548
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54623090"
---
# <a name="systemservicemodelchannelsmsmqmoveordeleteattemptfailed"></a><span data-ttu-id="af867-102">System.ServiceModel.Channels.MsmqMoveOrDeleteAttemptFailed</span><span class="sxs-lookup"><span data-stu-id="af867-102">System.ServiceModel.Channels.MsmqMoveOrDeleteAttemptFailed</span></span>
<span data-ttu-id="af867-103">Impossible de déplacer ou de supprimer le message.</span><span class="sxs-lookup"><span data-stu-id="af867-103">Cannot move or delete message.</span></span>  
  
## <a name="description"></a><span data-ttu-id="af867-104">Description</span><span class="sxs-lookup"><span data-stu-id="af867-104">Description</span></span>  
 <span data-ttu-id="af867-105">Le suivi indique qu'un échec a eu lieu lors de la tentative de déplacement, d'élimination ou de rejet d'un message MSMQ.</span><span class="sxs-lookup"><span data-stu-id="af867-105">The trace indicates that a failure occurred when attempting to move, delete, or reject an MSMQ message.</span></span>  
  
 <span data-ttu-id="af867-106">Messages MSMQ sont employés par Windows Communication Foundation (WCF) (lorsque utilisé avec NetMsmqBinding ou MsmqIntegrationBinding). Ce suivi est lié à la valeur choisie le `ReceiveErrorHandling` propriété sur NetMsmqBinding ou MsmqIntegrationBinding.</span><span class="sxs-lookup"><span data-stu-id="af867-106">MSMQ messages are employed by Windows Communication Foundation (WCF) (when used with either the NetMsmqBinding or the MsmqIntegrationBinding).This trace is related to the chosen value of the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding.</span></span>  
  
 <span data-ttu-id="af867-107">Ce suivi n'indique pas une défaillance générale du système.</span><span class="sxs-lookup"><span data-stu-id="af867-107">This trace is not indicative of an overall system failure.</span></span> <span data-ttu-id="af867-108">Toutefois, il indique que la disposition de message incohérent choisie a échoué pour un message.</span><span class="sxs-lookup"><span data-stu-id="af867-108">However, it indicates that the chosen poison message disposition failed for a message.</span></span> <span data-ttu-id="af867-109">Consultez [des messages incohérents](https://go.microsoft.com/fwlink/?LinkID=99546) pour plus d’informations sur le moment où les messages deviennent incohérents et comment configurer votre service pour traiter de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="af867-109">See [Poison-Message Handling](https://go.microsoft.com/fwlink/?LinkID=99546) for more details on when messages become poison and how to configure your service to handle them appropriately.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="af867-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af867-110">See also</span></span>
- [<span data-ttu-id="af867-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="af867-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="af867-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="af867-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="af867-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="af867-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
