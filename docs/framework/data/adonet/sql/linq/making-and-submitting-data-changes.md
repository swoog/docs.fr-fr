---
title: Apport et soumission de modifications de données
ms.date: 03/30/2017
ms.assetid: d68c2dc3-99b3-49ab-b547-2ca5b386429a
ms.openlocfilehash: c9d319727a750fbd3e2a186c28e79b20200c6bd0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33360791"
---
# <a name="making-and-submitting-data-changes"></a><span data-ttu-id="a568c-102">Apport et soumission de modifications de données</span><span class="sxs-lookup"><span data-stu-id="a568c-102">Making and Submitting Data Changes</span></span>
<span data-ttu-id="a568c-103">Les rubriques de cette section décrivent comment effectuer et transmettre des modifications à la base de données et comment gérer des conflits d'accès concurrentiel optimiste.</span><span class="sxs-lookup"><span data-stu-id="a568c-103">The topics in this section describe how to make and transmit changes to the database and how to handle optimistic concurrency conflicts.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a568c-104">Vous pouvez substituer des méthodes par défaut [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] pour les opérations `Insert`, `Update` et `Delete` sur les bases de données.</span><span class="sxs-lookup"><span data-stu-id="a568c-104">You can override [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] default methods for `Insert`, `Update`, and `Delete` database operations.</span></span> <span data-ttu-id="a568c-105">Pour plus d’informations, consultez [personnalisation des opérations d’insertion, mise à jour et supprimer](../../../../../../docs/framework/data/adonet/sql/linq/customizing-insert-update-and-delete-operations.md).</span><span class="sxs-lookup"><span data-stu-id="a568c-105">For more information, see [Customizing Insert, Update, and Delete Operations](../../../../../../docs/framework/data/adonet/sql/linq/customizing-insert-update-and-delete-operations.md).</span></span>  
>   
>  <span data-ttu-id="a568c-106">Les développeurs à l’aide de Visual Studio peuvent utiliser le [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] pour développer des procédures stockées dans le même but.</span><span class="sxs-lookup"><span data-stu-id="a568c-106">Developers using Visual Studio can use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to develop stored procedures for the same purpose.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="a568c-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a568c-107">In This Section</span></span>  
 [<span data-ttu-id="a568c-108">Guide pratique pour insérer des lignes dans la base de données</span><span class="sxs-lookup"><span data-stu-id="a568c-108">How to: Insert Rows Into the Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-insert-rows-into-the-database.md)  
 <span data-ttu-id="a568c-109">Explique comment insérer des lignes dans la base de données en ajoutant des objets au modèle objet.</span><span class="sxs-lookup"><span data-stu-id="a568c-109">Describes how to insert rows in the database by adding objects to the object model.</span></span>  
  
 [<span data-ttu-id="a568c-110">Guide pratique pour mettre à jour des lignes dans la base de données</span><span class="sxs-lookup"><span data-stu-id="a568c-110">How to: Update Rows in the Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-update-rows-in-the-database.md)  
 <span data-ttu-id="a568c-111">Explique comment mettre à jour des lignes dans la base de données en mettant à jour des objets du modèle objet.</span><span class="sxs-lookup"><span data-stu-id="a568c-111">Describes how to update rows in the database by updating objects in the object model.</span></span>  
  
 [<span data-ttu-id="a568c-112">Guide pratique pour supprimer des lignes de la base de données</span><span class="sxs-lookup"><span data-stu-id="a568c-112">How to: Delete Rows From the Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-delete-rows-from-the-database.md)  
 <span data-ttu-id="a568c-113">Explique comment supprimer des lignes de la base de données en supprimant des objets du modèle objet.</span><span class="sxs-lookup"><span data-stu-id="a568c-113">Describes how to delete rows in the database by deleting objects in the object model.</span></span>  
  
 [<span data-ttu-id="a568c-114">Guide pratique pour soumettre des modifications à la base de données</span><span class="sxs-lookup"><span data-stu-id="a568c-114">How to: Submit Changes to the Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-submit-changes-to-the-database.md)  
 <span data-ttu-id="a568c-115">Explique comment envoyer des modifications de modèle objet à la base de données.</span><span class="sxs-lookup"><span data-stu-id="a568c-115">Describes how to send object-model changes to the database.</span></span>  
  
 [<span data-ttu-id="a568c-116">Guide pratique pour mettre entre parenthèses des soumissions de données à l’aide de transactions</span><span class="sxs-lookup"><span data-stu-id="a568c-116">How to: Bracket Data Submissions by Using Transactions</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-bracket-data-submissions-by-using-transactions.md)  
 <span data-ttu-id="a568c-117">Explique comment inclure des opérations dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="a568c-117">Describes how to include operations in a transaction.</span></span>  
  
 [<span data-ttu-id="a568c-118">Guide pratique pour créer dynamiquement une base de données</span><span class="sxs-lookup"><span data-stu-id="a568c-118">How to: Dynamically Create a Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-dynamically-create-a-database.md)  
 <span data-ttu-id="a568c-119">Explique comment générer dynamiquement des bases de données et des scénarios classiques pour cette approche.</span><span class="sxs-lookup"><span data-stu-id="a568c-119">Describes how to generate databases dynamically, and typical scenarios for this approach.</span></span>  
  
 [<span data-ttu-id="a568c-120">Guide pratique pour gérer les conflits de changement</span><span class="sxs-lookup"><span data-stu-id="a568c-120">How to: Manage Change Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)  
 <span data-ttu-id="a568c-121">Propose des techniques pour traiter les problèmes d'accès concurrentiel optimiste.</span><span class="sxs-lookup"><span data-stu-id="a568c-121">Describes techniques for addressing optimistic concurrency issues.</span></span>
