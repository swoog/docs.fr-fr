---
title: System.ServiceModel.Channels.MsmqPoisonMessageRejected
ms.date: 03/30/2017
ms.assetid: 0e64b9bd-1f12-43df-a189-d7be3c2bace1
ms.openlocfilehash: 562399c1d45dc73c7c88bd165e9f95ee1bcfa19d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59125079"
---
# <a name="systemservicemodelchannelsmsmqpoisonmessagerejected"></a><span data-ttu-id="d1abd-102">System.ServiceModel.Channels.MsmqPoisonMessageRejected</span><span class="sxs-lookup"><span data-stu-id="d1abd-102">System.ServiceModel.Channels.MsmqPoisonMessageRejected</span></span>
<span data-ttu-id="d1abd-103">Message poison rejeté.</span><span class="sxs-lookup"><span data-stu-id="d1abd-103">Poison message rejected.</span></span>  
  
## <a name="description"></a><span data-ttu-id="d1abd-104">Description</span><span class="sxs-lookup"><span data-stu-id="d1abd-104">Description</span></span>  
 <span data-ttu-id="d1abd-105">Le suivi indique qu'un message poison a été rencontré et rejeté par la suite.</span><span class="sxs-lookup"><span data-stu-id="d1abd-105">The trace indicates that a poison message was encountered and subsequently rejected.</span></span> <span data-ttu-id="d1abd-106">Cela se produit seulement lorsque la propriété `ReceiveErrorHandling` sur NetMsmqBinding ou MsmqIntegrationBinding a la valeur `Reject`.</span><span class="sxs-lookup"><span data-stu-id="d1abd-106">This occurs when the `ReceiveErrorHandling` property on the NetMsmqBinding or MsmqIntegrationBinding is set to `Reject`.</span></span> <span data-ttu-id="d1abd-107">Un message refusé est remis à l’expéditeur [file d’attente de lettres mortes](https://go.microsoft.com/fwlink/?LinkId=99544).</span><span class="sxs-lookup"><span data-stu-id="d1abd-107">A rejected message is delivered back to the sender’s [Dead-Letter Queue](https://go.microsoft.com/fwlink/?LinkId=99544).</span></span>  
  
 <span data-ttu-id="d1abd-108">Consultez [des messages incohérents](https://go.microsoft.com/fwlink/?LinkId=99546) pour plus d’informations sur le moment où les messages deviennent incohérents et comment configurer votre service pour traiter de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="d1abd-108">See [Poison-Message Handling](https://go.microsoft.com/fwlink/?LinkId=99546) for more details on when messages become poison and how to configure your service to handle them appropriately.</span></span> <span data-ttu-id="d1abd-109">Consultez [MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkId=99548) pour plus d’informations sur ce que signifie un message refusé dans MSMQ.</span><span class="sxs-lookup"><span data-stu-id="d1abd-109">See [MQMarkMessageRejected](https://go.microsoft.com/fwlink/?LinkId=99548) for more details on what a rejected message means in MSMQ.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1abd-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1abd-110">See also</span></span>

- [<span data-ttu-id="d1abd-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="d1abd-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="d1abd-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="d1abd-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="d1abd-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="d1abd-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
- [<span data-ttu-id="d1abd-114">Messages incohérents</span><span class="sxs-lookup"><span data-stu-id="d1abd-114">Poison-Message Handling</span></span>](https://go.microsoft.com/fwlink/?LinkId=99546)
- [<span data-ttu-id="d1abd-115">MQMarkMessageRejected</span><span class="sxs-lookup"><span data-stu-id="d1abd-115">MQMarkMessageRejected</span></span>](https://go.microsoft.com/fwlink/?LinkId=99548)
