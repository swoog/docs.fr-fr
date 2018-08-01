---
title: Effectuer des jointures externes gauches (LINQ en C#)
description: Découvrez comment effectuer des jointures externes gauches à l’aide de LINQ en C#.
ms.date: 12/1/2016
ms.assetid: f542cee6-3169-4dcf-a631-3a6a79ccd473
ms.openlocfilehash: 3da144e6e3293d3a4084f7a99f77aec199f7a267
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2018
ms.locfileid: "37403850"
---
# <a name="perform-left-outer-joins"></a><span data-ttu-id="7ecc2-103">Effectuer des jointures externes gauches</span><span class="sxs-lookup"><span data-stu-id="7ecc2-103">Perform left outer joins</span></span>

<span data-ttu-id="7ecc2-104">Une jointure externe gauche est une jointure dans laquelle chaque élément de la première collection est retourné, qu’elle ait ou non des éléments corrélés dans la deuxième collection.</span><span class="sxs-lookup"><span data-stu-id="7ecc2-104">A left outer join is a join in which each element of the first collection is returned, regardless of whether it has any correlated elements in the second collection.</span></span> <span data-ttu-id="7ecc2-105">Vous pouvez utiliser LINQ pour effectuer une jointure externe gauche en appelant la méthode <xref:System.Linq.Enumerable.DefaultIfEmpty%2A> sur les résultats d’une jointure groupée.</span><span class="sxs-lookup"><span data-stu-id="7ecc2-105">You can use LINQ to perform a left outer join by calling the <xref:System.Linq.Enumerable.DefaultIfEmpty%2A> method on the results of a group join.</span></span>

## <a name="example"></a><span data-ttu-id="7ecc2-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="7ecc2-106">Example</span></span>

<span data-ttu-id="7ecc2-107">L’exemple suivant montre comment utiliser la méthode <xref:System.Linq.Enumerable.DefaultIfEmpty%2A> sur les résultats d’une jointure groupée pour effectuer une jointure externe gauche.</span><span class="sxs-lookup"><span data-stu-id="7ecc2-107">The following example demonstrates how to use the <xref:System.Linq.Enumerable.DefaultIfEmpty%2A> method on the results of a group join to perform a left outer join.</span></span>

<span data-ttu-id="7ecc2-108">Pour créer une jointure externe gauche entre deux collections, la première étape consiste à effectuer une jointure interne à l’aide d’une jointure groupée.</span><span class="sxs-lookup"><span data-stu-id="7ecc2-108">The first step in producing a left outer join of two collections is to perform an inner join by using a group join.</span></span> <span data-ttu-id="7ecc2-109">(Pour savoir comment faire, consultez [Effectuer des jointures internes](perform-inner-joins.md).) Dans cet exemple, la liste des objets `Person` est jointe par une jointure interne à la liste des objets `Pet` sur la base d’un objet `Person` qui correspond à `Pet.Owner`.</span><span class="sxs-lookup"><span data-stu-id="7ecc2-109">(See [Perform inner joins](perform-inner-joins.md) for an explanation of this process.) In this example, the list of `Person` objects is inner-joined to the list of `Pet` objects based on a `Person` object that matches `Pet.Owner`.</span></span>

<span data-ttu-id="7ecc2-110">La deuxième étape consiste à inclure tous les éléments de la première collection (celle de gauche) dans le jeu de résultats, y compris les éléments sans correspondance dans la collection de droite.</span><span class="sxs-lookup"><span data-stu-id="7ecc2-110">The second step is to include each element of the first (left) collection in the result set even if that element has no matches in the right collection.</span></span> <span data-ttu-id="7ecc2-111">Pour cela, appelez <xref:System.Linq.Enumerable.DefaultIfEmpty%2A> sur chaque séquence d’éléments correspondants de la jointure groupée.</span><span class="sxs-lookup"><span data-stu-id="7ecc2-111">This is accomplished by calling <xref:System.Linq.Enumerable.DefaultIfEmpty%2A> on each sequence of matching elements from the group join.</span></span> <span data-ttu-id="7ecc2-112">Dans cet exemple, la méthode <xref:System.Linq.Enumerable.DefaultIfEmpty%2A> est appelée sur chaque séquence d’objets `Pet` correspondants.</span><span class="sxs-lookup"><span data-stu-id="7ecc2-112">In this example, <xref:System.Linq.Enumerable.DefaultIfEmpty%2A> is called on each sequence of matching `Pet` objects.</span></span> <span data-ttu-id="7ecc2-113">La méthode retourne une collection qui contient uniquement une valeur par défaut si la séquence des objets `Pet` correspondants à un objet `Person` est vide, ce qui garantit que chaque objet `Person` est représenté dans la collection de résultats.</span><span class="sxs-lookup"><span data-stu-id="7ecc2-113">The method returns a collection that contains a single, default value if the sequence of matching `Pet` objects is empty for any `Person` object, thereby ensuring that each `Person` object is represented in the result collection.</span></span>

> [!NOTE]
> <span data-ttu-id="7ecc2-114">La valeur par défaut pour un type référence est `null`. L’exemple recherche donc une référence null avant d’accéder à chaque élément de chaque collection `Pet`.</span><span class="sxs-lookup"><span data-stu-id="7ecc2-114">The default value for a reference type is `null`; therefore, the example checks for a null reference before accessing each element of each `Pet` collection.</span></span>

[!code-csharp[CsLINQProgJoining#7](~/samples/snippets/csharp/concepts/linq/how-to-perform-left-outer-joins_1.cs)]

## <a name="see-also"></a><span data-ttu-id="7ecc2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ecc2-115">See also</span></span>

<xref:System.Linq.Enumerable.Join%2A>  
<xref:System.Linq.Enumerable.GroupJoin%2A>  
[<span data-ttu-id="7ecc2-116">Effectuer des jointures internes</span><span class="sxs-lookup"><span data-stu-id="7ecc2-116">Perform inner joins</span></span>](perform-inner-joins.md)  
[<span data-ttu-id="7ecc2-117">Effectuer des jointures groupées</span><span class="sxs-lookup"><span data-stu-id="7ecc2-117">Perform grouped joins</span></span>](perform-grouped-joins.md)  
[<span data-ttu-id="7ecc2-118">Types anonymes</span><span class="sxs-lookup"><span data-stu-id="7ecc2-118">Anonymous types</span></span>](../programming-guide/classes-and-structs/anonymous-types.md)  