---
title: System.ServiceModel.Channels.MsmqMessageDropped
ms.date: 03/30/2017
ms.assetid: 8b6e644d-fa68-4be7-abe9-3659671a37c1
ms.openlocfilehash: 07bef8b391a03f2c011e1d1a7c7fb4fad908e022
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2018
ms.locfileid: "46579798"
---
# <a name="systemservicemodelchannelsmsmqmessagedropped"></a><span data-ttu-id="a292d-102">System.ServiceModel.Channels.MsmqMessageDropped</span><span class="sxs-lookup"><span data-stu-id="a292d-102">System.ServiceModel.Channels.MsmqMessageDropped</span></span>
<span data-ttu-id="a292d-103">MSMQ a supprimé le message.</span><span class="sxs-lookup"><span data-stu-id="a292d-103">MSMQ dropped the message.</span></span>  
  
## <a name="description"></a><span data-ttu-id="a292d-104">Description</span><span class="sxs-lookup"><span data-stu-id="a292d-104">Description</span></span>  
 <span data-ttu-id="a292d-105">Cette trace indique qu’un message MSMQ a été déposé.</span><span class="sxs-lookup"><span data-stu-id="a292d-105">The trace indicates that an MSMQ message was dropped.</span></span> <span data-ttu-id="a292d-106">Messages MSMQ peuvent être supprimés lorsque Windows Communication Foundation (WCF) (utilisé avec NetMsmqBinding ou MsmqIntegrationBinding) ne peut pas les traiter.</span><span class="sxs-lookup"><span data-stu-id="a292d-106">MSMQ messages can be dropped when Windows Communication Foundation (WCF) (used with either the NetMsmqBinding or MsmqIntegrationBinding) is unable to process them.</span></span> <span data-ttu-id="a292d-107">Ces messages sont appelés des messages incohérents.</span><span class="sxs-lookup"><span data-stu-id="a292d-107">Such messages are referred to as poison messages.</span></span>  
  
 <span data-ttu-id="a292d-108">Un message incohérent est supprimé lorsque la propriété `ReceiveErrorHandling` sur NetMsmqBinding ou MsmqIntegrationBinding a la valeur `Drop`.</span><span class="sxs-lookup"><span data-stu-id="a292d-108">A poison message is dropped when the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding is set to `Drop`.</span></span> <span data-ttu-id="a292d-109">Ce message est supprimé de la file d’attente et ne peut plus être récupéré.</span><span class="sxs-lookup"><span data-stu-id="a292d-109">A dropped message is removed from the queue and is no longer recoverable.</span></span>  
  
 <span data-ttu-id="a292d-110">Consultez [des messages incohérents](https://go.microsoft.com/fwlink/?LinkID=99546) pour plus d’informations sur le moment où les messages deviennent incohérents et comment configurer votre service pour traiter de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="a292d-110">See [Poison-Message Handling](https://go.microsoft.com/fwlink/?LinkID=99546) for more details on when messages become poison and how to configure your service to handle them appropriately.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a292d-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a292d-111">See Also</span></span>  
 [<span data-ttu-id="a292d-112">Suivi</span><span class="sxs-lookup"><span data-stu-id="a292d-112">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [<span data-ttu-id="a292d-113">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="a292d-113">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [<span data-ttu-id="a292d-114">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="a292d-114">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)  
 [<span data-ttu-id="a292d-115">Messages incohérents</span><span class="sxs-lookup"><span data-stu-id="a292d-115">Poison-Message Handling</span></span>](https://go.microsoft.com/fwlink/?LinkID=99546)
