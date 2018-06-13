---
title: 'Comment : représenter les clés primaires'
ms.date: 03/30/2017
ms.assetid: 63c65289-6539-42b2-8493-891c232018fa
ms.openlocfilehash: dae8603a18318f45182c7148b10b8194e67fd017
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33352588"
---
# <a name="how-to-represent-primary-keys"></a>Comment : représenter les clés primaires
Utilisez le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A> propriété sur le <xref:System.Data.Linq.Mapping.ColumnAttribute> attribut pour désigner une propriété ou un champ pour représenter la clé primaire pour une colonne de base de données.  
  
 Pour obtenir des exemples de code, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A>.  
  
> [!NOTE]
>  [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] ne prend pas en charge les colonnes calculées en tant que clés primaires.  
  
### <a name="to-designate-a-property-or-field-as-a-primary-key"></a>Pour désigner une propriété ou un champ comme clé primaire  
  
1.  Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.  
  
2.  Affectez la valeur `true`.  
  
## <a name="see-also"></a>Voir aussi  
 [Modèle objet LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)  
 [Guide pratique pour personnaliser des classes d’entité à l’aide de l’éditeur de code](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
