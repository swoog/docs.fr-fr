---
title: Gérer des valeurs Null dans des expressions de requête (LINQ en C#)
description: Découvrez comment gérer des valeurs Null dans des expressions de requête LINQ en C#.
ms.date: 12/1/2016
ms.assetid: ac63ae8b-724d-4251-9334-528f4e884ae7
ms.openlocfilehash: 34cda0be5fa38422415b6c3927f40a0df95fc6a6
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2018
ms.locfileid: "37404101"
---
# <a name="handle-null-values-in-query-expressions"></a><span data-ttu-id="db05c-103">Gérer des valeurs Null dans des expressions de requête</span><span class="sxs-lookup"><span data-stu-id="db05c-103">Handle null values in query expressions</span></span>

<span data-ttu-id="db05c-104">Cet exemple montre comment gérer d’éventuelles valeurs Null dans des collections sources.</span><span class="sxs-lookup"><span data-stu-id="db05c-104">This example shows how to handle possible null values in source collections.</span></span> <span data-ttu-id="db05c-105">Une collection d’objets telle qu’un <xref:System.Collections.Generic.IEnumerable%601> peut contenir des éléments dont la valeur est [null](../language-reference/keywords/null.md).</span><span class="sxs-lookup"><span data-stu-id="db05c-105">An object collection such as an <xref:System.Collections.Generic.IEnumerable%601> can contain elements whose value is [null](../language-reference/keywords/null.md).</span></span> <span data-ttu-id="db05c-106">Si une collection source est null ou contient un élément dont la valeur est null et que votre requête ne gère pas les valeurs null, une <xref:System.NullReferenceException> est levée quand vous exécutez la requête.</span><span class="sxs-lookup"><span data-stu-id="db05c-106">If a source collection is null or contains an element whose value is null, and your query does not handle null values, a <xref:System.NullReferenceException> will be thrown when you execute the query.</span></span>

## <a name="example"></a><span data-ttu-id="db05c-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="db05c-107">Example</span></span>

<span data-ttu-id="db05c-108">Vous pouvez écrire du code en prévention pour éviter une exception de référence Null, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="db05c-108">You can code defensively to avoid a null reference exception as shown in the following example:</span></span>

[!code-csharp[csProgGuideLINQ#82](~/samples/snippets/csharp/concepts/linq/how-to-handle-null-values-in-query-expressions_1.cs)]

<span data-ttu-id="db05c-109">Dans l’exemple précédent, la clause `where` exclut tous les éléments Null de la séquence de catégories.</span><span class="sxs-lookup"><span data-stu-id="db05c-109">In the previous example, the `where` clause filters out all null elements in the categories sequence.</span></span> <span data-ttu-id="db05c-110">Cette technique est indépendante de la vérification de valeur Null de la clause join.</span><span class="sxs-lookup"><span data-stu-id="db05c-110">This technique is independent of the null check in the join clause.</span></span> <span data-ttu-id="db05c-111">Dans cet exemple, l’expression conditionnelle avec une valeur Null fonctionne, car `Products.CategoryID` est de type `int?`, qui est le raccourci de `Nullable<int>`.</span><span class="sxs-lookup"><span data-stu-id="db05c-111">The conditional expression with null in this example works because `Products.CategoryID` is of type `int?` which is shorthand for `Nullable<int>`.</span></span>

## <a name="example"></a><span data-ttu-id="db05c-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="db05c-112">Example</span></span>

<span data-ttu-id="db05c-113">Dans une clause join, si seulement l’une des clés de comparaison est un type valeur Nullable, vous pouvez caster l’autre clé en type Nullable dans l’expression de requête.</span><span class="sxs-lookup"><span data-stu-id="db05c-113">In a join clause, if only one of the comparison keys is a nullable value type, you can cast the other to a nullable type in the query expression.</span></span> <span data-ttu-id="db05c-114">Dans l’exemple suivant, supposons que `EmployeeID` soit une colonne qui contienne des valeurs de type `int?` :</span><span class="sxs-lookup"><span data-stu-id="db05c-114">In the following example, assume that `EmployeeID` is a column that contains values of type `int?`:</span></span>

[!code-csharp[csProgGuideLINQ#83](~/samples/snippets/csharp/concepts/linq/how-to-handle-null-values-in-query-expressions_2.cs)]

## <a name="see-also"></a><span data-ttu-id="db05c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db05c-115">See also</span></span>

<xref:System.Nullable%601>  
[<span data-ttu-id="db05c-116">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="db05c-116">Language Integrated Query (LINQ)</span></span>](index.md)  
[<span data-ttu-id="db05c-117">Types Nullable</span><span class="sxs-lookup"><span data-stu-id="db05c-117">Nullable types</span></span>](../programming-guide/nullable-types/index.md)  
