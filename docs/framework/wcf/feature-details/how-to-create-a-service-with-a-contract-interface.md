---
title: 'Comment : créer un service avec une interface de contrat'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7b6803f6-d6f9-4cc2-9f1b-6f4c920475d5
ms.openlocfilehash: 796870b80ed72db2353e79db3e4e3fc164c22875
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33489792"
---
# <a name="how-to-create-a-service-with-a-contract-interface"></a>Comment : créer un service avec une interface de contrat
Il est préférable de créer un contrat Windows Communication Foundation (WCF) à l’aide d’une interface. Ce contrat spécifie la collection et la structure des messages requis pour accéder aux opérations offertes par le service. Cette interface définit les types d'entrée et de sortie en appliquant la classe <xref:System.ServiceModel.ServiceContractAttribute> à l'interface et la classe <xref:System.ServiceModel.OperationContractAttribute> aux méthodes que vous souhaitez exposer.  
  
 Pour plus d’informations sur les contrats de service, consultez [concevoir des contrats de Service](../../../../docs/framework/wcf/designing-service-contracts.md).  
  
### <a name="creating-a-wcf-contract-with-an-interface"></a>Création d'un contrat WCF avec une interface  
  
1.  Créer une nouvelle interface à l’aide de Visual Basic, c# ou tout autre langage common language runtime.  
  
2.  Appliquez la classe <xref:System.ServiceModel.ServiceContractAttribute> à l'interface.  
  
3.  Définissez les méthodes dans l'interface.  
  
4.  Appliquer la <xref:System.ServiceModel.OperationContractAttribute> classe pour chaque méthode qui doit être exposé en tant que partie du contrat public WCF.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant présente une interface qui définit un contrat de service.  
  
 [!code-csharp[c_HowTo_CreateContractWithInterface#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createcontractwithinterface/cs/source.cs#1)]
 [!code-vb[c_HowTo_CreateContractWithInterface#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_createcontractwithinterface/vb/source.vb#1)]  
  
 Les méthodes auxquelles la classe <xref:System.ServiceModel.OperationContractAttribute> est appliquée utilisent un modèle de message demande-réponse par défaut. Pour plus d’informations sur ce modèle de message, consultez [Comment : créer un contrat demande-réponse](../../../../docs/framework/wcf/feature-details/how-to-create-a-request-reply-contract.md). Vous pouvez également créer et utiliser d’autres modèles de message en définissant les propriétés de l’attribut. Pour plus d’exemples, consultez [Comment : créer un contrat unidirectionnel](../../../../docs/framework/wcf/feature-details/how-to-create-a-one-way-contract.md) et [Comment : créer un contrat Duplex](../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.ServiceContractAttribute>  
 <xref:System.ServiceModel.OperationContractAttribute>
