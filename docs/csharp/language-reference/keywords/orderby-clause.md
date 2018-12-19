---
title: orderby, clause - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- orderby
- orderby_CSharpKeyword
helpviewer_keywords:
- orderby clause [C#]
- orderby keyword [C#]
ms.assetid: 21f87f48-d69d-4e95-9a52-6fec47b37e1f
ms.openlocfilehash: fc6e47270c4ae035a6387bf0e8d29efcd42e902f
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240981"
---
# <a name="orderby-clause-c-reference"></a><span data-ttu-id="45a17-102">orderby, clause (Référence C#)</span><span class="sxs-lookup"><span data-stu-id="45a17-102">orderby clause (C# Reference)</span></span>

<span data-ttu-id="45a17-103">Dans une expression de requête, la clause `orderby` a pour effet de trier la séquence ou la sous-séquence (groupe) retournée par ordre croissant ou décroissant.</span><span class="sxs-lookup"><span data-stu-id="45a17-103">In a query expression, the `orderby` clause causes the returned sequence or subsequence (group) to be sorted in either ascending or descending order.</span></span> <span data-ttu-id="45a17-104">Il est possible de spécifier plusieurs clés de façon à effectuer une ou plusieurs opérations de tri secondaire.</span><span class="sxs-lookup"><span data-stu-id="45a17-104">Multiple keys can be specified in order to perform one or more secondary sort operations.</span></span> <span data-ttu-id="45a17-105">Le tri est effectué par le comparateur par défaut du type de l’élément.</span><span class="sxs-lookup"><span data-stu-id="45a17-105">The sorting is performed by the default comparer for the type of the element.</span></span> <span data-ttu-id="45a17-106">L'ordre de tri par défaut est le tri croissant.</span><span class="sxs-lookup"><span data-stu-id="45a17-106">The default sort order is ascending.</span></span> <span data-ttu-id="45a17-107">Vous pouvez aussi spécifier un comparateur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="45a17-107">You can also specify a custom comparer.</span></span> <span data-ttu-id="45a17-108">Cependant, sa disponibilité est soumise à l’utilisation d’une syntaxe fondée sur une méthode.</span><span class="sxs-lookup"><span data-stu-id="45a17-108">However, it is only available by using method-based syntax.</span></span> <span data-ttu-id="45a17-109">Pour plus d’informations, consultez [Tri des données](../../programming-guide/concepts/linq/sorting-data.md).</span><span class="sxs-lookup"><span data-stu-id="45a17-109">For more information, see [Sorting Data](../../programming-guide/concepts/linq/sorting-data.md).</span></span>

## <a name="example"></a><span data-ttu-id="45a17-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="45a17-110">Example</span></span>

<span data-ttu-id="45a17-111">Dans l’exemple suivant, la première requête trie les mots par ordre alphabétique à partir de A, tandis que la deuxième requête trie les mêmes mots par ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="45a17-111">In the following example, the first query sorts the words in alphabetical order starting from A, and second query sorts the same words in descending order.</span></span> <span data-ttu-id="45a17-112">(Le mot clé `ascending` est la valeur de tri par défaut et peut être omis.)</span><span class="sxs-lookup"><span data-stu-id="45a17-112">(The `ascending` keyword is the default sort value and can be omitted.)</span></span>

[!code-csharp[cscsrefQueryKeywords#20](~/samples/snippets/csharp/VS_Snippets_VBCSharp/CsCsrefQueryKeywords/CS/Orderby.cs#20)]

## <a name="example"></a><span data-ttu-id="45a17-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="45a17-113">Example</span></span>

<span data-ttu-id="45a17-114">L’exemple suivant effectue un tri principal sur les noms des étudiants, puis un tri secondaire sur leurs prénoms.</span><span class="sxs-lookup"><span data-stu-id="45a17-114">The following example performs a primary sort on the students' last names, and then a secondary sort on their first names.</span></span>

[!code-csharp[cscsrefQueryKeywords#22](~/samples/snippets/csharp/VS_Snippets_VBCSharp/CsCsrefQueryKeywords/CS/Orderby.cs#22)]

## <a name="remarks"></a><span data-ttu-id="45a17-115">Notes</span><span class="sxs-lookup"><span data-stu-id="45a17-115">Remarks</span></span>

<span data-ttu-id="45a17-116">Au moment de la compilation, la clause `orderby` est traduite en appel à la méthode <xref:System.Linq.Enumerable.OrderBy%2A>.</span><span class="sxs-lookup"><span data-stu-id="45a17-116">At compile time, the `orderby` clause is translated to a call to the <xref:System.Linq.Enumerable.OrderBy%2A> method.</span></span> <span data-ttu-id="45a17-117">Les différentes clés présentes dans la clause `orderby` sont traduites en appels à la méthode <xref:System.Linq.Enumerable.ThenBy%2A>.</span><span class="sxs-lookup"><span data-stu-id="45a17-117">Multiple keys in the `orderby` clause translate to <xref:System.Linq.Enumerable.ThenBy%2A> method calls.</span></span>

## <a name="see-also"></a><span data-ttu-id="45a17-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45a17-118">See also</span></span>

- [<span data-ttu-id="45a17-119">Référence C#</span><span class="sxs-lookup"><span data-stu-id="45a17-119">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="45a17-120">Mots clés de requête (LINQ)</span><span class="sxs-lookup"><span data-stu-id="45a17-120">Query Keywords (LINQ)</span></span>](query-keywords.md)
- [<span data-ttu-id="45a17-121">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="45a17-121">Language Integrated Query (LINQ)</span></span>](../../linq/index.md)
- [<span data-ttu-id="45a17-122">group, clause</span><span class="sxs-lookup"><span data-stu-id="45a17-122">group clause</span></span>](group-clause.md)
- [<span data-ttu-id="45a17-123">Bien démarrer avec LINQ en C#</span><span class="sxs-lookup"><span data-stu-id="45a17-123">Getting Started with LINQ in C#</span></span>](../../programming-guide/concepts/linq/getting-started-with-linq.md)