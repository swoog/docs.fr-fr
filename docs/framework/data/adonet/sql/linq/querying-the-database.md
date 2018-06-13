---
title: Interrogation de la base de données
ms.date: 03/30/2017
ms.assetid: eefb8b0c-ff07-4e86-a3d3-567479523fe9
ms.openlocfilehash: fdcfaa3fc0d08df07027d44399612fb688b920d6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33358662"
---
# <a name="querying-the-database"></a><span data-ttu-id="84097-102">Interrogation de la base de données</span><span class="sxs-lookup"><span data-stu-id="84097-102">Querying the Database</span></span>
<span data-ttu-id="84097-103">Ce groupe de rubriques décrit comment développer et exécuter des requêtes dans les projets [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="84097-103">This group of topics describes how to develop and execute queries in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] projects.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="84097-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="84097-104">In This Section</span></span>  
 [<span data-ttu-id="84097-105">Guide pratique pour demander des informations</span><span class="sxs-lookup"><span data-stu-id="84097-105">How to: Query for Information</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-query-for-information.md)  
 <span data-ttu-id="84097-106">Montre brièvement comment les requêtes [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] s'apparentent généralement aux requêtes [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="84097-106">Briefly shows how [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] queries are basically the same as [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)] queries generally.</span></span>  
  
 [<span data-ttu-id="84097-107">Guide pratique pour récupérer des informations en lecture seule</span><span class="sxs-lookup"><span data-stu-id="84097-107">How to: Retrieve Information As Read-Only</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-retrieve-information-as-read-only.md)  
 <span data-ttu-id="84097-108">Explique comment augmenter les performances des requêtes lorsqu'aucune modification des données n'est planifiée.</span><span class="sxs-lookup"><span data-stu-id="84097-108">Describes how to increase query performance when no change to the data is planned.</span></span>  
  
 [<span data-ttu-id="84097-109">Guide pratique pour contrôler la quantité de données liées récupérées</span><span class="sxs-lookup"><span data-stu-id="84097-109">How to: Control How Much Related Data Is Retrieved</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-control-how-much-related-data-is-retrieved.md)  
 <span data-ttu-id="84097-110">Explique comment contrôler le type de données connexes récupérées avec la cible principale.</span><span class="sxs-lookup"><span data-stu-id="84097-110">Describes how to control which related data is retrieved together with the main target.</span></span>  
  
 [<span data-ttu-id="84097-111">Guide pratique pour filtrer des données liées</span><span class="sxs-lookup"><span data-stu-id="84097-111">How to: Filter Related Data</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-filter-related-data.md)  
 <span data-ttu-id="84097-112">Explique comment récupérer les données connexes à l'aide d'une sous-requête.</span><span class="sxs-lookup"><span data-stu-id="84097-112">Describes how to retrieve related data by using a sub-query.</span></span>  
  
 [<span data-ttu-id="84097-113">Guide pratique pour désactiver le chargement différé</span><span class="sxs-lookup"><span data-stu-id="84097-113">How to: Turn Off Deferred Loading</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-turn-off-deferred-loading.md)  
 <span data-ttu-id="84097-114">Explique comment désactiver le chargement différé.</span><span class="sxs-lookup"><span data-stu-id="84097-114">Describes how to turn off deferred loading.</span></span>  
  
 [<span data-ttu-id="84097-115">Guide pratique pour exécuter directement des requêtes SQL</span><span class="sxs-lookup"><span data-stu-id="84097-115">How to: Directly Execute SQL Queries</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-directly-execute-sql-queries.md)  
 <span data-ttu-id="84097-116">Explique comment soumettre des requêtes en utilisant le langage SQL.</span><span class="sxs-lookup"><span data-stu-id="84097-116">Describes how to submit queries by using SQL language.</span></span>  
  
 [<span data-ttu-id="84097-117">Guide pratique pour stocker et réutiliser des requêtes</span><span class="sxs-lookup"><span data-stu-id="84097-117">How to: Store and Reuse Queries</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-store-and-reuse-queries.md)  
 <span data-ttu-id="84097-118">Explique comment compiler une requête une fois et l'utiliser plusieurs fois avec des paramètres différents.</span><span class="sxs-lookup"><span data-stu-id="84097-118">Describes how to compile a query one time but use it multiple times with different parameters.</span></span>  
  
 [<span data-ttu-id="84097-119">Guide pratique pour gérer les clés composites dans les requêtes</span><span class="sxs-lookup"><span data-stu-id="84097-119">How to: Handle Composite Keys in Queries</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-handle-composite-keys-in-queries.md)  
 <span data-ttu-id="84097-120">Explique comment inclure plusieurs colonnes dans une requête où l’opérateur accepte uniquement un argument.</span><span class="sxs-lookup"><span data-stu-id="84097-120">Describes how to include more than one column in a query where the operator takes only a single argument.</span></span>  
  
 [<span data-ttu-id="84097-121">Guide pratique pour récupérer plusieurs objets à la fois</span><span class="sxs-lookup"><span data-stu-id="84097-121">How to: Retrieve Many Objects At Once</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-retrieve-many-objects-at-once.md)  
 <span data-ttu-id="84097-122">Explique comment utiliser <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A>.</span><span class="sxs-lookup"><span data-stu-id="84097-122">Describes how to use <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A>.</span></span>  
  
 [<span data-ttu-id="84097-123">Guide pratique pour filtrer au niveau du DataContext</span><span class="sxs-lookup"><span data-stu-id="84097-123">How to: Filter at the DataContext Level</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-filter-at-the-datacontext-level.md)  
 <span data-ttu-id="84097-124">Décrit une autre utilisation de <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A>.</span><span class="sxs-lookup"><span data-stu-id="84097-124">Describes another use of <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A>.</span></span>  
  
 [<span data-ttu-id="84097-125">Exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="84097-125">Query Examples</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)  
 <span data-ttu-id="84097-126">Fournit de nombreux exemples de requêtes.</span><span class="sxs-lookup"><span data-stu-id="84097-126">Provides many examples of queries.</span></span>
