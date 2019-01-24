---
title: Traitement ordonné des messages en mode de concurrence simple
ms.date: 03/30/2017
ms.assetid: a90f5662-a796-46cd-ae33-30a4072838af
ms.openlocfilehash: c9f2460a1def19212d3ba866b0b443830e9b69bb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745845"
---
# <a name="ordered-processing-of-messages-in-single-concurrency-mode"></a><span data-ttu-id="eb9d5-102">Traitement ordonné des messages en mode de concurrence simple</span><span class="sxs-lookup"><span data-stu-id="eb9d5-102">Ordered Processing of Messages in Single Concurrency Mode</span></span>
<span data-ttu-id="eb9d5-103">WCF n’offre aucune garantie concernant l’ordre dans lequel les messages sont traités, à moins que le canal sous-jacent soit session.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-103">WCF makes no guarantees about the order in which messages are processed, unless the underlying channel is sessionful.</span></span>  <span data-ttu-id="eb9d5-104">Par exemple, un service WCF qui utilise MsmqInputChannel, qui n’est pas un canal de session, ne traite pas les messages dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-104">For instance, a WCF service that uses MsmqInputChannel, which is not a sessionful channel, will fail to process messages in order.</span></span> <span data-ttu-id="eb9d5-105">Il existe certains cas où un développeur peut le comportement de traitement dans l’ordre, mais pas souhaitent utiliser des sessions.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-105">There are some circumstances where a developer may want the in order processing behavior but not want to use sessions.</span></span> <span data-ttu-id="eb9d5-106">Cette rubrique décrit comment configurer ce comportement lorsqu'un service s'exécute en mode de concurrence simple.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-106">This topic describes how to configure this behavior when a service is running in Single Concurrency Mode.</span></span>  
  
## <a name="in-order-message-processing"></a><span data-ttu-id="eb9d5-107">Traitement des messages dans l'ordre</span><span class="sxs-lookup"><span data-stu-id="eb9d5-107">In-order Message Processing</span></span>  
 <span data-ttu-id="eb9d5-108">Un nouvel attribut nommé <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> a été ajouté à la classe <xref:System.ServiceModel.ServiceBehaviorAttribute>.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-108">A new attribute called <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> has been added to the <xref:System.ServiceModel.ServiceBehaviorAttribute>.</span></span> <span data-ttu-id="eb9d5-109">Lorsque <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> a la valeur true et <xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> a la valeur <xref:System.ServiceModel.ConcurrencyMode.Single> les messages envoyés au service sont traités dans l'ordre.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-109">When <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> is set to true and <xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> is set to <xref:System.ServiceModel.ConcurrencyMode.Single> messages sent to the service will be processed in order.</span></span> <span data-ttu-id="eb9d5-110">L'extrait de code suivant illustre comment définir ces attributs.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-110">The following code snippet illustrates how to set these attributes.</span></span>  
  
```  
[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single, EnsureOrderedDispatch = true )]  
    class Service : IService  
    {  
         // ...  
    }  
```  
  
 <span data-ttu-id="eb9d5-111">Si une autre valeur est affectée à la propriété <xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A>, une exception <xref:System.InvalidOperationException> est levée.</span><span class="sxs-lookup"><span data-stu-id="eb9d5-111">If <xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> is set to any other value, an <xref:System.InvalidOperationException> is thrown.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb9d5-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb9d5-112">See also</span></span>
- [<span data-ttu-id="eb9d5-113">Sessions, instanciation et accès concurrentiel</span><span class="sxs-lookup"><span data-stu-id="eb9d5-113">Sessions, Instancing, and Concurrency</span></span>](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)
- [<span data-ttu-id="eb9d5-114">Concurrence</span><span class="sxs-lookup"><span data-stu-id="eb9d5-114">Concurrency</span></span>](../../../../docs/framework/wcf/samples/concurrency.md)
