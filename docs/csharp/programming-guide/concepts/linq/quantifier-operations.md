---
title: Opérations de quantificateur (C#)
ms.date: 07/20/2015
ms.assetid: 84ac2ac2-7a63-4581-bc4c-14e34be1493b
ms.openlocfilehash: 24c8f9a6b589592c26c8a514bc44ff9623a82d2f
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43523103"
---
# <a name="quantifier-operations-c"></a><span data-ttu-id="0781b-102">Opérations de quantificateur (C#)</span><span class="sxs-lookup"><span data-stu-id="0781b-102">Quantifier Operations (C#)</span></span>
<span data-ttu-id="0781b-103">Les opérations de quantificateur retournent une valeur <xref:System.Boolean> qui indique si certains ou tous les éléments d’une séquence remplissent une condition.</span><span class="sxs-lookup"><span data-stu-id="0781b-103">Quantifier operations return a <xref:System.Boolean> value that indicates whether some or all of the elements in a sequence satisfy a condition.</span></span>  
  
 <span data-ttu-id="0781b-104">L’illustration suivante représente deux opérations de quantificateur différentes sur deux séquences sources différentes.</span><span class="sxs-lookup"><span data-stu-id="0781b-104">The following illustration depicts two different quantifier operations on two different source sequences.</span></span> <span data-ttu-id="0781b-105">La première opération demande si un ou plusieurs des éléments sont le caractère 'A' et le résultat est `true`.</span><span class="sxs-lookup"><span data-stu-id="0781b-105">The first operation asks if one or more of the elements are the character 'A', and the result is `true`.</span></span> <span data-ttu-id="0781b-106">La deuxième opération demande si tous les éléments sont le caractère 'A' et le résultat est `true`.</span><span class="sxs-lookup"><span data-stu-id="0781b-106">The second operation asks if all the elements are the character 'A', and the result is `true`.</span></span>  
  
 <span data-ttu-id="0781b-107">![Opérations de quantificateur LINQ](../../../../csharp/programming-guide/concepts/linq/media/linq_quantifier.png "Quantificateur_LINQ")</span><span class="sxs-lookup"><span data-stu-id="0781b-107">![LINQ Quantifier Operations](../../../../csharp/programming-guide/concepts/linq/media/linq_quantifier.png "LINQ_Quantifier")</span></span>  
  
 <span data-ttu-id="0781b-108">Les méthodes d’opérateur de requête standard qui effectuent des opérations de quantificateur sont répertoriées dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="0781b-108">The standard query operator methods that perform quantifier operations are listed in the following section.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0781b-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0781b-109">Methods</span></span>  
  
|<span data-ttu-id="0781b-110">Nom de la méthode</span><span class="sxs-lookup"><span data-stu-id="0781b-110">Method Name</span></span>|<span data-ttu-id="0781b-111">Description</span><span class="sxs-lookup"><span data-stu-id="0781b-111">Description</span></span>|<span data-ttu-id="0781b-112">Syntaxe d'expression de requête C#</span><span class="sxs-lookup"><span data-stu-id="0781b-112">C# Query Expression Syntax</span></span>|<span data-ttu-id="0781b-113">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="0781b-113">More Information</span></span>|  
|-----------------|-----------------|---------------------------------|----------------------|  
|<span data-ttu-id="0781b-114">Tous</span><span class="sxs-lookup"><span data-stu-id="0781b-114">All</span></span>|<span data-ttu-id="0781b-115">Détermine si tous les éléments d’une séquence remplissent une condition.</span><span class="sxs-lookup"><span data-stu-id="0781b-115">Determines whether all the elements in a sequence satisfy a condition.</span></span>|<span data-ttu-id="0781b-116">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="0781b-116">Not applicable.</span></span>|<xref:System.Linq.Enumerable.All%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.All%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="0781b-117">Any</span><span class="sxs-lookup"><span data-stu-id="0781b-117">Any</span></span>|<span data-ttu-id="0781b-118">Détermine si certains éléments d’une séquence remplissent une condition.</span><span class="sxs-lookup"><span data-stu-id="0781b-118">Determines whether any elements in a sequence satisfy a condition.</span></span>|<span data-ttu-id="0781b-119">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="0781b-119">Not applicable.</span></span>|<xref:System.Linq.Enumerable.Any%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Any%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="0781b-120">Contient</span><span class="sxs-lookup"><span data-stu-id="0781b-120">Contains</span></span>|<span data-ttu-id="0781b-121">Détermine si une séquence contient un élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="0781b-121">Determines whether a sequence contains a specified element.</span></span>|<span data-ttu-id="0781b-122">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="0781b-122">Not applicable.</span></span>|<xref:System.Linq.Enumerable.Contains%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Contains%2A?displayProperty=nameWithType>|  
  
## <a name="see-also"></a><span data-ttu-id="0781b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0781b-123">See Also</span></span>

- <xref:System.Linq>  
- [<span data-ttu-id="0781b-124">Présentation des opérateurs de requête standard (C#)</span><span class="sxs-lookup"><span data-stu-id="0781b-124">Standard Query Operators Overview (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)  
- [<span data-ttu-id="0781b-125">Guide pratique pour spécifier dynamiquement des filtres de prédicat au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="0781b-125">How to: Dynamically Specify Predicate Filters at Runtime</span></span>](../../../../csharp/programming-guide/linq-query-expressions/how-to-dynamically-specify-predicate-filters-at-runtime.md)  
- [<span data-ttu-id="0781b-126">Guide pratique pour rechercher des phrases qui contiennent un groupe de mots spécifié (LINQ) (C#)</span><span class="sxs-lookup"><span data-stu-id="0781b-126">How to: Query for Sentences that Contain a Specified Set of Words (LINQ) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-query-for-sentences-that-contain-a-specified-set-of-words-linq.md)
