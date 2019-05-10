---
title: 'Procédure : Appeler des opérations de Service WCF de façon asynchrone'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 0face17f-43ca-417b-9b33-737c0fc360df
ms.openlocfilehash: aba41d707426f29c2bcd626dbbe13d16d9e1b1f7
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64624508"
---
# <a name="how-to-call-wcf-service-operations-asynchronously"></a><span data-ttu-id="65fb8-102">Procédure : Appeler des opérations de Service WCF de façon asynchrone</span><span class="sxs-lookup"><span data-stu-id="65fb8-102">How to: Call WCF Service Operations Asynchronously</span></span>
<span data-ttu-id="65fb8-103">Cette rubrique présente comment un client peut accéder de façon asynchrone à une opération de service.</span><span class="sxs-lookup"><span data-stu-id="65fb8-103">This topic covers how a client can access a service operation asynchronously.</span></span> <span data-ttu-id="65fb8-104">Le service dans cette rubrique implémente l'interface `ICalculator`.</span><span class="sxs-lookup"><span data-stu-id="65fb8-104">The service in this topic implements the `ICalculator` interface.</span></span> <span data-ttu-id="65fb8-105">Le client peut appeler les opérations sur cette interface de manière asynchrone à l'aide du modèle d'appel asynchrone commandé par événement.</span><span class="sxs-lookup"><span data-stu-id="65fb8-105">The client can call the operations on this interface asynchronously by using the event-driven asynchronous calling model.</span></span> <span data-ttu-id="65fb8-106">(Pour plus d’informations sur le modèle d’appel asynchrone basé sur des événements, consultez [programmation multithread avec le modèle asynchrone basé sur événement](https://go.microsoft.com/fwlink/?LinkId=248184)).</span><span class="sxs-lookup"><span data-stu-id="65fb8-106">(For more information about the event-based asynchronous calling model, see [Multithreaded Programming with the Event-based Asynchronous Pattern](https://go.microsoft.com/fwlink/?LinkId=248184)).</span></span> <span data-ttu-id="65fb8-107">Pour obtenir un exemple qui montre comment implémenter une opération de façon asynchrone dans un service, consultez [Comment : Implémenter une opération de Service asynchrone](../../../../docs/framework/wcf/how-to-implement-an-asynchronous-service-operation.md).</span><span class="sxs-lookup"><span data-stu-id="65fb8-107">For an example that shows how to implement an operation asynchronously in a service, see [How to: Implement an Asynchronous Service Operation](../../../../docs/framework/wcf/how-to-implement-an-asynchronous-service-operation.md).</span></span> <span data-ttu-id="65fb8-108">Pour plus d’informations sur les opérations synchrones et asynchrones, consultez [synchrone et opérations asynchrones](../../../../docs/framework/wcf/synchronous-and-asynchronous-operations.md).</span><span class="sxs-lookup"><span data-stu-id="65fb8-108">For more information about synchronous and asynchronous operations, see [Synchronous and Asynchronous Operations](../../../../docs/framework/wcf/synchronous-and-asynchronous-operations.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="65fb8-109">Le modèle d'appel asynchrone commandé par événement n'est pas pris en charge lorsqu'il utilise un <xref:System.ServiceModel.ChannelFactory%601>.</span><span class="sxs-lookup"><span data-stu-id="65fb8-109">The event-driven asynchronous calling model is not supported when using a <xref:System.ServiceModel.ChannelFactory%601>.</span></span> <span data-ttu-id="65fb8-110">Pour plus d’informations sur les appels asynchrones à l’aide de la <xref:System.ServiceModel.ChannelFactory%601>, consultez [Comment : Appeler des opérations de façon asynchrone à l’aide d’une fabrique de canaux](../../../../docs/framework/wcf/feature-details/how-to-call-operations-asynchronously-using-a-channel-factory.md).</span><span class="sxs-lookup"><span data-stu-id="65fb8-110">For information about making asynchronous calls using the <xref:System.ServiceModel.ChannelFactory%601>, see [How to: Call Operations Asynchronously Using a Channel Factory](../../../../docs/framework/wcf/feature-details/how-to-call-operations-asynchronously-using-a-channel-factory.md).</span></span>  
  
## <a name="procedure"></a><span data-ttu-id="65fb8-111">Procédure</span><span class="sxs-lookup"><span data-stu-id="65fb8-111">Procedure</span></span>  
  
#### <a name="to-call-wcf-service-operations-asynchronously"></a><span data-ttu-id="65fb8-112">Pour appeler des opérations de service WCF de façon asynchrone</span><span class="sxs-lookup"><span data-stu-id="65fb8-112">To call WCF service operations asynchronously</span></span>  
  
1. <span data-ttu-id="65fb8-113">Exécutez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) outil avec les deux le `/async` et le `/tcv:Version35` commande options ensemble, comme indiqué dans la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="65fb8-113">Run the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) tool with both the `/async` and the `/tcv:Version35` command options together as shown in the following command.</span></span>  
  
    ```  
    svcutil /n:http://Microsoft.ServiceModel.Samples,Microsoft.ServiceModel.Samples http://localhost:8000/servicemodelsamples/service/mex /a /tcv:Version35  
    ```  
  
     <span data-ttu-id="65fb8-114">Cette opération génère en plus les opérations synchrones et standards en fonction de délégué asynchrones, une classe de client WCF qui contient :</span><span class="sxs-lookup"><span data-stu-id="65fb8-114">This generates, in addition to the synchronous and standard delegate-based asynchronous operations, a WCF client class that contains:</span></span>  
  
    - <span data-ttu-id="65fb8-115">Deux <`operationName` > `Async` opérations pour une utilisation avec l’approche appel asynchrone basé sur des événements.</span><span class="sxs-lookup"><span data-stu-id="65fb8-115">Two <`operationName`>`Async` operations for use with the event-based asynchronous calling approach.</span></span> <span data-ttu-id="65fb8-116">Exemple :</span><span class="sxs-lookup"><span data-stu-id="65fb8-116">For example:</span></span>  
  
         [!code-csharp[EventAsync#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/eventasync/cs/generatedclient.cs#1)]
         [!code-vb[EventAsync#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/eventasync/vb/generatedclient.vb#1)]  
  
    - <span data-ttu-id="65fb8-117">Événements terminés d’opérations sous la forme <`operationName` > `Completed` pour une utilisation avec l’approche appel asynchrone basé sur des événements.</span><span class="sxs-lookup"><span data-stu-id="65fb8-117">Operation completed events of the form <`operationName`>`Completed` for use with the event-based asynchronous calling approach.</span></span> <span data-ttu-id="65fb8-118">Exemple :</span><span class="sxs-lookup"><span data-stu-id="65fb8-118">For example:</span></span>  
  
         [!code-csharp[EventAsync#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/eventasync/cs/generatedclient.cs#2)]
         [!code-vb[EventAsync#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/eventasync/vb/generatedclient.vb#2)]  
  
    - <span data-ttu-id="65fb8-119"><xref:System.EventArgs?displayProperty=nameWithType> types pour chaque opération (sous la forme <`operationName`>`CompletedEventArgs`) pour une utilisation avec l’approche appel asynchrone basé sur des événements.</span><span class="sxs-lookup"><span data-stu-id="65fb8-119"><xref:System.EventArgs?displayProperty=nameWithType> types for each operation (of the form <`operationName`>`CompletedEventArgs`) for use with the event-based asynchronous calling approach.</span></span> <span data-ttu-id="65fb8-120">Exemple :</span><span class="sxs-lookup"><span data-stu-id="65fb8-120">For example:</span></span>  
  
         [!code-csharp[EventAsync#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/eventasync/cs/generatedclient.cs#3)]
         [!code-vb[EventAsync#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/eventasync/vb/generatedclient.vb#3)]  
  
2. <span data-ttu-id="65fb8-121">Dans l'application d'appel, créez une méthode de rappel à appeler au terme de l'opération asynchrone en vous conformant à l'exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="65fb8-121">In the calling application, create a callback method to be called when the asynchronous operation is complete, as shown in the following sample code.</span></span>  
  
     [!code-csharp[EventAsync#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/eventasync/cs/client.cs#4)]
     [!code-vb[EventAsync#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/eventasync/vb/client.vb#4)]  
  
3. <span data-ttu-id="65fb8-122">Avant d’appeler l’opération, utilisez un nouveau générique <xref:System.EventHandler%601?displayProperty=nameWithType> de type <`operationName` > `EventArgs` pour ajouter la méthode de gestionnaire (créée à l’étape précédente) à la <`operationName` > `Completed` événement.</span><span class="sxs-lookup"><span data-stu-id="65fb8-122">Prior to calling the operation, use a new generic <xref:System.EventHandler%601?displayProperty=nameWithType> of type <`operationName`>`EventArgs` to add the handler method (created in the preceding step) to the <`operationName`>`Completed` event.</span></span> <span data-ttu-id="65fb8-123">Appelez ensuite la <`operationName` > `Async` (méthode).</span><span class="sxs-lookup"><span data-stu-id="65fb8-123">Then call the <`operationName`>`Async` method.</span></span> <span data-ttu-id="65fb8-124">Exemple :</span><span class="sxs-lookup"><span data-stu-id="65fb8-124">For example:</span></span>  
  
     [!code-csharp[EventAsync#5](../../../../samples/snippets/csharp/VS_Snippets_CFX/eventasync/cs/client.cs#5)]
     [!code-vb[EventAsync#5](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/eventasync/vb/client.vb#5)]  
  
## <a name="example"></a><span data-ttu-id="65fb8-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="65fb8-125">Example</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="65fb8-126">Les règles de conception pour le modèle asynchrone basé sur les événements stipulent que si plusieurs valeurs sont retournées, une valeur est retournée comme la propriété `Result` et les autres sont retournées comme les propriétés sur l'objet <xref:System.EventArgs>.</span><span class="sxs-lookup"><span data-stu-id="65fb8-126">The design guidelines for the event-based asynchronous model state that if more than one value is returned, one value is returned as the `Result` property and the others are returned as properties on the <xref:System.EventArgs> object.</span></span> <span data-ttu-id="65fb8-127">Il en découle que si un client importe des métadonnées à l'aide des options de commande asynchrone basées sur les événements et que l'opération retourne plusieurs valeurs, l'objet <xref:System.EventArgs> par défaut retourne une valeur comme la propriété `Result` et le reste sont des propriétés de l'objet <xref:System.EventArgs>. Pour recevoir l'objet message comme la propriété `Result` et que les valeurs retournées sur cet objet soient des propriétés, utilisez l'option de commande `/messageContract`.</span><span class="sxs-lookup"><span data-stu-id="65fb8-127">One result of this is that if a client imports metadata using the event-based asynchronous command options and the operation returns more than one value, the default <xref:System.EventArgs> object returns one value as the `Result` property and the remainder are properties of the <xref:System.EventArgs> object.If you want to receive the message object as the `Result` property and have the returned values as properties on that object, use the `/messageContract` command option.</span></span> <span data-ttu-id="65fb8-128">Cette opération génère une signature qui retourne le message de réponse comme la propriété `Result` sur l'objet <xref:System.EventArgs>.</span><span class="sxs-lookup"><span data-stu-id="65fb8-128">This generates a signature that returns the response message as the `Result` property on the <xref:System.EventArgs> object.</span></span> <span data-ttu-id="65fb8-129">Toutes les valeurs de retour internes sont ensuite des propriétés de l'objet de message de réponse.</span><span class="sxs-lookup"><span data-stu-id="65fb8-129">All internal return values are then properties of the response message object.</span></span>  
  
 [!code-csharp[EventAsync#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/eventasync/cs/client.cs#6)]
 [!code-vb[EventAsync#6](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/eventasync/vb/client.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="65fb8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65fb8-130">See also</span></span>

- [<span data-ttu-id="65fb8-131">Guide pratique pour Implémenter une opération de Service asynchrone</span><span class="sxs-lookup"><span data-stu-id="65fb8-131">How to: Implement an Asynchronous Service Operation</span></span>](../../../../docs/framework/wcf/how-to-implement-an-asynchronous-service-operation.md)
