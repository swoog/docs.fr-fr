---
title: 'Procédure : Représentent les colonnes en tant que Timestamp ou Version'
ms.date: 03/30/2017
ms.assetid: 5afd5ce8-1d20-4bc3-a34f-49d95449f493
ms.openlocfilehash: fa9ffe01c45df3ce0342b62e12007ddf88ee412d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54674568"
---
# <a name="how-to-represent-columns-as-timestamp-or-version-columns"></a><span data-ttu-id="29b98-102">Procédure : Représentent les colonnes en tant que Timestamp ou Version</span><span class="sxs-lookup"><span data-stu-id="29b98-102">How to: Represent Columns as Timestamp or Version Columns</span></span>
<span data-ttu-id="29b98-103">Utilisez le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> propriété de la <xref:System.Data.Linq.Mapping.ColumnAttribute> attribut pour désigner un champ ou une propriété comme représentant d’une colonne de base de données qui contient les numéros de version ou les horodateurs de base de données.</span><span class="sxs-lookup"><span data-stu-id="29b98-103">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> property of the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute to designate a field or property as representing a database column that holds database timestamps or version numbers.</span></span>  
  
 <span data-ttu-id="29b98-104">Pour obtenir des exemples de code, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A>.</span><span class="sxs-lookup"><span data-stu-id="29b98-104">For code examples, see <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A>.</span></span>  
  
### <a name="to-designate-a-field-or-property-as-representing-a-timestamp-or-version-column"></a><span data-ttu-id="29b98-105">Pour désigner un champ ou une propriété comme représentant d'une colonne timestamp ou version</span><span class="sxs-lookup"><span data-stu-id="29b98-105">To designate a field or property as representing a timestamp or version column</span></span>  
  
1.  <span data-ttu-id="29b98-106">Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span><span class="sxs-lookup"><span data-stu-id="29b98-106">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2.  <span data-ttu-id="29b98-107">Affectez la valeur <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> à la propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="29b98-107">Set the <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A> property value to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29b98-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29b98-108">See also</span></span>
- [<span data-ttu-id="29b98-109">Modèle objet LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="29b98-109">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [<span data-ttu-id="29b98-110">Guide pratique pour Spécifier que les membres qui doivent être vérifiés pour les conflits d’accès concurrentiel</span><span class="sxs-lookup"><span data-stu-id="29b98-110">How to: Specify Which Members are Tested for Concurrency Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-specify-which-members-are-tested-for-concurrency-conflicts.md)
- [<span data-ttu-id="29b98-111">Guide pratique pour Personnaliser des Classes d’entité à l’aide de l’éditeur de Code</span><span class="sxs-lookup"><span data-stu-id="29b98-111">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
