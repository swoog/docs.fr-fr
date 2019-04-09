---
title: 'Procédure : Déclarer des erreurs dans les contrats de service'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e8da98e7-d22f-4f60-ac82-3fb0928a353f
ms.openlocfilehash: 90abb29550ce7e027244b220f30e9fe46e282ff3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59129491"
---
# <a name="how-to-declare-faults-in-service-contracts"></a>Procédure : Déclarer des erreurs dans les contrats de service
Dans le code managé, des exceptions sont levées en cas de conditions d'erreur. Dans les applications Windows Communication Foundation (WCF), toutefois, contrats de service spécifient les informations d’erreur sont retournées aux clients en déclarant des erreurs SOAP dans le contrat de service. Pour une vue d’ensemble de la relation entre les exceptions et erreurs, consultez [spécification et gestion des erreurs dans les contrats et Services](../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md).  
  
### <a name="create-a-service-contract-that-specifies-a-soap-fault"></a>Créer un contrat de service qui spécifie une erreur SOAP  
  
1.  Créez un contrat de service qui contient au moins une opération. Pour voir un exemple, consultez [Comment : Définir un contrat de Service](../../../docs/framework/wcf/how-to-define-a-wcf-service-contract.md).  
  
2.  Sélectionnez une opération qui peut spécifier une condition d'erreur dont les clients peuvent s'attendre à être notifiés. Pour déterminer les conditions d’erreur justifient de retourner des erreurs SOAP aux clients, consultez [spécification et gestion des erreurs dans les contrats et Services](../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md).  
  
3.  Appliquez <xref:System.ServiceModel.FaultContractAttribute?displayProperty=nameWithType> à l'opération sélectionnée et passez un type d'erreur sérialisable au constructeur. Pour plus d’informations sur la création et à l’aide de types sérialisables, consultez [Specifying Data Transfer in Service Contracts](../../../docs/framework/wcf/feature-details/specifying-data-transfer-in-service-contracts.md). L'exemple suivant montre comment spécifier que l'opération `SampleMethod` peut provoquer `GreetingFault`.  
  
     [!code-csharp[FaultContractAttribute#4](../../../samples/snippets/csharp/VS_Snippets_CFX/faultcontractattribute/cs/services.cs#4)]
     [!code-vb[FaultContractAttribute#4](../../../samples/snippets/visualbasic/VS_Snippets_CFX/faultcontractattribute/vb/services.vb#4)]  
  
4.  Répétez les étapes 2 et 3 pour toutes les opérations dans le contrat qui communiquent des conditions d'erreur aux clients.  
  
## <a name="implementing-an-operation-to-return-a-specified-soap-fault"></a>Implémentation d'une opération pour retourner une erreur SOAP spécifiée  
 Une fois qu'une opération a spécifié qu'une erreur SOAP spécifique peut être retournée (tel que dans la procédure précédente) pour communiquer une condition d'erreur à une application appelante, l'étape suivante consiste à implémenter cette spécification.  
  
#### <a name="throw-the-specified-soap-fault-in-the-operation"></a>Générer l'erreur SOAP spécifiée dans l'opération  
  
1.  Lorsqu’une condition d’erreur spécifique à <xref:System.ServiceModel.FaultContractAttribute> se produit dans une opération, levez une nouvelle <xref:System.ServiceModel.FaultException%601?displayProperty=nameWithType> où l’erreur SOAP spécifiée est le paramètre de type. L'exemple suivant montre comment générer `GreetingFault` dans le `SampleMethod` présenté dans la procédure précédente et dans la section de code suivante.  
  
     [!code-csharp[FaultContractAttribute#5](../../../samples/snippets/csharp/VS_Snippets_CFX/faultcontractattribute/cs/services.cs#5)]
     [!code-vb[FaultContractAttribute#5](../../../samples/snippets/visualbasic/VS_Snippets_CFX/faultcontractattribute/vb/services.vb#5)]  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant montre une implémentation d'une opération unique qui spécifie `GreetingFault` pour l'opération `SampleMethod`.  
  
 [!code-csharp[FaultContractAttribute#1](../../../samples/snippets/csharp/VS_Snippets_CFX/faultcontractattribute/cs/services.cs#1)]
 [!code-vb[FaultContractAttribute#1](../../../samples/snippets/visualbasic/VS_Snippets_CFX/faultcontractattribute/vb/services.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.FaultContractAttribute?displayProperty=nameWithType>
- <xref:System.ServiceModel.FaultException%601?displayProperty=nameWithType>
