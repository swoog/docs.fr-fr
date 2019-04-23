---
title: 'Procédure : Représenter des colonnes en tant que colonnes générées par une base de données'
ms.date: 03/30/2017
ms.assetid: 6524b8a6-e5d2-4a3b-8e08-beafc4a84fd2
ms.openlocfilehash: 2803697c668a8e1dbbeb426ea41b64878f70c145
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59307910"
---
# <a name="how-to-represent-columns-as-database-generated"></a><span data-ttu-id="3466e-102">Procédure : Représenter des colonnes en tant que colonnes générées par une base de données</span><span class="sxs-lookup"><span data-stu-id="3466e-102">How to: Represent Columns as Database-Generated</span></span>
<span data-ttu-id="3466e-103">Utilisez le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> propriété sur le <xref:System.Data.Linq.Mapping.ColumnAttribute> attribut pour désigner un champ ou une propriété comme représentant d’une colonne de base de données générée.</span><span class="sxs-lookup"><span data-stu-id="3466e-103">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> property on the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute to designate a field or property as representing a database-generated column.</span></span>  
  
 <span data-ttu-id="3466e-104">Pour obtenir des exemples de code, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A>.</span><span class="sxs-lookup"><span data-stu-id="3466e-104">For code examples, see <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A>.</span></span>  
  
### <a name="to-designate-a-field-or-property-as-representing-a-database-generated-column"></a><span data-ttu-id="3466e-105">Pour désigner un champ ou une propriété comme représentant d'une colonne générée par une base de données</span><span class="sxs-lookup"><span data-stu-id="3466e-105">To designate a field or property as representing a database-generated column</span></span>  
  
1. <span data-ttu-id="3466e-106">Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span><span class="sxs-lookup"><span data-stu-id="3466e-106">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2. <span data-ttu-id="3466e-107">Affectez la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="3466e-107">Set the property value to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3466e-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3466e-108">See also</span></span>

- [<span data-ttu-id="3466e-109">Modèle objet LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="3466e-109">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [<span data-ttu-id="3466e-110">Guide pratique pour Personnaliser des Classes d’entité à l’aide de l’éditeur de Code</span><span class="sxs-lookup"><span data-stu-id="3466e-110">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
