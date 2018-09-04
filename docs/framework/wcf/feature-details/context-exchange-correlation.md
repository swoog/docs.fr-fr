---
title: Corrélation d'échange de contexte
ms.date: 03/30/2017
ms.assetid: 1e2852be-3601-45ae-b507-ccc465d45c60
ms.openlocfilehash: d9de111fa08b4a398bba52bc903ea1fec8c7f298
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43519730"
---
# <a name="context-exchange-correlation"></a><span data-ttu-id="98a8b-102">Corrélation d'échange de contexte</span><span class="sxs-lookup"><span data-stu-id="98a8b-102">Context Exchange Correlation</span></span>
<span data-ttu-id="98a8b-103">Corrélation de contexte est basée sur le mécanisme d’échange de contexte décrit dans le [.NET Context Exchange Protocol Specification](https://go.microsoft.com/fwlink/?LinkId=166059).</span><span class="sxs-lookup"><span data-stu-id="98a8b-103">Context correlation is based on the context exchange mechanism described in the [.NET Context Exchange Protocol Specification](https://go.microsoft.com/fwlink/?LinkId=166059).</span></span> <span data-ttu-id="98a8b-104">La corrélation de contexte utilise un en-tête ou un cookie de contexte bien connu pour lier les messages à l'instance correcte.</span><span class="sxs-lookup"><span data-stu-id="98a8b-104">Context correlation uses a well-known context header or cookie to relate messages to the correct instance.</span></span> <span data-ttu-id="98a8b-105">Pour utiliser la corrélation de contexte, une liaison basée sur le contexte, telle que <xref:System.ServiceModel.BasicHttpContextBinding>, <xref:System.ServiceModel.WSHttpContextBinding> ou <xref:System.ServiceModel.NetTcpContextBinding>, doit être utilisée sur le point de terminaison fourni à l'objet <xref:System.ServiceModel.Activities.WorkflowServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="98a8b-105">To use context correlation, a context-based binding such as <xref:System.ServiceModel.BasicHttpContextBinding>, <xref:System.ServiceModel.WSHttpContextBinding>, or <xref:System.ServiceModel.NetTcpContextBinding> must be used on the endpoint provided to the <xref:System.ServiceModel.Activities.WorkflowServiceHost>.</span></span> <span data-ttu-id="98a8b-106">Cette rubrique explique comment utiliser la corrélation de contexte avec des activités de messagerie dans un service de workflow.</span><span class="sxs-lookup"><span data-stu-id="98a8b-106">This topic explains how to use context correlation with messaging activities in a workflow service.</span></span>  
  
## <a name="using-context-correlation"></a><span data-ttu-id="98a8b-107">Utilisation de la corrélation de contexte</span><span class="sxs-lookup"><span data-stu-id="98a8b-107">Using Context Correlation</span></span>  
 <span data-ttu-id="98a8b-108">La corrélation de contexte est utilisée lorsqu’un client doit faire des appels répétés dans un service de workflow et que le service est hébergé en utilisant l’une des liaisons de contexte.</span><span class="sxs-lookup"><span data-stu-id="98a8b-108">Context correlation is used when a client must make repeated calls into a workflow service and the service is hosted using one of the context bindings.</span></span> <span data-ttu-id="98a8b-109">Ce type de corrélation est initialisé par une <xref:System.ServiceModel.Activities.Receive> / <xref:System.ServiceModel.Activities.SendReply> paire dans le service de workflow.</span><span class="sxs-lookup"><span data-stu-id="98a8b-109">This type of correlation is initialized by a <xref:System.ServiceModel.Activities.Receive>/<xref:System.ServiceModel.Activities.SendReply> pair in the workflow service.</span></span> <span data-ttu-id="98a8b-110">Le contexte est renvoyé au client avec la réponse, puis le client joint ce contexte dans les appels ultérieurs au service.</span><span class="sxs-lookup"><span data-stu-id="98a8b-110">The context is sent back to the client together with the reply, and then the client attaches this context on subsequent calls to the service.</span></span>  
  
### <a name="configuring-context-correlation-in-a-workflow-service"></a><span data-ttu-id="98a8b-111">Configuration de la corrélation de contexte dans un service de workflow</span><span class="sxs-lookup"><span data-stu-id="98a8b-111">Configuring Context Correlation in a Workflow Service</span></span>  
 <span data-ttu-id="98a8b-112">La corrélation de contexte est initialisée à l'aide d'un objet <xref:System.ServiceModel.Activities.ContextCorrelationInitializer>, associé à l'activité <xref:System.ServiceModel.Activities.SendReply> qui répond au message entrant initial.</span><span class="sxs-lookup"><span data-stu-id="98a8b-112">Context correlation is initialized by using a <xref:System.ServiceModel.Activities.ContextCorrelationInitializer> that is associated with the <xref:System.ServiceModel.Activities.SendReply> activity that replies to the initial incoming message.</span></span> <span data-ttu-id="98a8b-113">Dans l'exemple suivant, l'activité <xref:System.ServiceModel.Activities.SendReply> est configurée pour initialiser une corrélation de contexte.</span><span class="sxs-lookup"><span data-stu-id="98a8b-113">In the following example, the <xref:System.ServiceModel.Activities.SendReply> is configured to initialize a context correlation.</span></span>  
  
```csharp  
Variable<string> Item = new Variable<string>();  
Variable<CorrelationHandle> OrderHandle = new Variable<CorrelationHandle>();  
  
Receive StartOrder = new Receive  
{  
    CanCreateInstance = true,  
    ServiceContractName = "IOrderService",  
    OperationName = "StartOrder"  
};  
  
SendReply ReplyToStartOrder = new SendReply  
{  
    Request = StartOrder,  
    CorrelationInitializers =  
    {  
        new ContextCorrelationInitializer  
        {  
            CorrelationHandle = OrderHandle  
        }  
    }  
};  
```  
  
> [!NOTE]
>  <span data-ttu-id="98a8b-114">Dans cet exemple, deux types de correlation sont en fait utilisés : la corrélation de contexte et la corrélation demande-réponse.</span><span class="sxs-lookup"><span data-stu-id="98a8b-114">In this example, there are actually two types of correlation being used: context correlation and request-reply correlation.</span></span> <span data-ttu-id="98a8b-115">La corrélation de contexte est utilisée pour que les appels des clients soient acheminés à l'instance correcte.</span><span class="sxs-lookup"><span data-stu-id="98a8b-115">The context correlation is used so that calls from clients are routed to the correct instance.</span></span> <span data-ttu-id="98a8b-116">La corrélation demande-réponse est utilisée à la fois par les activités <xref:System.ServiceModel.Activities.Receive> et <xref:System.ServiceModel.Activities.SendReply> pour implémenter l'opération bidirectionnelle modelée par ces activités.</span><span class="sxs-lookup"><span data-stu-id="98a8b-116">The request-reply correlation is used by the <xref:System.ServiceModel.Activities.Receive> and the <xref:System.ServiceModel.Activities.SendReply> activities together to implement the two-way operation modeled by these activities.</span></span> <span data-ttu-id="98a8b-117">Dans cet exemple, uniquement la corrélation de contexte est explicitement configurée et le <xref:System.ServiceModel.Activities.Receive> / <xref:System.ServiceModel.Activities.SendReply> paire est à l’aide de la corrélation demande-réponse par défaut qui est fournie par le caractère implicite <xref:System.ServiceModel.Activities.CorrelationHandle> gestion de <xref:System.ServiceModel.Activities.WorkflowServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="98a8b-117">In this example, only the context correlation is explicitly configured, and the <xref:System.ServiceModel.Activities.Receive>/<xref:System.ServiceModel.Activities.SendReply> pair is using the default request-reply correlation that is provided by the implicit <xref:System.ServiceModel.Activities.CorrelationHandle> management of <xref:System.ServiceModel.Activities.WorkflowServiceHost>.</span></span> <span data-ttu-id="98a8b-118">Lorsque vous utilisez le **ReceiveAndSendReply** modèle d’activité dans le Concepteur de workflow, demande-réponse corrélation est explicitement configuré.</span><span class="sxs-lookup"><span data-stu-id="98a8b-118">When using the **ReceiveAndSendReply** activity template in the workflow designer, request-reply correlation is explicitly configured.</span></span> <span data-ttu-id="98a8b-119">Pour plus d’informations sur la corrélation demande-réponse et la gestion de handle de corrélation implicite, consultez [demande-réponse](../../../../docs/framework/wcf/feature-details/request-reply-correlation.md) et [vue d’ensemble de corrélations](../../../../docs/framework/wcf/feature-details/correlation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="98a8b-119">For more information about request-reply correlation and implicit correlation handle management, see [Request-Reply](../../../../docs/framework/wcf/feature-details/request-reply-correlation.md) and [Correlation Overview](../../../../docs/framework/wcf/feature-details/correlation-overview.md).</span></span> <span data-ttu-id="98a8b-120">Pour plus d’informations sur la **ReceiveAndSendReply** modèle d’activité, consultez [ReceiveAndSendReply](/visualstudio/workflow-designer/receiveandsendreply-template-designer).</span><span class="sxs-lookup"><span data-stu-id="98a8b-120">For more information about the **ReceiveAndSendReply** activity template, see [ReceiveAndSendReply](/visualstudio/workflow-designer/receiveandsendreply-template-designer).</span></span>  
  
 <span data-ttu-id="98a8b-121">Les activités <xref:System.ServiceModel.Activities.Receive> ultérieures dans le service de workflow peuvent référencer le <xref:System.ServiceModel.Activities.CorrelationHandle> initialisé par l'activité <xref:System.ServiceModel.Activities.SendReply> dans l'exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="98a8b-121">Subsequent <xref:System.ServiceModel.Activities.Receive> activities in the workflow service can reference the <xref:System.ServiceModel.Activities.CorrelationHandle> that was initialized by the <xref:System.ServiceModel.Activities.SendReply> in the previous example.</span></span>  
  
```csharp  
Receive AddItem = new Receive  
{  
    ServiceContractName = "IOrderService",  
    OperationName = "AddItem",  
    CorrelatesWith = OrderHandle  
};  
```  
  
 <span data-ttu-id="98a8b-122">Le point de terminaison est ensuite configuré sur le <xref:System.ServiceModel.Activities.WorkflowServiceHost> pour utiliser une liaison basée sur le contexte, telle que <xref:System.ServiceModel.BasicHttpContextBinding>.</span><span class="sxs-lookup"><span data-stu-id="98a8b-122">The endpoint is then configured on the <xref:System.ServiceModel.Activities.WorkflowServiceHost> to use a context-based binding, such as <xref:System.ServiceModel.BasicHttpContextBinding>.</span></span>  
  
```xml  
<endpoint  
  contract="IOrderContract"  
  binding = "basicHttpContextBinding"  
  address="http://localhost:8080/OrderService" />  
```  
  
### <a name="configuring-context-correlation-in-a-workflow-client"></a><span data-ttu-id="98a8b-123">Configuration de la corrélation de contexte dans un client workflow</span><span class="sxs-lookup"><span data-stu-id="98a8b-123">Configuring Context Correlation in a Workflow Client</span></span>  
 <span data-ttu-id="98a8b-124">Lorsque le client est un autre workflow, la corrélation de contexte doit être également configurée sur le client.</span><span class="sxs-lookup"><span data-stu-id="98a8b-124">When the client is another workflow, context correlation must be configured on the client as well.</span></span> <span data-ttu-id="98a8b-125">Sur le flux de travail client, le <xref:System.ServiceModel.Activities.ReceiveReply> de la <xref:System.ServiceModel.Activities.Send> / <xref:System.ServiceModel.Activities.ReceiveReply> paire qui effectue l’appel initial au service de workflow doit être configuré avec un <xref:System.ServiceModel.Activities.ContextCorrelationInitializer>.</span><span class="sxs-lookup"><span data-stu-id="98a8b-125">On the client workflow, the <xref:System.ServiceModel.Activities.ReceiveReply> of the <xref:System.ServiceModel.Activities.Send>/<xref:System.ServiceModel.Activities.ReceiveReply> pair that makes the initial call to the workflow service must be configured with a <xref:System.ServiceModel.Activities.ContextCorrelationInitializer>.</span></span>  
  
```csharp  
Variable<CorrelationHandle> cchandle = new Variable<CorrelationHandle>();  
Send request = new Send  
{  
    // Activity configuration omitted.  
};  
  
ReceiveReply reply = new ReceiveReply  
{  
    Request = request,  
    CorrelationInitializers =   
    {  
        new ContextCorrelationInitializer  
        {  
            CorrelationHandle = cchandle  
        }  
    }  
};  
```  
  
 <span data-ttu-id="98a8b-126">Une fois la corrélation initialisée, les activités <xref:System.ServiceModel.Activities.Send> ultérieures peuvent utiliser le <xref:System.ServiceModel.Activities.CorrelationHandle> pour appeler les méthodes sur la même instance du service.</span><span class="sxs-lookup"><span data-stu-id="98a8b-126">After the correlation is initialized, subsequent <xref:System.ServiceModel.Activities.Send> activities can use the <xref:System.ServiceModel.Activities.CorrelationHandle> to invoke methods on the same service instance.</span></span>  
  
```csharp  
Send request2 = new Send  
{  
    CorrelatesWith = cchandle,  
    // Remaining activity configuration omitted.  
};  
```  
  
 <span data-ttu-id="98a8b-127">Notez que dans ces exemples, la corrélation de contexte a été configurée de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="98a8b-127">Note that in these examples, the context correlation has been explicitly configured.</span></span> <span data-ttu-id="98a8b-128">Si le workflow client n'est pas également hébergé dans un <xref:System.ServiceModel.Activities.WorkflowServiceHost>, la corrélation doit être configurée de manière explicite, sauf si les activités sont contenues dans une activité <xref:System.ServiceModel.Activities.CorrelationScope>.</span><span class="sxs-lookup"><span data-stu-id="98a8b-128">If the client workflow is not also hosted in a <xref:System.ServiceModel.Activities.WorkflowServiceHost>, then correlation must be explicitly configured, unless the activities are contained within a <xref:System.ServiceModel.Activities.CorrelationScope> activity.</span></span> <span data-ttu-id="98a8b-129">Pour plus d’informations sur la corrélation de contexte, consultez le [NetContextExchangeCorrelation](https://msdn.microsoft.com/library/93c74a1a-b9e2-46c6-95c0-c9b0e9472caf) exemple.</span><span class="sxs-lookup"><span data-stu-id="98a8b-129">For more information about context correlation, see the [NetContextExchangeCorrelation](https://msdn.microsoft.com/library/93c74a1a-b9e2-46c6-95c0-c9b0e9472caf) sample.</span></span>  
  
 <span data-ttu-id="98a8b-130">Si le client qui appelle le service de workflow n'est pas un workflow, il peut toujours répéter ses appels, à condition de retransmettre de manière explicite le contexte retourné par le premier appel au service de workflow.</span><span class="sxs-lookup"><span data-stu-id="98a8b-130">If the client that is making calls to the workflow service is not a workflow, then it can still make repeated calls as long as it explicitly passes back the context that is returned from the first call to the workflow service.</span></span> <span data-ttu-id="98a8b-131">Les proxys générés en ajoutant une référence de service dans [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] stockent et transmettent ce contexte par défaut.</span><span class="sxs-lookup"><span data-stu-id="98a8b-131">Proxies generated by adding a service reference in [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] store and pass this context by default.</span></span>
