---
title: 'Procédure : Créer un contrat Windows Communication Foundation avec une classe'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1ad69393-3915-4e7f-9b91-b6fc59c6f5ba
ms.openlocfilehash: b32d4feb03daac33af8b7ca3b533a0b7013bb090
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54658924"
---
# <a name="how-to-create-a-windows-communication-foundation-contract-with-a-class"></a>Procédure : Créer un contrat Windows Communication Foundation avec une classe
Le meilleur moyen de la création d’un contrat Windows Communication Foundation (WCF) est à l’aide d’une interface. Pour plus d'informations, voir [Procédure : Définir un contrat de Service](../../../../docs/framework/wcf/how-to-define-a-wcf-service-contract.md). Une autre solution, présentée dans cette rubrique, consiste à créer une classe, à appliquer l'attribut <xref:System.ServiceModel.ServiceContractAttribute> directement sur celle-ci, puis l'attribut <xref:System.ServiceModel.OperationContractAttribute> sur chacune des méthodes de la classe qui font partie du contrat.  
  
> [!WARNING]
>  `[ServiceContract]` et `[ServiceContractAttribute]` produisent le même résultat. La même chose vaut pour `[OperationContract]` et `[OperationContractAttribute]`. Dans chaque cas, le précédent est abrégé pour cette dernière.  
  
 Pour plus d’informations sur les contrats de service, consultez [Designing Service Contracts](../../../../docs/framework/wcf/designing-service-contracts.md).  
  
### <a name="creating-a-windows-communication-foundation-contract-with-a-class"></a>Création d'un contrat Windows Communication Foundation à l'aide d'une classe  
  
1.  Créer une nouvelle classe à l’aide de Visual Basic, C#, ou n’importe quel autre langage common language runtime.  
  
2.  Appliquez la classe <xref:System.ServiceModel.ServiceContractAttribute> à la classe.  
  
3.  Créez des méthodes dans la classe.  
  
4.  Appliquer le <xref:System.ServiceModel.OperationContractAttribute> classe pour chaque méthode qui doit être exposé en tant que partie du contrat WCF public.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant présente une classe qui définit un contrat de service.  
  
 [!code-csharp[c_HowTo_CreateContractWithClass#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createcontractwithclass/cs/source.cs#1)]
 [!code-vb[c_HowTo_CreateContractWithClass#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_createcontractwithclass/vb/source.vb#1)]  
  
 Les méthodes auxquelles la classe <xref:System.ServiceModel.OperationContractAttribute> est appliquée utilisent un modèle de message demande-réponse par défaut. Pour plus d’informations sur ce modèle de message, consultez [Comment : Créer un contrat demande-réponse](../../../../docs/framework/wcf/feature-details/how-to-create-a-request-reply-contract.md). Vous pouvez également créer et utiliser d’autres modèles de message en définissant les propriétés de l’attribut. Pour plus d'exemples, consultez [Procédure : Créer un contrat unidirectionnel](../../../../docs/framework/wcf/feature-details/how-to-create-a-one-way-contract.md) et [Comment : Créer un contrat Duplex](../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>
