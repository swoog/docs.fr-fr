---
title: 'Comment : supprimer des lignes de la base de données'
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-ado
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 2144c99b-8055-4080-a5c6-1ea14335e2a3
caps.latest.revision: 3
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload:
- dotnet
ms.openlocfilehash: f84531be8bc8ae57db895959513fdc7dd4a8d154
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-delete-rows-from-the-database"></a><span data-ttu-id="12fa8-102">Comment : supprimer des lignes de la base de données</span><span class="sxs-lookup"><span data-stu-id="12fa8-102">How to: Delete Rows From the Database</span></span>
<span data-ttu-id="12fa8-103">Vous pouvez supprimer des lignes dans une base de données en supprimant correspondant [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] objets à partir de leur collection liée à des tables.</span><span class="sxs-lookup"><span data-stu-id="12fa8-103">You can delete rows in a database by removing the corresponding [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] objects from their table-related collection.</span></span> [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]<span data-ttu-id="12fa8-104"> traduit vos modifications à la requête SQL appropriée `DELETE` commandes.</span><span class="sxs-lookup"><span data-stu-id="12fa8-104"> translates your changes to the appropriate SQL `DELETE` commands.</span></span>  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]<span data-ttu-id="12fa8-105"> ne prend pas en charge ni ne reconnaît les opérations de suppression en cascade.</span><span class="sxs-lookup"><span data-stu-id="12fa8-105"> does not support or recognize cascade-delete operations.</span></span> <span data-ttu-id="12fa8-106">Si vous souhaitez supprimer une ligne dans une table comportant des contraintes sur cette suppression, vous devez terminer l'une des tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="12fa8-106">If you want to delete a row in a table that has constraints against it, you must complete either of the following tasks:</span></span>  
  
-   <span data-ttu-id="12fa8-107">Définissez la règle `ON DELETE CASCADE` dans la contrainte de clé étrangère dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="12fa8-107">Set the `ON DELETE CASCADE` rule in the foreign-key constraint in the database.</span></span>  
  
-   <span data-ttu-id="12fa8-108">Utilisez votre propre code pour supprimer en premier les objets enfants qui empêchent la suppression de l'objet parent.</span><span class="sxs-lookup"><span data-stu-id="12fa8-108">Use your own code to first delete the child objects that prevent the parent object from being deleted.</span></span>  
  
 <span data-ttu-id="12fa8-109">Sinon, une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="12fa8-109">Otherwise, an exception is thrown.</span></span> <span data-ttu-id="12fa8-110">Consultez le second exemple de code décrit plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="12fa8-110">See the second code example later in this topic.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="12fa8-111">Vous pouvez substituer des méthodes par défaut [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] pour les opérations `Insert`, `Update` et `Delete` sur les bases de données.</span><span class="sxs-lookup"><span data-stu-id="12fa8-111">You can override [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] default methods for `Insert`, `Update`, and `Delete` database operations.</span></span> <span data-ttu-id="12fa8-112">Pour plus d’informations, consultez [personnalisation des opérations d’insertion, mise à jour et supprimer](../../../../../../docs/framework/data/adonet/sql/linq/customizing-insert-update-and-delete-operations.md).</span><span class="sxs-lookup"><span data-stu-id="12fa8-112">For more information, see [Customizing Insert, Update, and Delete Operations](../../../../../../docs/framework/data/adonet/sql/linq/customizing-insert-update-and-delete-operations.md).</span></span>  
>   
>  <span data-ttu-id="12fa8-113">Les développeurs à l’aide de Visual Studio peuvent utiliser le [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] pour développer des procédures stockées dans le même but.</span><span class="sxs-lookup"><span data-stu-id="12fa8-113">Developers using Visual Studio can use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to develop stored procedures for the same purpose.</span></span>  
  
 <span data-ttu-id="12fa8-114">Les étapes suivantes supposent qu'un <xref:System.Data.Linq.DataContext> valide vous connecte à la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="12fa8-114">The following steps assume that a valid <xref:System.Data.Linq.DataContext> connects you to the Northwind database.</span></span> <span data-ttu-id="12fa8-115">Pour plus d’informations, consultez [Comment : se connecter à une base de données](../../../../../../docs/framework/data/adonet/sql/linq/how-to-connect-to-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="12fa8-115">For more information, see [How to: Connect to a Database](../../../../../../docs/framework/data/adonet/sql/linq/how-to-connect-to-a-database.md).</span></span>  
  
### <a name="to-delete-a-row-in-the-database"></a><span data-ttu-id="12fa8-116">Pour supprimer une ligne de la base de données</span><span class="sxs-lookup"><span data-stu-id="12fa8-116">To delete a row in the database</span></span>  
  
1.  <span data-ttu-id="12fa8-117">Interrogez la base de données concernant la ligne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="12fa8-117">Query the database for the row to be deleted.</span></span>  
  
2.  <span data-ttu-id="12fa8-118">Appelez la méthode <xref:System.Data.Linq.Table%601.DeleteOnSubmit%2A>.</span><span class="sxs-lookup"><span data-stu-id="12fa8-118">Call the <xref:System.Data.Linq.Table%601.DeleteOnSubmit%2A> method.</span></span>  
  
3.  <span data-ttu-id="12fa8-119">Soumettez la modification à la base de données.</span><span class="sxs-lookup"><span data-stu-id="12fa8-119">Submit the change to the database.</span></span>  
  
## <a name="example"></a><span data-ttu-id="12fa8-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="12fa8-120">Example</span></span>  
 <span data-ttu-id="12fa8-121">Le premier exemple de code interroge la base de données à propos de détails de commande concernant la commande 11000, marque ces détails de commande pour suppression, et soumet ces modifications à la base de données.</span><span class="sxs-lookup"><span data-stu-id="12fa8-121">This first code example queries the database for order details that belong to Order #11000, marks these order details for deletion, and submits these changes to the database.</span></span>  
  
 [!code-csharp[System.Data.Linq.Table#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.table/cs/program.cs#3)]
 [!code-vb[System.Data.Linq.Table#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.table/vb/module1.vb#3)]  
  
## <a name="example"></a><span data-ttu-id="12fa8-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="12fa8-122">Example</span></span>  
 <span data-ttu-id="12fa8-123">Dans ce second exemple, l'objectif est de supprimer une commande (10250).</span><span class="sxs-lookup"><span data-stu-id="12fa8-123">In this second example, the objective is to remove an order (#10250).</span></span> <span data-ttu-id="12fa8-124">Le code commence par examiner la table `OrderDetails` pour voir si la commande à supprimer y a des enfants.</span><span class="sxs-lookup"><span data-stu-id="12fa8-124">The code first examines the `OrderDetails` table to see whether the order to be removed has children there.</span></span> <span data-ttu-id="12fa8-125">Si la commande a des enfants, ces enfants sont marqués en vue de leur suppression, puis c'est au tour de la commande.</span><span class="sxs-lookup"><span data-stu-id="12fa8-125">If the order has children, first the children and then the order are marked for removal.</span></span> <span data-ttu-id="12fa8-126">Le <xref:System.Data.Linq.DataContext> place les véritables suppressions dans l'ordre approprié afin que les commandes de suppression envoyées à la base de données se conforment aux contraintes de la base de données.</span><span class="sxs-lookup"><span data-stu-id="12fa8-126">The <xref:System.Data.Linq.DataContext> puts the actual deletes in correct order so that delete commands sent to the database abide by the database constraints.</span></span>  
  
 [!code-csharp[DLinqCascadeWorkaround#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCascadeWorkaround/cs/Program.cs#1)]
 [!code-vb[DLinqCascadeWorkaround#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCascadeWorkaround/vb/Module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="12fa8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12fa8-127">See Also</span></span>  
 [<span data-ttu-id="12fa8-128">Guide pratique pour gérer les conflits de changement</span><span class="sxs-lookup"><span data-stu-id="12fa8-128">How to: Manage Change Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)  
 [<span data-ttu-id="12fa8-129">Comment : assigner des procédures stockées pour effectuer des mises à jour, insertions et suppressions (Concepteur O/R)</span><span class="sxs-lookup"><span data-stu-id="12fa8-129">How to: Assign stored procedures to perform updates, inserts, and deletes (O/R Designer)</span></span>](/visualstudio/data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer)  
 [<span data-ttu-id="12fa8-130">Apport et soumission de modifications de données</span><span class="sxs-lookup"><span data-stu-id="12fa8-130">Making and Submitting Data Changes</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
