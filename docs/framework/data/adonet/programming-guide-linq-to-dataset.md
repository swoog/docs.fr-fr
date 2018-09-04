---
title: Guide de programmation (LINQ to DataSet)
ms.date: 03/30/2017
ms.assetid: 977aedd7-0084-46a0-b56f-345787a55da1
ms.openlocfilehash: 0c6b026d86a898aa52d93833ac3e447d6f6cba11
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43513368"
---
# <a name="programming-guide-linq-to-dataset"></a><span data-ttu-id="aa559-102">Guide de programmation (LINQ to DataSet)</span><span class="sxs-lookup"><span data-stu-id="aa559-102">Programming Guide (LINQ to DataSet)</span></span>
<span data-ttu-id="aa559-103">Cette section fournit des informations conceptuelles et des exemples pour la programmation avec [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)].</span><span class="sxs-lookup"><span data-stu-id="aa559-103">This section provides conceptual information and examples for programming with [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)].</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="aa559-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="aa559-104">In This Section</span></span>  
 [<span data-ttu-id="aa559-105">Requêtes dans LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="aa559-105">Queries in LINQ to DataSet</span></span>](../../../../docs/framework/data/adonet/queries-in-linq-to-dataset.md)  
 <span data-ttu-id="aa559-106">Fournit des informations sur la manière d'écrire des requêtes [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)].</span><span class="sxs-lookup"><span data-stu-id="aa559-106">Provides information about how to write [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] queries.</span></span>  
  
 [<span data-ttu-id="aa559-107">Interrogation de DataSets</span><span class="sxs-lookup"><span data-stu-id="aa559-107">Querying DataSets</span></span>](../../../../docs/framework/data/adonet/querying-datasets-linq-to-dataset.md)  
 <span data-ttu-id="aa559-108">Explique comment interroger des objets <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="aa559-108">Describes how to query <xref:System.Data.DataSet> objects.</span></span>  
  
 [<span data-ttu-id="aa559-109">Comparaison de DataRows</span><span class="sxs-lookup"><span data-stu-id="aa559-109">Comparing DataRows</span></span>](../../../../docs/framework/data/adonet/comparing-datarows-linq-to-dataset.md)  
 <span data-ttu-id="aa559-110">Explique comment utiliser l'objet <xref:System.Data.DataRowComparer> pour comparer des lignes de données.</span><span class="sxs-lookup"><span data-stu-id="aa559-110">Describes how to use the <xref:System.Data.DataRowComparer> object to compare data rows.</span></span>  
  
 [<span data-ttu-id="aa559-111">Création d’un DataTable à partir d’une requête</span><span class="sxs-lookup"><span data-stu-id="aa559-111">Creating a DataTable From a Query</span></span>](../../../../docs/framework/data/adonet/creating-a-datatable-from-a-query-linq-to-dataset.md)  
 <span data-ttu-id="aa559-112">Fournit des informations sur la création d’un <xref:System.Data.DataTable> à partir d’un [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] requête à l’aide de la <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="aa559-112">Provides information about creating a <xref:System.Data.DataTable> from a [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] query by using the <xref:System.Data.DataTableExtensions.CopyToDataTable%2A> method.</span></span>  
  
 [<span data-ttu-id="aa559-113">Comment : implémenter CopyToDataTable\<T > où le Type générique T n’est pas un DataRow</span><span class="sxs-lookup"><span data-stu-id="aa559-113">How to: Implement CopyToDataTable\<T> Where the Generic Type T Is Not a DataRow</span></span>](../../../../docs/framework/data/adonet/implement-copytodatatable-where-type-not-a-datarow.md)  
 <span data-ttu-id="aa559-114">Explique comment implémenter une méthode `CopyToDataTable<T>` personnalisée dans laquelle le paramètre générique T n'est pas du type <xref:System.Data.DataRow>.</span><span class="sxs-lookup"><span data-stu-id="aa559-114">Describes how to implement a custom `CopyToDataTable<T>` method where the generic parameter T is not of type <xref:System.Data.DataRow>.</span></span>  
  
 [<span data-ttu-id="aa559-115">Méthodes génériques Field et SetField</span><span class="sxs-lookup"><span data-stu-id="aa559-115">Generic Field and SetField Methods</span></span>](../../../../docs/framework/data/adonet/generic-field-and-setfield-methods-linq-to-dataset.md)  
 <span data-ttu-id="aa559-116">Fournit des informations sur les méthodes génériques <xref:System.Data.DataRowExtensions.Field%2A> et <xref:System.Data.DataRowExtensions.SetField%2A>.</span><span class="sxs-lookup"><span data-stu-id="aa559-116">Provides information about the generic <xref:System.Data.DataRowExtensions.Field%2A> and <xref:System.Data.DataRowExtensions.SetField%2A> methods.</span></span>  
  
 [<span data-ttu-id="aa559-117">Liaison de données et LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="aa559-117">Data Binding and LINQ to DataSet</span></span>](../../../../docs/framework/data/adonet/data-binding-and-linq-to-dataset.md)  
 <span data-ttu-id="aa559-118">Décrit la liaison de données à l'aide de l'objet <xref:System.Data.DataView>.</span><span class="sxs-lookup"><span data-stu-id="aa559-118">Describes databinding using the <xref:System.Data.DataView> object.</span></span>  
  
 [<span data-ttu-id="aa559-119">Débogage des requêtes LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="aa559-119">Debugging LINQ to DataSet Queries</span></span>](../../../../docs/framework/data/adonet/debugging-linq-to-dataset-queries.md)  
 <span data-ttu-id="aa559-120">Fournit des informations sur le débogage et résolution des problèmes [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] requêtes.</span><span class="sxs-lookup"><span data-stu-id="aa559-120">Provides information about debugging and troubleshooting [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)] queries.</span></span>  
  
 [<span data-ttu-id="aa559-121">Sécurité</span><span class="sxs-lookup"><span data-stu-id="aa559-121">Security</span></span>](../../../../docs/framework/data/adonet/security-linq-to-dataset.md)  
 <span data-ttu-id="aa559-122">Décrit les problèmes de sécurité dans [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)].</span><span class="sxs-lookup"><span data-stu-id="aa559-122">Describes security issues in [!INCLUDE[linq_dataset](../../../../includes/linq-dataset-md.md)].</span></span>  
  
 [<span data-ttu-id="aa559-123">Exemples LINQ to DataSet</span><span class="sxs-lookup"><span data-stu-id="aa559-123">LINQ to DataSet Examples</span></span>](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md)  
 <span data-ttu-id="aa559-124">Fournit des exemples de requête qui utilisent des opérateurs [!INCLUDE[vbteclinq](../../../../includes/vbteclinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="aa559-124">Provides query examples that use the [!INCLUDE[vbteclinq](../../../../includes/vbteclinq-md.md)] operators.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="aa559-125">Référence</span><span class="sxs-lookup"><span data-stu-id="aa559-125">Reference</span></span>  
 <xref:System.Data.DataRowComparer>  
  
 <xref:System.Data.DataRowExtensions>  
  
 <xref:System.Data.DataTableExtensions>  
  
 <xref:System.Data.DataView>  
  
## <a name="see-also"></a><span data-ttu-id="aa559-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa559-126">See also</span></span>

- [<span data-ttu-id="aa559-127">LINQ et ADO.NET</span><span class="sxs-lookup"><span data-stu-id="aa559-127">LINQ and ADO.NET</span></span>](linq-and-ado-net.md)  
- [<span data-ttu-id="aa559-128">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="aa559-128">Language Integrated Query (LINQ)</span></span>](../../../csharp/programming-guide/concepts/linq/index.md)
