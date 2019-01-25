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
# <a name="how-to-represent-tables-as-classes"></a><span data-ttu-id="f3ff0-102">Procédure : Représentent les Tables en tant que Classes</span><span class="sxs-lookup"><span data-stu-id="f3ff0-102">How to: Represent Tables as Classes</span></span>
<span data-ttu-id="f3ff0-103">Utilisez le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.TableAttribute> attribut pour désigner une classe comme classe d’entité associée à une table de base de données.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-103">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.TableAttribute> attribute to designate a class as an entity class associated with a database table.</span></span>  
  
### <a name="to-map-a-class-to-a-database-table"></a><span data-ttu-id="f3ff0-104">Pour mapper une classe à une table de base de données</span><span class="sxs-lookup"><span data-stu-id="f3ff0-104">To map a class to a database table</span></span>  
  
-   <span data-ttu-id="f3ff0-105">Ajoutez l'attribut <xref:System.Data.Linq.Mapping.TableAttribute> à la déclaration de classe.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-105">Add the <xref:System.Data.Linq.Mapping.TableAttribute> attribute to the class declaration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f3ff0-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="f3ff0-106">Example</span></span>  
 <span data-ttu-id="f3ff0-107">Le code suivant établit la classe `Customer` comme une classe d'entité associée à la table de base de données `Customers`.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-107">The following code establishes the `Customer` class as an entity class that is associated with the `Customers` database table.</span></span>  
  
 [!code-csharp[DLinqCustomize#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCustomize/cs/Program.cs#1)]
 [!code-vb[DLinqCustomize#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCustomize/vb/Module1.vb#1)]  
  
 <span data-ttu-id="f3ff0-108">Il n'est pas nécessaire de spécifier la propriété <xref:System.Data.Linq.Mapping.TableAttribute.Name%2A> si le nom peut être déduit.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-108">You do not have to specify the <xref:System.Data.Linq.Mapping.TableAttribute.Name%2A> property if the name can be inferred.</span></span> <span data-ttu-id="f3ff0-109">Si vous ne spécifiez pas de nom, on considère qu'il s'agit du même nom que pour la propriété ou le champ.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-109">If you do not specify a name, the name is presumed to be the same name as that of the property or field.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3ff0-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3ff0-110">See also</span></span>
- [<span data-ttu-id="f3ff0-111">Modèle objet LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="f3ff0-111">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [<span data-ttu-id="f3ff0-112">Guide pratique pour Personnaliser des Classes d’entité à l’aide de l’éditeur de Code</span><span class="sxs-lookup"><span data-stu-id="f3ff0-112">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
