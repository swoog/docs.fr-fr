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
# <a name="how-to-update-rows-in-the-database"></a><span data-ttu-id="c52a5-102">Comment : mettre à jour des lignes dans la base de données</span><span class="sxs-lookup"><span data-stu-id="c52a5-102">How to: Update Rows in the Database</span></span>
<span data-ttu-id="c52a5-103">Vous pouvez mettre à jour les lignes dans une base de données en modifiant les valeurs de membre des objets associés à la [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Table%601> collection et en soumettant les modifications apportées à la base de données.</span><span class="sxs-lookup"><span data-stu-id="c52a5-103">You can update rows in a database by modifying member values of the objects associated with the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Table%601> collection and then submitting the changes to the database.</span></span> [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]<span data-ttu-id="c52a5-104"> traduit vos modifications dans la requête SQL appropriée `UPDATE` commandes.</span><span class="sxs-lookup"><span data-stu-id="c52a5-104"> translates your changes into the appropriate SQL `UPDATE` commands.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c52a5-105">Vous pouvez substituer des méthodes par défaut [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] pour les opérations `Insert`, `Update` et `Delete` sur les bases de données.</span><span class="sxs-lookup"><span data-stu-id="c52a5-105">You can override [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] default methods for `Insert`, `Update`, and `Delete` database operations.</span></span> <span data-ttu-id="c52a5-106">Pour plus d’informations, consultez [personnalisation des opérations d’insertion, mise à jour et supprimer](../../../../../../docs/framework/data/adonet/sql/linq/customizing-insert-update-and-delete-operations.md).</span><span class="sxs-lookup"><span data-stu-id="c52a5-106">For more information, see [Customizing Insert, Update, and Delete Operations](../../../../../../docs/framework/data/adonet/sql/linq/customizing-insert-update-and-delete-operations.md).</span></span>  
>   
>  <span data-ttu-id="c52a5-107">Les développeurs à l’aide de Visual Studio peuvent utiliser le [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] pour développer des procédures stockées dans le même but.</span><span class="sxs-lookup"><span data-stu-id="c52a5-107">Developers using Visual Studio can use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to develop stored procedures for the same purpose.</span></span>  
  
 <span data-ttu-id="c52a5-108">Les étapes suivantes supposent qu'un <xref:System.Data.Linq.DataContext> valide vous connecte à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="c52a5-108">The following steps assume that a valid <xref:System.Data.Linq.DataContext> connects you to the Northwind database.</span></span> <span data-ttu-id="c52a5-109">Pour plus d’informations, consultez [Comment : se connecter à une base de données](../../../../../../docs/framework/data/adonet/sql/linq/how-to-connect-to-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="c52a5-109">For more information, see [How to: Connect to a Database](../../../../../../docs/framework/data/adonet/sql/linq/how-to-connect-to-a-database.md).</span></span>  
  
### <a name="to-update-a-row-in-the-database"></a><span data-ttu-id="c52a5-110">Pour mettre à jour une ligne dans la base de données</span><span class="sxs-lookup"><span data-stu-id="c52a5-110">To update a row in the database</span></span>  
  
1.  <span data-ttu-id="c52a5-111">Interrogez la base de données concernant la ligne à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="c52a5-111">Query the database for the row to be updated.</span></span>  
  
2.  <span data-ttu-id="c52a5-112">Apportez les modifications souhaitées aux valeurs de membre dans l'objet [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] obtenu.</span><span class="sxs-lookup"><span data-stu-id="c52a5-112">Make desired changes to member values in the resulting [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] object.</span></span>  
  
3.  <span data-ttu-id="c52a5-113">Soumettez les modifications à la base de données.</span><span class="sxs-lookup"><span data-stu-id="c52a5-113">Submit the changes to the database.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c52a5-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="c52a5-114">Example</span></span>  
 <span data-ttu-id="c52a5-115">L'exemple suivant interroge la base de données concernant la commande 11000, puis modifie les valeurs de `ShipName` et `ShipVia` dans l'objet `Order` obtenu.</span><span class="sxs-lookup"><span data-stu-id="c52a5-115">The following example queries the database for order #11000, and then changes the values of `ShipName` and `ShipVia` in the resulting `Order` object.</span></span> <span data-ttu-id="c52a5-116">Enfin, les modifications apportées à ces valeurs de membre sont soumises à la base de données comme modifications dans les colonnes `ShipName` et `ShipVia`.</span><span class="sxs-lookup"><span data-stu-id="c52a5-116">Finally, the changes to these member values are submitted to the database as changes in the `ShipName` and `ShipVia` columns.</span></span>  
  
 [!code-csharp[System.Data.Linq.Table#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.table/cs/program.cs#2)]
 [!code-vb[System.Data.Linq.Table#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.table/vb/module1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="c52a5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c52a5-117">See Also</span></span>  
 [<span data-ttu-id="c52a5-118">Guide pratique pour gérer les conflits de changement</span><span class="sxs-lookup"><span data-stu-id="c52a5-118">How to: Manage Change Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)  
 [<span data-ttu-id="c52a5-119">Comment : assigner des procédures stockées pour effectuer des mises à jour, insertions et suppressions (Concepteur O/R)</span><span class="sxs-lookup"><span data-stu-id="c52a5-119">How to: Assign stored procedures to perform updates, inserts, and deletes (O/R Designer)</span></span>](/visualstudio/data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer)  
 [<span data-ttu-id="c52a5-120">Apport et soumission de modifications de données</span><span class="sxs-lookup"><span data-stu-id="c52a5-120">Making and Submitting Data Changes</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
