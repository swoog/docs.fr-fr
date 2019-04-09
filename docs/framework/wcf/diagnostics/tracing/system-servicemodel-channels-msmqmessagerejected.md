---
title: System.ServiceModel.Channels.MsmqMessageRejected
ms.date: 03/30/2017
ms.assetid: 9b7c10a7-2af6-44a2-8b1a-90bba0c7cf26
ms.openlocfilehash: 4feeb1b57d79c7445d51f5d688b0a9f55e761542
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59143388"
---
# <a name="systemservicemodelchannelsmsmqmessagerejected"></a><span data-ttu-id="83b93-102">System.ServiceModel.Channels.MsmqMessageRejected</span><span class="sxs-lookup"><span data-stu-id="83b93-102">System.ServiceModel.Channels.MsmqMessageRejected</span></span>
<span data-ttu-id="83b93-103">MSMQ a refusé le message.</span><span class="sxs-lookup"><span data-stu-id="83b93-103">MSMQ rejected the message.</span></span>  
  
## <a name="description"></a><span data-ttu-id="83b93-104">Description</span><span class="sxs-lookup"><span data-stu-id="83b93-104">Description</span></span>  
 <span data-ttu-id="83b93-105">Ce suivi indique qu'un message MSMQ a été refusé.</span><span class="sxs-lookup"><span data-stu-id="83b93-105">This trace indicates that an MSMQ message was rejected.</span></span>  
  
 <span data-ttu-id="83b93-106">Messages MSMQ pouvant être rejetées lorsque Windows Communication Foundation (WCF) (utilisé avec NetMsmqBinding ou MsmqIntegrationBinding) ne peut pas les traiter.</span><span class="sxs-lookup"><span data-stu-id="83b93-106">MSMQ messages can be rejected when Windows Communication Foundation (WCF) (used with either the NetMsmqBinding or MsmqIntegrationBinding) is unable to process them.</span></span> <span data-ttu-id="83b93-107">Ces messages sont appelés des messages incohérents.</span><span class="sxs-lookup"><span data-stu-id="83b93-107">Such messages are referred to as poison messages.</span></span> <span data-ttu-id="83b93-108">Un message incohérent est refusé lorsque la propriété `ReceiveErrorHandling` sur NetMsmqBinding ou MsmqIntegrationBinding a la valeur `Reject`.</span><span class="sxs-lookup"><span data-stu-id="83b93-108">A poison message is rejected when the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding is set to `Reject`.</span></span> <span data-ttu-id="83b93-109">Un message refusé est remis à l’expéditeur [file d’attente de lettres mortes](https://go.microsoft.com/fwlink/?LinkID=99544).</span><span class="sxs-lookup"><span data-stu-id="83b93-109">A rejected message is delivered back to the sender’s [Dead-Letter Queue](https://go.microsoft.com/fwlink/?LinkID=99544).</span></span>  
  
 <span data-ttu-id="83b93-110">Consultez [des messages incohérents](https://go.microsoft.com/fwlink/?LinkID=99546) pour plus d’informations sur le moment où les messages deviennent incohérents et comment configurer votre service pour traiter de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="83b93-110">See [Poison-Message Handling](https://go.microsoft.com/fwlink/?LinkID=99546) for more details on when messages become poison and how to configure your service to handle them appropriately.</span></span>  
  
 <span data-ttu-id="83b93-111">Consultez [MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkID=99548) pour plus d’informations sur ce que signifie un message refusé dans MSMQ.</span><span class="sxs-lookup"><span data-stu-id="83b93-111">See [MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkID=99548) for more details on what a rejected message means in MSMQ.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83b93-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83b93-112">See also</span></span>

- [<span data-ttu-id="83b93-113">Traçage</span><span class="sxs-lookup"><span data-stu-id="83b93-113">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="83b93-114">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="83b93-114">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="83b93-115">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="83b93-115">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
- [<span data-ttu-id="83b93-116">Gestion des messages incohérents</span><span class="sxs-lookup"><span data-stu-id="83b93-116">Poison-Message Handling</span></span>](https://go.microsoft.com/fwlink/?LinkID=99546)
- [<span data-ttu-id="83b93-117">MQMarkMessageRejected</span><span class="sxs-lookup"><span data-stu-id="83b93-117">MQMarkMessageRejected</span></span>](https://go.microsoft.com/fwlink/?LinkID=99548)
