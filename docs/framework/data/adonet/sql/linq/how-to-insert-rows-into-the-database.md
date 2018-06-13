---
title: 'Comment : insérer des lignes dans la base de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 44d99680-69c7-4879-a732-f6771b334211
ms.openlocfilehash: 4f46e38642d42e3a2e4d5f05e23cc76cf431119b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33361732"
---
# <a name="how-to-insert-rows-into-the-database"></a><span data-ttu-id="102dc-102">Comment : insérer des lignes dans la base de données</span><span class="sxs-lookup"><span data-stu-id="102dc-102">How to: Insert Rows Into the Database</span></span>
<span data-ttu-id="102dc-103">Insérer des lignes dans une base de données en ajoutant des objets à le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Table%601> collection et en soumettant les modifications apportées à la base de données.</span><span class="sxs-lookup"><span data-stu-id="102dc-103">You insert rows into a database by adding objects to the associated [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Table%601> collection and then submitting the changes to the database.</span></span> [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]<span data-ttu-id="102dc-104"> traduit vos modifications dans la requête SQL appropriée `INSERT` commandes.</span><span class="sxs-lookup"><span data-stu-id="102dc-104"> translates your changes into the appropriate SQL `INSERT` commands.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="102dc-105">Vous pouvez substituer des méthodes par défaut [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] pour les opérations `Insert`, `Update` et `Delete` sur les bases de données.</span><span class="sxs-lookup"><span data-stu-id="102dc-105">You can override [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] default methods for `Insert`, `Update`, and `Delete` database operations.</span></span> <span data-ttu-id="102dc-106">Pour plus d’informations, consultez [personnalisation des opérations d’insertion, mise à jour et supprimer](../../../../../../docs/framework/data/adonet/sql/linq/customizing-insert-update-and-delete-operations.md).</span><span class="sxs-lookup"><span data-stu-id="102dc-106">For more information, see [Customizing Insert, Update, and Delete Operations](../../../../../../docs/framework/data/adonet/sql/linq/customizing-insert-update-and-delete-operations.md).</span></span>  
>   
>  <span data-ttu-id="102dc-107">Les développeurs à l’aide de Visual Studio peuvent utiliser le [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] pour développer des procédures stockées dans le même but.</span><span class="sxs-lookup"><span data-stu-id="102dc-107">Developers using Visual Studio can use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to develop stored procedures for the same purpose.</span></span>  
  
 <span data-ttu-id="102dc-108">Les étapes suivantes supposent qu'un <xref:System.Data.Linq.DataContext> valide vous connecte à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="102dc-108">The following steps assume that a valid <xref:System.Data.Linq.DataContext> connects you to the Northwind database.</span></span> <span data-ttu-id="102dc-109">Pour plus d’informations, consultez [Comment : se connecter à une base de données](../../../../../../docs/framework/data/adonet/sql/linq/how-to-connect-to-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="102dc-109">For more information, see [How to: Connect to a Database](../../../../../../docs/framework/data/adonet/sql/linq/how-to-connect-to-a-database.md).</span></span>  
  
### <a name="to-insert-a-row-into-the-database"></a><span data-ttu-id="102dc-110">Pour insérer une ligne dans la base de données</span><span class="sxs-lookup"><span data-stu-id="102dc-110">To insert a row into the database</span></span>  
  
1.  <span data-ttu-id="102dc-111">Créez un objet qui inclut les données de colonne à soumettre.</span><span class="sxs-lookup"><span data-stu-id="102dc-111">Create a new object that includes the column data to be submitted.</span></span>  
  
2.  <span data-ttu-id="102dc-112">Ajouter le nouvel objet à la [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] `Table` collection associée à la table cible dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="102dc-112">Add the new object to the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] `Table` collection associated with the target table in the database.</span></span>  
  
3.  <span data-ttu-id="102dc-113">Soumettez la modification à la base de données.</span><span class="sxs-lookup"><span data-stu-id="102dc-113">Submit the change to the database.</span></span>  
  
## <a name="example"></a><span data-ttu-id="102dc-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="102dc-114">Example</span></span>  
 <span data-ttu-id="102dc-115">L'exemple de code suivant crée un objet de type `Order` et le remplit avec les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="102dc-115">The following code example creates a new object of type `Order` and populates it with appropriate values.</span></span> <span data-ttu-id="102dc-116">Il ajoute ensuite le nouvel objet à la collection `Order`.</span><span class="sxs-lookup"><span data-stu-id="102dc-116">It then adds the new object to the `Order` collection.</span></span> <span data-ttu-id="102dc-117">Enfin, il soumet la modification à la base de données comme une nouvelle ligne de la table `Orders`.</span><span class="sxs-lookup"><span data-stu-id="102dc-117">Finally, it submits the change to the database as a new row in the `Orders` table.</span></span>  
  
 [!code-csharp[System.Data.Linq.Table#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.table/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.Table#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.table/vb/module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="102dc-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="102dc-118">See Also</span></span>  
 [<span data-ttu-id="102dc-119">Guide pratique pour gérer les conflits de changement</span><span class="sxs-lookup"><span data-stu-id="102dc-119">How to: Manage Change Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)  
 [<span data-ttu-id="102dc-120">Méthodes DataContext (Concepteur O/R)</span><span class="sxs-lookup"><span data-stu-id="102dc-120">DataContext Methods (O/R Designer)</span></span>](/visualstudio/data-tools/datacontext-methods-o-r-designer)  
 [<span data-ttu-id="102dc-121">Comment : assigner des procédures stockées pour effectuer des mises à jour, insertions et suppressions (Concepteur O/R)</span><span class="sxs-lookup"><span data-stu-id="102dc-121">How to: Assign stored procedures to perform updates, inserts, and deletes (O/R Designer)</span></span>](/visualstudio/data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer)  
 [<span data-ttu-id="102dc-122">Apport et soumission de modifications de données</span><span class="sxs-lookup"><span data-stu-id="102dc-122">Making and Submitting Data Changes</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
