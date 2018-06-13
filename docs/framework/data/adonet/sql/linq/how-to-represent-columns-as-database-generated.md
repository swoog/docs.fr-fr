---
title: 'Comment : représenter des colonnes en tant que colonnes générées par une base de données'
ms.date: 03/30/2017
ms.assetid: 6524b8a6-e5d2-4a3b-8e08-beafc4a84fd2
ms.openlocfilehash: f6b127208ae359b43f273f54d7b5c72933c2eba6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33353739"
---
# <a name="how-to-represent-columns-as-database-generated"></a><span data-ttu-id="2b946-102">Comment : représenter des colonnes en tant que colonnes générées par une base de données</span><span class="sxs-lookup"><span data-stu-id="2b946-102">How to: Represent Columns as Database-Generated</span></span>
<span data-ttu-id="2b946-103">Utilisez le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> propriété sur le <xref:System.Data.Linq.Mapping.ColumnAttribute> attribut pour désigner un champ ou une propriété comme représentant d’une colonne de base de données générée.</span><span class="sxs-lookup"><span data-stu-id="2b946-103">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> property on the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute to designate a field or property as representing a database-generated column.</span></span>  
  
 <span data-ttu-id="2b946-104">Pour obtenir des exemples de code, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A>.</span><span class="sxs-lookup"><span data-stu-id="2b946-104">For code examples, see <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A>.</span></span>  
  
### <a name="to-designate-a-field-or-property-as-representing-a-database-generated-column"></a><span data-ttu-id="2b946-105">Pour désigner un champ ou une propriété comme représentant d'une colonne générée par une base de données</span><span class="sxs-lookup"><span data-stu-id="2b946-105">To designate a field or property as representing a database-generated column</span></span>  
  
1.  <span data-ttu-id="2b946-106">Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span><span class="sxs-lookup"><span data-stu-id="2b946-106">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2.  <span data-ttu-id="2b946-107">Affectez la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="2b946-107">Set the property value to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b946-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b946-108">See Also</span></span>  
 [<span data-ttu-id="2b946-109">Modèle objet LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="2b946-109">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)  
 [<span data-ttu-id="2b946-110">Guide pratique pour personnaliser des classes d’entité à l’aide de l’éditeur de code</span><span class="sxs-lookup"><span data-stu-id="2b946-110">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
