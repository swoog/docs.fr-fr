---
title: Regrouper les résultats d’une requête (LINQ en C#)
description: Découvrez comment regrouper les résultats à l’aide de LINQ en C#.
ms.date: 12/1/2016
ms.assetid: 2e4ec27f-06fb-4de7-8973-0189906d4520
ms.openlocfilehash: f768718cb1435efdc67791612776c9e9ce2b14b8
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43798331"
---
# <a name="group-query-results"></a><span data-ttu-id="e746a-103">Regrouper les résultats d’une requête</span><span class="sxs-lookup"><span data-stu-id="e746a-103">Group query results</span></span>

<span data-ttu-id="e746a-104">Le regroupement est l’une des fonctionnalités les plus puissantes de LINQ.</span><span class="sxs-lookup"><span data-stu-id="e746a-104">Grouping is one of the most powerful capabilities of LINQ.</span></span> <span data-ttu-id="e746a-105">Les exemples suivants montrent comment regrouper des données de différentes manières :</span><span class="sxs-lookup"><span data-stu-id="e746a-105">The following examples show how to group data in various ways:</span></span>

- <span data-ttu-id="e746a-106">Selon une propriété</span><span class="sxs-lookup"><span data-stu-id="e746a-106">By a single property.</span></span>

- <span data-ttu-id="e746a-107">Selon la première lettre d’une propriété de chaîne</span><span class="sxs-lookup"><span data-stu-id="e746a-107">By the first letter of a string property.</span></span>

- <span data-ttu-id="e746a-108">Selon une plage numérique calculée</span><span class="sxs-lookup"><span data-stu-id="e746a-108">By a computed numeric range.</span></span>

- <span data-ttu-id="e746a-109">Selon un prédicat booléen ou une autre expression</span><span class="sxs-lookup"><span data-stu-id="e746a-109">By Boolean predicate or other expression.</span></span>

- <span data-ttu-id="e746a-110">Selon une clé composée</span><span class="sxs-lookup"><span data-stu-id="e746a-110">By a compound key.</span></span>

<span data-ttu-id="e746a-111">En outre, les deux dernières requêtes projettent leurs résultats dans un nouveau type anonyme qui contient uniquement le prénom et le nom de l’étudiant.</span><span class="sxs-lookup"><span data-stu-id="e746a-111">In addition, the last two queries project their results into a new anonymous type that contains only the student's first and last name.</span></span> <span data-ttu-id="e746a-112">Pour plus d’informations, consultez [group, clause](../language-reference/keywords/group-clause.md).</span><span class="sxs-lookup"><span data-stu-id="e746a-112">For more information, see the [group clause](../language-reference/keywords/group-clause.md).</span></span>

## <a name="example"></a><span data-ttu-id="e746a-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="e746a-113">Example</span></span>

<span data-ttu-id="e746a-114">Tous les exemples de cette rubrique utilisent les classes d’assistance et les sources de données suivantes.</span><span class="sxs-lookup"><span data-stu-id="e746a-114">All the examples in this topic use the following helper classes and data sources.</span></span>

[!code-csharp[csProgGuideLINQ#15](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_1.cs)]

## <a name="example"></a><span data-ttu-id="e746a-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="e746a-115">Example</span></span>

<span data-ttu-id="e746a-116">L’exemple suivant montre comment regrouper des éléments source en utilisant une propriété de l’élément comme clé de groupe.</span><span class="sxs-lookup"><span data-stu-id="e746a-116">The following example shows how to group source elements by using a single property of the element as the group key.</span></span> <span data-ttu-id="e746a-117">Dans ce cas, la clé est un `string`, qui correspond au nom de l’étudiant.</span><span class="sxs-lookup"><span data-stu-id="e746a-117">In this case the key is a `string`, the student's last name.</span></span> <span data-ttu-id="e746a-118">Il est également possible d’utiliser une sous-chaîne comme clé.</span><span class="sxs-lookup"><span data-stu-id="e746a-118">It is also possible to use a substring for the key.</span></span> <span data-ttu-id="e746a-119">L’opération de regroupement utilise le comparateur d’égalité par défaut pour le type.</span><span class="sxs-lookup"><span data-stu-id="e746a-119">The grouping operation uses the default equality comparer for the type.</span></span>

<span data-ttu-id="e746a-120">Copiez-collez la méthode suivante dans la classe `StudentClass`.</span><span class="sxs-lookup"><span data-stu-id="e746a-120">Paste the following method into the `StudentClass` class.</span></span> <span data-ttu-id="e746a-121">Remplacez l’instruction d’appel de la méthode `Main` par `sc.GroupBySingleProperty()`.</span><span class="sxs-lookup"><span data-stu-id="e746a-121">Change the calling statement in the `Main` method to `sc.GroupBySingleProperty()`.</span></span>

[!code-csharp[csProgGuideLINQ#17](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_2.cs)]

## <a name="example"></a><span data-ttu-id="e746a-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="e746a-122">Example</span></span>

<span data-ttu-id="e746a-123">L’exemple suivant montre comment regrouper des éléments source en utilisant autre chose qu’une propriété de l’objet comme clé de groupe.</span><span class="sxs-lookup"><span data-stu-id="e746a-123">The following example shows how to group source elements by using something other than a property of the object for the group key.</span></span> <span data-ttu-id="e746a-124">Dans cet exemple, la clé est la première lettre du nom de l’étudiant.</span><span class="sxs-lookup"><span data-stu-id="e746a-124">In this example, the key is the first letter of the student's last name.</span></span>

<span data-ttu-id="e746a-125">Copiez-collez la méthode suivante dans la classe `StudentClass`.</span><span class="sxs-lookup"><span data-stu-id="e746a-125">Paste the following method into the `StudentClass` class.</span></span> <span data-ttu-id="e746a-126">Remplacez l’instruction d’appel de la méthode `Main` par `sc.GroupBySubstring()`.</span><span class="sxs-lookup"><span data-stu-id="e746a-126">Change the calling statement in the `Main` method to `sc.GroupBySubstring()`.</span></span>

[!code-csharp[csProgGuideLINQ#18](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_3.cs)]

## <a name="example"></a><span data-ttu-id="e746a-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="e746a-127">Example</span></span>

<span data-ttu-id="e746a-128">L’exemple suivant montre comment regrouper des éléments source en utilisant une plage numérique comme clé de groupe.</span><span class="sxs-lookup"><span data-stu-id="e746a-128">The following example shows how to group source elements by using a numeric range as a group key.</span></span> <span data-ttu-id="e746a-129">La requête projette ensuite les résultats dans un type anonyme qui contient uniquement le prénom et le nom de l’étudiant, ainsi que la plage de centiles à laquelle appartient l’étudiant.</span><span class="sxs-lookup"><span data-stu-id="e746a-129">The query then projects the results into an anonymous type that contains only the first and last name and the percentile range to which the student belongs.</span></span> <span data-ttu-id="e746a-130">Un type anonyme est utilisé, car il n’est pas nécessaire d’utiliser l’intégralité de l’objet `Student` pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="e746a-130">An anonymous type is used because it is not necessary to use the complete `Student` object to display the results.</span></span> <span data-ttu-id="e746a-131">`GetPercentile` est une fonction d’assistance qui calcule un centile à partir de la note moyenne obtenue par l’étudiant.</span><span class="sxs-lookup"><span data-stu-id="e746a-131">`GetPercentile` is a helper function that calculates a percentile based on the student's average score.</span></span> <span data-ttu-id="e746a-132">La méthode retourne un entier compris entre 0 et 10.</span><span class="sxs-lookup"><span data-stu-id="e746a-132">The method returns an integer between 0 and 10.</span></span>

[!code-csharp[csProgGuideLINQ#50](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_4.cs)]

<span data-ttu-id="e746a-133">Copiez-collez la méthode suivante dans la classe `StudentClass`.</span><span class="sxs-lookup"><span data-stu-id="e746a-133">Paste the following method into the `StudentClass` class.</span></span> <span data-ttu-id="e746a-134">Remplacez l’instruction d’appel de la méthode `Main` par `sc.GroupByRange()`.</span><span class="sxs-lookup"><span data-stu-id="e746a-134">Change the calling statement in the `Main` method to `sc.GroupByRange()`.</span></span>

[!code-csharp[csProgGuideLINQ#19](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_5.cs)]

## <a name="example"></a><span data-ttu-id="e746a-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="e746a-135">Example</span></span>

<span data-ttu-id="e746a-136">L’exemple suivant montre comment regrouper des éléments source en utilisant une expression de comparaison booléenne.</span><span class="sxs-lookup"><span data-stu-id="e746a-136">The following example shows how to group source elements by using a Boolean comparison expression.</span></span> <span data-ttu-id="e746a-137">Dans cet exemple, l’expression booléenne teste si la note moyenne d’un étudiant est supérieure à 75.</span><span class="sxs-lookup"><span data-stu-id="e746a-137">In this example, the Boolean expression tests whether a student's average exam score is greater than 75.</span></span> <span data-ttu-id="e746a-138">Comme dans les exemples précédents, les résultats sont projetés dans un type anonyme, car il n’est pas nécessaire d’avoir l’élément source complet.</span><span class="sxs-lookup"><span data-stu-id="e746a-138">As in previous examples, the results are projected into an anonymous type because the complete source element is not needed.</span></span> <span data-ttu-id="e746a-139">Notez que les propriétés du type anonyme deviennent des propriétés du membre `Key` et sont accessibles par nom lorsque la requête est exécutée.</span><span class="sxs-lookup"><span data-stu-id="e746a-139">Note that the properties in the anonymous type become properties on the `Key` member and can be accessed by name when the query is executed.</span></span>

<span data-ttu-id="e746a-140">Copiez-collez la méthode suivante dans la classe `StudentClass`.</span><span class="sxs-lookup"><span data-stu-id="e746a-140">Paste the following method into the `StudentClass` class.</span></span> <span data-ttu-id="e746a-141">Remplacez l’instruction d’appel de la méthode `Main` par `sc.GroupByBoolean()`.</span><span class="sxs-lookup"><span data-stu-id="e746a-141">Change the calling statement in the `Main` method to `sc.GroupByBoolean()`.</span></span>

[!code-csharp[csProgGuideLINQ#20](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_6.cs)]

## <a name="example"></a><span data-ttu-id="e746a-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="e746a-142">Example</span></span>

<span data-ttu-id="e746a-143">L’exemple suivant montre comment utiliser un type anonyme pour encapsuler une clé qui contient plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="e746a-143">The following example shows how to use an anonymous type to encapsulate a key that contains multiple values.</span></span> <span data-ttu-id="e746a-144">Dans cet exemple, la première valeur de clé est la première lettre du nom de l’étudiant.</span><span class="sxs-lookup"><span data-stu-id="e746a-144">In this example, the first key value is the first letter of the student's last name.</span></span> <span data-ttu-id="e746a-145">La deuxième valeur de clé est une valeur booléenne qui spécifie si l’étudiant a obtenu une note supérieure à 85 au premier examen.</span><span class="sxs-lookup"><span data-stu-id="e746a-145">The second key value is a Boolean that specifies whether the student scored over 85 on the first exam.</span></span> <span data-ttu-id="e746a-146">Vous pouvez organiser les groupes selon n’importe quelle propriété de la clé.</span><span class="sxs-lookup"><span data-stu-id="e746a-146">You can order the groups by any property in the key.</span></span>

<span data-ttu-id="e746a-147">Copiez-collez la méthode suivante dans la classe `StudentClass`.</span><span class="sxs-lookup"><span data-stu-id="e746a-147">Paste the following method into the `StudentClass` class.</span></span> <span data-ttu-id="e746a-148">Remplacez l’instruction d’appel de la méthode `Main` par `sc.GroupByCompositeKey()`.</span><span class="sxs-lookup"><span data-stu-id="e746a-148">Change the calling statement in the `Main` method to `sc.GroupByCompositeKey()`.</span></span>

[!code-csharp[csProgGuideLINQ#21](~/samples/snippets/csharp/concepts/linq/how-to-group-query-results_7.cs)]

## <a name="see-also"></a><span data-ttu-id="e746a-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e746a-149">See also</span></span>

- <xref:System.Linq.Enumerable.GroupBy%2A>  
- <xref:System.Linq.IGrouping%602>  
- [<span data-ttu-id="e746a-150">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="e746a-150">Language Integrated Query (LINQ)</span></span>](index.md)  
- [<span data-ttu-id="e746a-151">group, clause</span><span class="sxs-lookup"><span data-stu-id="e746a-151">group clause</span></span>](../language-reference/keywords/group-clause.md)  
- [<span data-ttu-id="e746a-152">Types anonymes</span><span class="sxs-lookup"><span data-stu-id="e746a-152">Anonymous Types</span></span>](../programming-guide/classes-and-structs/anonymous-types.md)  
- [<span data-ttu-id="e746a-153">Effectuer une sous-requête sur une opération de regroupement</span><span class="sxs-lookup"><span data-stu-id="e746a-153">Perform a Subquery on a Grouping Operation</span></span>](perform-a-subquery-on-a-grouping-operation.md)  
- [<span data-ttu-id="e746a-154">Créer un groupe imbriqué</span><span class="sxs-lookup"><span data-stu-id="e746a-154">Create a Nested Group</span></span>](create-a-nested-group.md)  
- [<span data-ttu-id="e746a-155">Regroupement de données</span><span class="sxs-lookup"><span data-stu-id="e746a-155">Grouping Data</span></span>](../programming-guide/concepts/linq/grouping-data.md)  