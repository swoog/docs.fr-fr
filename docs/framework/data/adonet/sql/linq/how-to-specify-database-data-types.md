---
title: 'Procédure : Spécifier des types de données de base de données'
ms.date: 03/30/2017
ms.assetid: 2228fdad-7e6a-4b1b-b4d1-79d0198b7c28
ms.openlocfilehash: bf53463be8c715fd1c599efac1b19d838be19f86
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59218041"
---
# <a name="how-to-specify-database-data-types"></a><span data-ttu-id="bb559-102">Procédure : Spécifier des types de données de base de données</span><span class="sxs-lookup"><span data-stu-id="bb559-102">How to: Specify Database Data Types</span></span>
<span data-ttu-id="bb559-103">Utilisez le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> propriété sur un <xref:System.Data.Linq.Mapping.ColumnAttribute> attribut pour spécifier le texte exact qui définit la colonne dans une déclaration de table T-SQL.</span><span class="sxs-lookup"><span data-stu-id="bb559-103">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> property on a <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute to specify the exact text that defines the column in a T-SQL table declaration.</span></span>  
  
 <span data-ttu-id="bb559-104">Vous devez spécifier la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> uniquement si vous envisagez d'utiliser <xref:System.Data.Linq.DataContext.CreateDatabase%2A> pour créer une instance de la base de données.</span><span class="sxs-lookup"><span data-stu-id="bb559-104">You must specify the <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> property only if you plan to use <xref:System.Data.Linq.DataContext.CreateDatabase%2A> to create an instance of the database.</span></span>  
  
 <span data-ttu-id="bb559-105">Pour obtenir des exemples de code, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A>.</span><span class="sxs-lookup"><span data-stu-id="bb559-105">For code examples, see <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A>.</span></span>  
  
### <a name="to-specify-text-to-define-a-data-type-in-a-t-sql-table"></a><span data-ttu-id="bb559-106">Pour spécifier du texte afin de définir un type de données dans une table T-SQL</span><span class="sxs-lookup"><span data-stu-id="bb559-106">To specify text to define a data type in a T-SQL table</span></span>  
  
1.  <span data-ttu-id="bb559-107">Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span><span class="sxs-lookup"><span data-stu-id="bb559-107">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2.  <span data-ttu-id="bb559-108">Affectez la valeur de la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> au texte exact utilisé par T-SQL.</span><span class="sxs-lookup"><span data-stu-id="bb559-108">Set the value of the <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> property to the exact text that is used by T-SQL.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb559-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb559-109">See also</span></span>

- [<span data-ttu-id="bb559-110">Modèle objet LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="bb559-110">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [<span data-ttu-id="bb559-111">Procédure : Personnaliser des classes d’entité à l’aide de l’éditeur de code</span><span class="sxs-lookup"><span data-stu-id="bb559-111">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
