---
title: 'Procédure : appeler des opérations de façon asynchrone à l’aide d’une fabrique de canaux'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: cc17dd47-b9ad-451c-a362-e36e0aac7ba0
ms.openlocfilehash: 17b6dd979f7554cd433cc1abcf2a4da8dd9b83cb
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59338915"
---
# <a name="how-to-call-operations-asynchronously-using-a-channel-factory"></a>Procédure : appeler des opérations de façon asynchrone à l’aide d’une fabrique de canaux
Cette rubrique décrit comment un client peut accéder de façon asynchrone à une opération de service lors de l'utilisation d'une application cliente basée sur <xref:System.ServiceModel.ChannelFactory%601>. (Lors de l'utilisation d'un objet <xref:System.ServiceModel.ClientBase%601?displayProperty=nameWithType> pour appeler un service, vous pouvez utiliser le modèle d'appel asynchrone commandé par événement. Pour plus d'informations, voir [Procédure : Appeler des opérations de Service de façon asynchrone](../../../../docs/framework/wcf/feature-details/how-to-call-wcf-service-operations-asynchronously.md). Pour plus d’informations sur le modèle d’appel asynchrone basé sur des événements, consultez [modèle asynchrone basé sur des événements (EAP)](../../../../docs/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-eap.md).)  
  
 Le service dans cette rubrique implémente l'interface `ICalculator`. Le client peut appeler les opérations sur cette interface de façon asynchrone, ce qui signifie que des opérations telles que `Add` sont divisées en deux méthodes : `BeginAdd` et `EndAdd`, la première initiant l'appel et la seconde récupérant le résultat au terme de l'opération. Pour obtenir un exemple montrant comment implémenter une opération de façon asynchrone dans un service, consultez [Comment : Implémenter une opération de Service asynchrone](../../../../docs/framework/wcf/how-to-implement-an-asynchronous-service-operation.md). Pour plus d’informations sur les opérations synchrones et asynchrones, consultez [synchrone et opérations asynchrones](../../../../docs/framework/wcf/synchronous-and-asynchronous-operations.md).  
  
## <a name="procedure"></a>Procédure  
  
#### <a name="to-call-wcf-service-operations-asynchronously"></a>Pour appeler des opérations de service WCF de façon asynchrone  
  
1. Exécutez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) outil avec la `/async` option comme illustré dans la commande suivante.  
  
    ```  
    svcutil /n:http://Microsoft.ServiceModel.Samples,Microsoft.ServiceModel.Samples http://localhost:8000/servicemodelsamples/service/mex /a  
    ```  
  
     Cela génère une version cliente asynchrone du contrat de service pour l'opération.  
  
2. Créez une fonction de rappel à appeler au terme de l'opération asynchrone en vous conformant à l'exemple de code suivant.  
  
     [!code-csharp[C_How_To_CF_Async#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_how_to_cf_async/cs/client.cs#2)]
     [!code-vb[C_How_To_CF_Async#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_how_to_cf_async/vb/client.vb#2)]  
  
3. Pour accéder de façon asynchrone à une opération de service, créez le client, puis appelez la méthode `Begin[Operation]` (par exemple, `BeginAdd`) et spécifiez une fonction de rappel en vous conformant à l'exemple de code suivant.  
  
     [!code-csharp[C_How_To_CF_Async#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_how_to_cf_async/cs/client.cs#3)]
     [!code-vb[C_How_To_CF_Async#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_how_to_cf_async/vb/client.vb#3)]  
  
     Lors de l'exécution de la fonction de rappel, le client appelle la méthode `End<operation>` (par exemple, `EndAdd`) pour récupérer le résultat.  
  
## <a name="example"></a>Exemple  
 Le service utilisé avec le code client utilisé dans la procédure précédente implémente l'interface `ICalculator` comme affiché dans le code suivant. Sur le côté service, le `Add` et `Subtract` opérations du contrat sont appelées de façon synchrone par le Windows Communication Foundation (WCF) l’exécution, même si les étapes clientes précédentes sont appelées de façon asynchrone sur le client. Les opérations `Multiply` et `Divide` sont utilisées pour appeler de façon asynchrone le service du côté service, même si le client les appelle de façon synchrone. Cet exemple affecte la propriété <xref:System.ServiceModel.OperationContractAttribute.AsyncPattern%2A> à `true`. Ce paramètre de propriété, ainsi que l'implémentation du modèle asynchrone du [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] indiquent au temps d'exécution d'appeler l'opération de façon asynchrone.  
  
 [!code-csharp[C_How_To_CF_Async#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_how_to_cf_async/cs/service.cs#4)]
 [!code-vb[C_How_To_CF_Async#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_how_to_cf_async/vb/service.vb#4)]  
