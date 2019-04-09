---
title: 'Procédure : contrôler l’instanciation des services'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e0b12b34-8004-443a-a46d-83a5c00f2601
ms.openlocfilehash: 1c1a08c702ab1bdc4579cb05359db1681e7203b9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59135016"
---
# <a name="how-to-control-service-instancing"></a>Procédure : contrôler l’instanciation des services
La définition du mode d'instance d'un service vous permet de spécifier quand un <xref:System.ServiceModel.InstanceContext?displayProperty=nameWithType> (et son objet de service associé, défini par l'utilisateur) est créé. Consultez l'énumération <xref:System.ServiceModel.InstanceContextMode> pour obtenir les modes possibles. Pour plus d’informations sur les comportements, consultez [configuration et extension de l’exécution des comportements](../../../../docs/framework/wcf/extending/configuring-and-extending-the-runtime-with-behaviors.md). Pour obtenir des exemples fonctionnels, consultez [comportements](../../../../docs/framework/wcf/samples/behaviors.md).  
  
### <a name="to-control-the-service-instance-lifetime-using-code"></a>Pour contrôler la durée de vie de l'instance de service en utilisant du code  
  
1.  Appliquez <xref:System.ServiceModel.ServiceBehaviorAttribute> à la classe de service.  
  
2.  Affectez à la propriété <xref:System.ServiceModel.ServiceBehaviorAttribute.InstanceContextMode%2A> l'une des valeurs suivantes : <xref:System.ServiceModel.InstanceContextMode.PerCall>, <xref:System.ServiceModel.InstanceContextMode.PerSession> ou <xref:System.ServiceModel.InstanceContextMode.Single>.  
  
     [!code-csharp[C_ControlServiceInstancing#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_controlserviceinstancing/cs/source.cs#1)]
     [!code-vb[C_ControlServiceInstancing#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_controlserviceinstancing/vb/source.vb#1)]  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant affecte à la propriété <xref:System.ServiceModel.ServiceBehaviorAttribute.InstanceContextMode%2A> de l'attribut <xref:System.ServiceModel.ServiceBehaviorAttribute> la valeur <xref:System.ServiceModel.InstanceContextMode.PerCall>.  
  
 [!code-csharp[c_ControlServiceInstancing#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_controlserviceinstancing/cs/source.cs#2)]
 [!code-vb[c_ControlServiceInstancing#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_controlserviceinstancing/vb/source.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.ServiceBehaviorAttribute>
- <xref:System.ServiceModel.ServiceBehaviorAttribute.InstanceContextMode%2A>
- <xref:System.ServiceModel.InstanceContextMode>
- [Service : Exemples de comportements](../samples/behaviors.md)
