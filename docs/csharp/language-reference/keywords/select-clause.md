---
title: select, clause (Référence C#)
ms.date: 07/20/2015
f1_keywords:
- select_CSharpKeyword
- select
helpviewer_keywords:
- select keyword [C#]
- select clause [C#]
ms.assetid: df01e266-5781-4aaa-80c4-67cf28ea093f
ms.openlocfilehash: 3fa60d4e7546fc88ac2a2ffea45ae69b0da7a6a6
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53130899"
---
# <a name="select-clause-c-reference"></a><span data-ttu-id="cde96-102">select, clause (Référence C#)</span><span class="sxs-lookup"><span data-stu-id="cde96-102">select clause (C# Reference)</span></span>

<span data-ttu-id="cde96-103">Dans une expression de requête, la clause `select` spécifie le type de valeurs qui sont générées quand la requête est exécutée.</span><span class="sxs-lookup"><span data-stu-id="cde96-103">In a query expression, the `select` clause specifies the type of values that will be produced when the query is executed.</span></span> <span data-ttu-id="cde96-104">Le résultat est basé sur l’évaluation de toutes les clauses précédentes et sur toutes les expressions de la clause `select` elle-même.</span><span class="sxs-lookup"><span data-stu-id="cde96-104">The result is based on the evaluation of all the previous clauses and on any expressions in the `select` clause itself.</span></span> <span data-ttu-id="cde96-105">Une expression de requête doit se terminer par une clause `select` ou par une clause [group](group-clause.md).</span><span class="sxs-lookup"><span data-stu-id="cde96-105">A query expression must terminate with either a `select` clause or a [group](group-clause.md) clause.</span></span>

<span data-ttu-id="cde96-106">L’exemple suivant présente une clause `select` simple dans une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="cde96-106">The following example shows a simple `select` clause in a query expression.</span></span>

[!code-csharp[cscsrefQueryKeywords#8](~/samples/snippets/csharp/VS_Snippets_VBCSharp/CsCsrefQueryKeywords/CS/Select.cs#8)]  

<span data-ttu-id="cde96-107">Le type de la séquence générée par la clause `select` détermine le type de la variable de requête `queryHighScores`.</span><span class="sxs-lookup"><span data-stu-id="cde96-107">The type of the sequence produced by the `select` clause determines the type of the query variable `queryHighScores`.</span></span> <span data-ttu-id="cde96-108">Dans le cas le plus simple, la clause `select` spécifie uniquement la variable de portée.</span><span class="sxs-lookup"><span data-stu-id="cde96-108">In the simplest case, the `select` clause just specifies the range variable.</span></span> <span data-ttu-id="cde96-109">La séquence retournée contient alors des éléments du même type que la source de données.</span><span class="sxs-lookup"><span data-stu-id="cde96-109">This causes the returned sequence to contain elements of the same type as the data source.</span></span> <span data-ttu-id="cde96-110">Pour plus d’informations, consultez [Relations des types dans des opérations de requête LINQ](../../programming-guide/concepts/linq/type-relationships-in-linq-query-operations.md).</span><span class="sxs-lookup"><span data-stu-id="cde96-110">For more information, see [Type Relationships in LINQ Query Operations](../../programming-guide/concepts/linq/type-relationships-in-linq-query-operations.md).</span></span> <span data-ttu-id="cde96-111">Toutefois, la clause `select` fournit également un mécanisme puissant pour transformer (ou *projeter*) les données sources en nouveaux types.</span><span class="sxs-lookup"><span data-stu-id="cde96-111">However, the `select` clause also provides a powerful mechanism for transforming (or *projecting*) source data into new types.</span></span> <span data-ttu-id="cde96-112">Pour plus d’informations, consultez [Transformations de données avec LINQ (C#)](../../programming-guide/concepts/linq/data-transformations-with-linq.md).</span><span class="sxs-lookup"><span data-stu-id="cde96-112">For more information, see [Data Transformations with LINQ (C#)](../../programming-guide/concepts/linq/data-transformations-with-linq.md).</span></span>

## <a name="example"></a><span data-ttu-id="cde96-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="cde96-113">Example</span></span>

<span data-ttu-id="cde96-114">L’exemple suivant affiche l’ensemble des différentes formes que peut prendre une clause `select`.</span><span class="sxs-lookup"><span data-stu-id="cde96-114">The following example shows all the different forms that a `select` clause may take.</span></span> <span data-ttu-id="cde96-115">Dans chaque requête, notez la relation entre la clause `select` et le type de la *variable de requête* (`studentQuery1`, `studentQuery2`, etc.).</span><span class="sxs-lookup"><span data-stu-id="cde96-115">In each query, note the relationship between the `select` clause and the type of the *query variable* (`studentQuery1`, `studentQuery2`, and so on).</span></span>

[!code-csharp[cscsrefQueryKeywords#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/CsCsrefQueryKeywords/CS/Select.cs#9)]

<span data-ttu-id="cde96-116">Comme indiqué dans `studentQuery8` dans l’exemple précédent, vous pouvez parfois souhaiter que les éléments de la séquence retournée contiennent uniquement un sous-ensemble des propriétés des éléments sources.</span><span class="sxs-lookup"><span data-stu-id="cde96-116">As shown in `studentQuery8` in the previous example, sometimes you might want the elements of the returned sequence to contain only a subset of the properties of the source elements.</span></span> <span data-ttu-id="cde96-117">En limitant au maximum la séquence retournée, vous pouvez réduire les besoins en ressources mémoire et augmenter la vitesse d’exécution de la requête.</span><span class="sxs-lookup"><span data-stu-id="cde96-117">By keeping the returned sequence as small as possible you can reduce the memory requirements and increase the speed of the execution of the query.</span></span> <span data-ttu-id="cde96-118">Pour ce faire, créez un type anonyme dans la clause `select` et utilisez un initialiseur d’objet pour l’initialiser avec les propriétés appropriées de l’élément source.</span><span class="sxs-lookup"><span data-stu-id="cde96-118">You can accomplish this by creating an anonymous type in the `select` clause and using an object initializer to initialize it with the appropriate properties from the source element.</span></span> <span data-ttu-id="cde96-119">Pour obtenir un exemple de la procédure à suivre, consultez [Initialiseurs d’objet et de collection](../../programming-guide/classes-and-structs/object-and-collection-initializers.md).</span><span class="sxs-lookup"><span data-stu-id="cde96-119">For an example of how to do this, see [Object and Collection Initializers](../../programming-guide/classes-and-structs/object-and-collection-initializers.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cde96-120">Notes</span><span class="sxs-lookup"><span data-stu-id="cde96-120">Remarks</span></span>

<span data-ttu-id="cde96-121">Au moment de la compilation, la clause `select` traduite en un appel de méthode à l’opérateur de requête standard <xref:System.Linq.Enumerable.Select%2A>.</span><span class="sxs-lookup"><span data-stu-id="cde96-121">At compile time, the `select` clause is translated to a method call to the <xref:System.Linq.Enumerable.Select%2A> standard query operator.</span></span>

## <a name="see-also"></a><span data-ttu-id="cde96-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cde96-122">See also</span></span>

- [<span data-ttu-id="cde96-123">Référence C#</span><span class="sxs-lookup"><span data-stu-id="cde96-123">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="cde96-124">Mots clés de requête (LINQ)</span><span class="sxs-lookup"><span data-stu-id="cde96-124">Query Keywords (LINQ)</span></span>](query-keywords.md)
- [<span data-ttu-id="cde96-125">from, clause</span><span class="sxs-lookup"><span data-stu-id="cde96-125">from clause</span></span>](from-clause.md)
- [<span data-ttu-id="cde96-126">partial, méthode (Référence C#)</span><span class="sxs-lookup"><span data-stu-id="cde96-126">partial (Method) (C# Reference)</span></span>](partial-method.md)
- [<span data-ttu-id="cde96-127">Types anonymes</span><span class="sxs-lookup"><span data-stu-id="cde96-127">Anonymous Types</span></span>](../../programming-guide/classes-and-structs/anonymous-types.md)
- [<span data-ttu-id="cde96-128">Expressions de requête LINQ</span><span class="sxs-lookup"><span data-stu-id="cde96-128">LINQ Query Expressions</span></span>](../../programming-guide/linq-query-expressions/index.md)
- [<span data-ttu-id="cde96-129">Bien démarrer avec LINQ en C#</span><span class="sxs-lookup"><span data-stu-id="cde96-129">Getting Started with LINQ in C#</span></span>](../../programming-guide/concepts/linq/getting-started-with-linq.md)