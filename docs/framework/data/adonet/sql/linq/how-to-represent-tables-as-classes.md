---
title: 'Procédure : Représentent les Tables en tant que Classes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 84dda12b-88a2-4cd2-92b3-8db87b28d14c
ms.openlocfilehash: 307356e056aae29af7c8ceafae0ca02604658aab
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54509608"
---
# <a name="how-to-represent-tables-as-classes"></a>Procédure : Représentent les Tables en tant que Classes
Utilisez le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.TableAttribute> attribut pour désigner une classe comme classe d’entité associée à une table de base de données.  
  
### <a name="to-map-a-class-to-a-database-table"></a>Pour mapper une classe à une table de base de données  
  
-   Ajoutez l'attribut <xref:System.Data.Linq.Mapping.TableAttribute> à la déclaration de classe.  
  
## <a name="example"></a>Exemple  
 Le code suivant établit la classe `Customer` comme une classe d'entité associée à la table de base de données `Customers`.  
  
 [!code-csharp[DLinqCustomize#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCustomize/cs/Program.cs#1)]
 [!code-vb[DLinqCustomize#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCustomize/vb/Module1.vb#1)]  
  
 Il n'est pas nécessaire de spécifier la propriété <xref:System.Data.Linq.Mapping.TableAttribute.Name%2A> si le nom peut être déduit. Si vous ne spécifiez pas de nom, on considère qu'il s'agit du même nom que pour la propriété ou le champ.  
  
## <a name="see-also"></a>Voir aussi
- [Modèle objet LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [Guide pratique pour Personnaliser des Classes d’entité à l’aide de l’éditeur de Code](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
