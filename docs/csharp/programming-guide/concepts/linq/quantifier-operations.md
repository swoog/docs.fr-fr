---
title: Opérations de quantificateur (C#)
ms.date: 07/20/2015
ms.assetid: 84ac2ac2-7a63-4581-bc4c-14e34be1493b
ms.openlocfilehash: 090bc53c3dcedc82972ab7d16fa2968011a7db65
ms.sourcegitcommit: 3630c2515809e6f4b7dbb697a3354efec105a5cd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2019
ms.locfileid: "58412251"
---
# <a name="quantifier-operations-c"></a><span data-ttu-id="e65a6-102">Opérations de quantificateur (C#)</span><span class="sxs-lookup"><span data-stu-id="e65a6-102">Quantifier Operations (C#)</span></span>
<span data-ttu-id="e65a6-103">Les opérations de quantificateur retournent une valeur <xref:System.Boolean> qui indique si certains ou tous les éléments d’une séquence remplissent une condition.</span><span class="sxs-lookup"><span data-stu-id="e65a6-103">Quantifier operations return a <xref:System.Boolean> value that indicates whether some or all of the elements in a sequence satisfy a condition.</span></span>  
  
 <span data-ttu-id="e65a6-104">L’illustration suivante représente deux opérations de quantificateur différentes sur deux séquences sources différentes.</span><span class="sxs-lookup"><span data-stu-id="e65a6-104">The following illustration depicts two different quantifier operations on two different source sequences.</span></span> <span data-ttu-id="e65a6-105">La première opération demande si un ou plusieurs des éléments sont le caractère 'A' et le résultat est `true`.</span><span class="sxs-lookup"><span data-stu-id="e65a6-105">The first operation asks if one or more of the elements are the character 'A', and the result is `true`.</span></span> <span data-ttu-id="e65a6-106">La deuxième opération demande si tous les éléments sont le caractère 'A' et le résultat est `true`.</span><span class="sxs-lookup"><span data-stu-id="e65a6-106">The second operation asks if all the elements are the character 'A', and the result is `true`.</span></span>  
  
 ![Opérations de quantificateur LINQ](./media/quantifier-operations/linq-quantifier-operations.png)  
  
 <span data-ttu-id="e65a6-108">Les méthodes d’opérateur de requête standard qui effectuent des opérations de quantificateur sont répertoriées dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="e65a6-108">The standard query operator methods that perform quantifier operations are listed in the following section.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e65a6-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e65a6-109">Methods</span></span>  
  
|<span data-ttu-id="e65a6-110">Nom de la méthode</span><span class="sxs-lookup"><span data-stu-id="e65a6-110">Method Name</span></span>|<span data-ttu-id="e65a6-111">Description</span><span class="sxs-lookup"><span data-stu-id="e65a6-111">Description</span></span>|<span data-ttu-id="e65a6-112">Syntaxe d'expression de requête C#</span><span class="sxs-lookup"><span data-stu-id="e65a6-112">C# Query Expression Syntax</span></span>|<span data-ttu-id="e65a6-113">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="e65a6-113">More Information</span></span>|  
|-----------------|-----------------|---------------------------------|----------------------|  
|<span data-ttu-id="e65a6-114">Tous</span><span class="sxs-lookup"><span data-stu-id="e65a6-114">All</span></span>|<span data-ttu-id="e65a6-115">Détermine si tous les éléments d’une séquence remplissent une condition.</span><span class="sxs-lookup"><span data-stu-id="e65a6-115">Determines whether all the elements in a sequence satisfy a condition.</span></span>|<span data-ttu-id="e65a6-116">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="e65a6-116">Not applicable.</span></span>|<xref:System.Linq.Enumerable.All%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.All%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="e65a6-117">Any</span><span class="sxs-lookup"><span data-stu-id="e65a6-117">Any</span></span>|<span data-ttu-id="e65a6-118">Détermine si certains éléments d’une séquence remplissent une condition.</span><span class="sxs-lookup"><span data-stu-id="e65a6-118">Determines whether any elements in a sequence satisfy a condition.</span></span>|<span data-ttu-id="e65a6-119">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="e65a6-119">Not applicable.</span></span>|<xref:System.Linq.Enumerable.Any%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Any%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="e65a6-120">Contient</span><span class="sxs-lookup"><span data-stu-id="e65a6-120">Contains</span></span>|<span data-ttu-id="e65a6-121">Détermine si une séquence contient un élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="e65a6-121">Determines whether a sequence contains a specified element.</span></span>|<span data-ttu-id="e65a6-122">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="e65a6-122">Not applicable.</span></span>|<xref:System.Linq.Enumerable.Contains%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Contains%2A?displayProperty=nameWithType>|  
  
## <a name="see-also"></a><span data-ttu-id="e65a6-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e65a6-123">See also</span></span>

- <xref:System.Linq>
- [<span data-ttu-id="e65a6-124">Vue d’ensemble des opérateurs de requête standard (C#)</span><span class="sxs-lookup"><span data-stu-id="e65a6-124">Standard Query Operators Overview (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [<span data-ttu-id="e65a6-125">Guide pratique pour spécifier dynamiquement des filtres de prédicat au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="e65a6-125">How to: Dynamically Specify Predicate Filters at Runtime</span></span>](../../../../csharp/programming-guide/linq-query-expressions/how-to-dynamically-specify-predicate-filters-at-runtime.md)
- [<span data-ttu-id="e65a6-126">Guide pratique pour rechercher des phrases qui contiennent un groupe de mots spécifié (LINQ) (C#)</span><span class="sxs-lookup"><span data-stu-id="e65a6-126">How to: Query for Sentences that Contain a Specified Set of Words (LINQ) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-query-for-sentences-that-contain-a-specified-set-of-words-linq.md)
