---
title: 'Procédure : Représenter des colonnes comme autorisant les valeurs Null'
ms.date: 03/30/2017
ms.assetid: ebb71a37-1f4c-4fa7-b2d2-d903f13c4af1
ms.openlocfilehash: ba362e45c8694dbb30e977b3d9f25702ee9dea48
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715528"
---
# <a name="how-to-represent-columns-as-allowing-null-values"></a>Procédure : Représenter des colonnes comme autorisant les valeurs Null
Utilisez le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A> propriété sur le <xref:System.Data.Linq.Mapping.ColumnAttribute> attribut pour spécifier que la colonne de base de données associée peut contenir des valeurs null.  
  
 Pour obtenir des exemples de code, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A>.  
  
### <a name="to-designate-a-column-as-allowing-null-values"></a>Pour désigner une colonne comme autorisant des valeurs null  
  
1.  Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.  
  
2.  Affectez la valeur <xref:System.Data.Linq.Mapping.ColumnAttribute.CanBeNull%2A> à la propriété `true`.  
  
## <a name="see-also"></a>Voir aussi
- [Modèle objet LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [Guide pratique pour Personnaliser des Classes d’entité à l’aide de l’éditeur de Code](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
