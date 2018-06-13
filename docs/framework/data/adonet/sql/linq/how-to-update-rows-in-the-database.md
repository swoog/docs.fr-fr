---
title: 'Comment : mettre à jour des lignes dans la base de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: a2b5c90f-6cc3-4128-bfab-1db488d5af26
ms.openlocfilehash: b1e993aeb510d34e76d91cfd5222ef190d554846
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33363752"
---
# <a name="how-to-update-rows-in-the-database"></a>Comment : mettre à jour des lignes dans la base de données
Vous pouvez mettre à jour les lignes dans une base de données en modifiant les valeurs de membre des objets associés à la [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Table%601> collection et en soumettant les modifications apportées à la base de données. [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] traduit vos modifications dans la requête SQL appropriée `UPDATE` commandes.  
  
> [!NOTE]
>  Vous pouvez substituer des méthodes par défaut [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] pour les opérations `Insert`, `Update` et `Delete` sur les bases de données. Pour plus d’informations, consultez [personnalisation des opérations d’insertion, mise à jour et supprimer](../../../../../../docs/framework/data/adonet/sql/linq/customizing-insert-update-and-delete-operations.md).  
>   
>  Les développeurs à l’aide de Visual Studio peuvent utiliser le [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] pour développer des procédures stockées dans le même but.  
  
 Les étapes suivantes supposent qu'un <xref:System.Data.Linq.DataContext> valide vous connecte à la base de données Northwind. Pour plus d’informations, consultez [Comment : se connecter à une base de données](../../../../../../docs/framework/data/adonet/sql/linq/how-to-connect-to-a-database.md).  
  
### <a name="to-update-a-row-in-the-database"></a>Pour mettre à jour une ligne dans la base de données  
  
1.  Interrogez la base de données concernant la ligne à mettre à jour.  
  
2.  Apportez les modifications souhaitées aux valeurs de membre dans l'objet [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] obtenu.  
  
3.  Soumettez les modifications à la base de données.  
  
## <a name="example"></a>Exemple  
 L'exemple suivant interroge la base de données concernant la commande 11000, puis modifie les valeurs de `ShipName` et `ShipVia` dans l'objet `Order` obtenu. Enfin, les modifications apportées à ces valeurs de membre sont soumises à la base de données comme modifications dans les colonnes `ShipName` et `ShipVia`.  
  
 [!code-csharp[System.Data.Linq.Table#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.table/cs/program.cs#2)]
 [!code-vb[System.Data.Linq.Table#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.table/vb/module1.vb#2)]  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour gérer les conflits de changement](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)  
 [Comment : assigner des procédures stockées pour effectuer des mises à jour, insertions et suppressions (Concepteur O/R)](/visualstudio/data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer)  
 [Apport et soumission de modifications de données](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
