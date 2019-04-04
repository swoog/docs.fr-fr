---
title: Types valeur Nullable - Visual Basic
ms.date: 07/20/2015
f1_keywords:
- vb.Nullable
helpviewer_keywords:
- nullable types [Visual Basic]
- '? [Visual Basic]'
- types [Visual Basic], nullable
- nullable types [Visual Basic]
- data types [Visual Basic], nullable
ms.assetid: 9ac3b602-6f96-4e6d-96f7-cd4e81c468a6
ms.openlocfilehash: d17d2ad3fd99c6d563c21ddd646396ccb1c1ca48
ms.sourcegitcommit: a3db1a9eafca89f95ccf361bc1833b47fbb2bb30
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "58921310"
---
# <a name="nullable-value-types-visual-basic"></a><span data-ttu-id="e3485-102">Types valeur Nullable (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e3485-102">Nullable Value Types (Visual Basic)</span></span>

<span data-ttu-id="e3485-103">Parfois, vous travaillez avec un type valeur qui n’a pas une valeur définie dans certaines circonstances.</span><span class="sxs-lookup"><span data-stu-id="e3485-103">Sometimes you work with a value type that does not have a defined value in certain circumstances.</span></span> <span data-ttu-id="e3485-104">Par exemple, un champ dans une base de données peut devoir faire la distinction entre une valeur assignée est significative et n’ayant ne pas une valeur assignée.</span><span class="sxs-lookup"><span data-stu-id="e3485-104">For example, a field in a database might have to distinguish between having an assigned value that is meaningful and not having an assigned value.</span></span> <span data-ttu-id="e3485-105">Types de valeur peuvent être étendues pour prendre leurs valeurs normales ou une valeur null.</span><span class="sxs-lookup"><span data-stu-id="e3485-105">Value types can be extended to take either their normal values or a null value.</span></span> <span data-ttu-id="e3485-106">Cette extension est appelée un *type nullable*.</span><span class="sxs-lookup"><span data-stu-id="e3485-106">Such an extension is called a *nullable type*.</span></span>

<span data-ttu-id="e3485-107">Chaque type nullable est construit à partir de générique <xref:System.Nullable%601> structure.</span><span class="sxs-lookup"><span data-stu-id="e3485-107">Each nullable type is constructed from the generic <xref:System.Nullable%601> structure.</span></span> <span data-ttu-id="e3485-108">Considérons une base de données qui assure le suivi des activités liées à leur travail.</span><span class="sxs-lookup"><span data-stu-id="e3485-108">Consider a database that tracks work-related activities.</span></span> <span data-ttu-id="e3485-109">L’exemple suivant construit un nullable `Boolean` tapez et déclare une variable de ce type.</span><span class="sxs-lookup"><span data-stu-id="e3485-109">The following example constructs a nullable `Boolean` type and declares a variable of that type.</span></span> <span data-ttu-id="e3485-110">Vous pouvez écrire la déclaration de trois façons :</span><span class="sxs-lookup"><span data-stu-id="e3485-110">You can write the declaration in three ways:</span></span>

[!code-vb[VbVbalrNullableValue#1](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#1)]

<span data-ttu-id="e3485-111">La variable `ridesBusToWork` peut contenir une valeur de `True`, une valeur de `False`, ou aucune valeur.</span><span class="sxs-lookup"><span data-stu-id="e3485-111">The variable `ridesBusToWork` can hold a value of `True`, a value of `False`, or no value at all.</span></span> <span data-ttu-id="e3485-112">Sa valeur initiale par défaut n’est aucune valeur, qui dans ce cas signifie que les informations n’ont pas encore été obtenues pour cette personne.</span><span class="sxs-lookup"><span data-stu-id="e3485-112">Its initial default value is no value at all, which in this case could mean that the information has not yet been obtained for this person.</span></span> <span data-ttu-id="e3485-113">En revanche, `False` peut signifier que les informations ont été obtenues et que la personne ne puisse pas surfer sur le bus fonctionne.</span><span class="sxs-lookup"><span data-stu-id="e3485-113">In contrast, `False` could mean that the information has been obtained and the person does not ride the bus to work.</span></span>

<span data-ttu-id="e3485-114">Vous pouvez déclarer des variables et des propriétés avec des types nullables, et vous pouvez déclarer un tableau avec des éléments d’un type nullable.</span><span class="sxs-lookup"><span data-stu-id="e3485-114">You can declare variables and properties with nullable types, and you can declare an array with elements of a nullable type.</span></span> <span data-ttu-id="e3485-115">Vous pouvez déclarer des procédures avec des types nullable en tant que paramètres, et vous pouvez retourner un type nullable à partir d’un `Function` procédure.</span><span class="sxs-lookup"><span data-stu-id="e3485-115">You can declare procedures with nullable types as parameters, and you can return a nullable type from a `Function` procedure.</span></span>

<span data-ttu-id="e3485-116">Vous ne pouvez pas construire un type nullable sur un type référence tel qu’un tableau, un `String`, ou une classe.</span><span class="sxs-lookup"><span data-stu-id="e3485-116">You cannot construct a nullable type on a reference type such as an array, a `String`, or a class.</span></span> <span data-ttu-id="e3485-117">Le type sous-jacent doit être un type valeur.</span><span class="sxs-lookup"><span data-stu-id="e3485-117">The underlying type must be a value type.</span></span> <span data-ttu-id="e3485-118">Pour plus d'informations, consultez [Value Types and Reference Types](value-types-and-reference-types.md).</span><span class="sxs-lookup"><span data-stu-id="e3485-118">For more information, see [Value Types and Reference Types](value-types-and-reference-types.md).</span></span>

## <a name="using-a-nullable-type-variable"></a><span data-ttu-id="e3485-119">À l’aide d’une Variable de Type Nullable</span><span class="sxs-lookup"><span data-stu-id="e3485-119">Using a Nullable Type Variable</span></span>

<span data-ttu-id="e3485-120">Les membres les plus importants d’un type nullable sont ses <xref:System.Nullable%601.HasValue%2A> et <xref:System.Nullable%601.Value%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="e3485-120">The most important members of a nullable type are its <xref:System.Nullable%601.HasValue%2A> and <xref:System.Nullable%601.Value%2A> properties.</span></span> <span data-ttu-id="e3485-121">Pour une variable de type nullable, <xref:System.Nullable%601.HasValue%2A> vous indique si la variable contient une valeur définie.</span><span class="sxs-lookup"><span data-stu-id="e3485-121">For a variable of a nullable type, <xref:System.Nullable%601.HasValue%2A> tells you whether the variable contains a defined value.</span></span> <span data-ttu-id="e3485-122">Si <xref:System.Nullable%601.HasValue%2A> est `True`, vous pouvez lire la valeur à partir de <xref:System.Nullable%601.Value%2A>.</span><span class="sxs-lookup"><span data-stu-id="e3485-122">If <xref:System.Nullable%601.HasValue%2A> is `True`, you can read the value from <xref:System.Nullable%601.Value%2A>.</span></span> <span data-ttu-id="e3485-123">Notez que les deux <xref:System.Nullable%601.HasValue%2A> et <xref:System.Nullable%601.Value%2A> sont `ReadOnly` propriétés.</span><span class="sxs-lookup"><span data-stu-id="e3485-123">Note that both <xref:System.Nullable%601.HasValue%2A> and <xref:System.Nullable%601.Value%2A> are `ReadOnly` properties.</span></span>

### <a name="default-values"></a><span data-ttu-id="e3485-124">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="e3485-124">Default Values</span></span>

<span data-ttu-id="e3485-125">Lorsque vous déclarez une variable avec un type nullable, sa <xref:System.Nullable%601.HasValue%2A> propriété a la valeur par défaut `False`.</span><span class="sxs-lookup"><span data-stu-id="e3485-125">When you declare a variable with a nullable type, its <xref:System.Nullable%601.HasValue%2A> property has a default value of `False`.</span></span> <span data-ttu-id="e3485-126">Cela signifie que, par défaut, la variable n’a aucune valeur définie, au lieu de la valeur par défaut de son type valeur sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="e3485-126">This means that by default the variable has no defined value, instead of the default value of its underlying value type.</span></span> <span data-ttu-id="e3485-127">Dans l’exemple suivant, la variable `numberOfChildren` a d’initialement aucune valeur définie, même si la valeur par défaut de la `Integer` type a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="e3485-127">In the following example, the variable `numberOfChildren` initially has no defined value, even though the default value of the `Integer` type is 0.</span></span>

[!code-vb[VbVbalrNullableValue#2](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#2)]

<span data-ttu-id="e3485-128">Une valeur null est utile pour indiquer une valeur inconnue ou non définie.</span><span class="sxs-lookup"><span data-stu-id="e3485-128">A null value is useful to indicate an undefined or unknown value.</span></span> <span data-ttu-id="e3485-129">Si `numberOfChildren` avait été déclaré comme `Integer`, il n’y aurait aucun valeur qui peut indiquer que les informations ne sont pas disponibles actuellement.</span><span class="sxs-lookup"><span data-stu-id="e3485-129">If `numberOfChildren` had been declared as `Integer`, there would be no value that could indicate that the information is not currently available.</span></span>

### <a name="storing-values"></a><span data-ttu-id="e3485-130">Stockage de valeurs</span><span class="sxs-lookup"><span data-stu-id="e3485-130">Storing Values</span></span>

<span data-ttu-id="e3485-131">Vous stocker une valeur dans une variable ou une propriété d’un type nullable de la façon habituelle.</span><span class="sxs-lookup"><span data-stu-id="e3485-131">You store a value in a variable or property of a nullable type in the typical way.</span></span> <span data-ttu-id="e3485-132">L’exemple suivant assigne une valeur à la variable `numberOfChildren` déclaré dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="e3485-132">The following example assigns a value to the variable `numberOfChildren` declared in the previous example.</span></span>

[!code-vb[VbVbalrNullableValue#3](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#3)]

<span data-ttu-id="e3485-133">Si une variable ou une propriété d’un type nullable contient une valeur définie, vous pouvez le rendre revenir à son état initial de ne pas avoir une valeur assignée.</span><span class="sxs-lookup"><span data-stu-id="e3485-133">If a variable or property of a nullable type contains a defined value, you can cause it to revert to its initial state of not having a value assigned.</span></span> <span data-ttu-id="e3485-134">Pour cela en définissant la variable ou la propriété `Nothing`, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e3485-134">You do this by setting the variable or property to `Nothing`, as the following example shows.</span></span>

[!code-vb[VbVbalrNullableValue#4](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#4)]

> [!NOTE]
> <span data-ttu-id="e3485-135">Bien que vous puissiez attribuer `Nothing` à une variable d’un type nullable, vous ne pouvez pas tester pour `Nothing` à l’aide du signe égal.</span><span class="sxs-lookup"><span data-stu-id="e3485-135">Although you can assign `Nothing` to a variable of a nullable type, you cannot test it for `Nothing` by using the equal sign.</span></span> <span data-ttu-id="e3485-136">Comparaison qui utilise le signe égal, `someVar = Nothing`, a toujours la valeur `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="e3485-136">Comparison that uses the equal sign, `someVar = Nothing`, always evaluates to `Nothing`.</span></span> <span data-ttu-id="e3485-137">Vous pouvez tester la variable <xref:System.Nullable%601.HasValue%2A> propriété pour `False`, ou de test à l’aide de la `Is` ou `IsNot` opérateur.</span><span class="sxs-lookup"><span data-stu-id="e3485-137">You can test the variable's <xref:System.Nullable%601.HasValue%2A> property for `False`, or test by using the `Is` or `IsNot` operator.</span></span>

### <a name="retrieving-values"></a><span data-ttu-id="e3485-138">Récupération de valeurs</span><span class="sxs-lookup"><span data-stu-id="e3485-138">Retrieving Values</span></span>

<span data-ttu-id="e3485-139">Pour récupérer la valeur d’une variable d’un type nullable, vous devez tout d’abord tester son <xref:System.Nullable%601.HasValue%2A> propriété pour confirmer qu’il a une valeur.</span><span class="sxs-lookup"><span data-stu-id="e3485-139">To retrieve the value of a variable of a nullable type, you should first test its <xref:System.Nullable%601.HasValue%2A> property to confirm that it has a value.</span></span> <span data-ttu-id="e3485-140">Si vous essayez de lire la valeur lorsque <xref:System.Nullable%601.HasValue%2A> est `False`, Visual Basic lève une <xref:System.InvalidOperationException> exception.</span><span class="sxs-lookup"><span data-stu-id="e3485-140">If you try to read the value when <xref:System.Nullable%601.HasValue%2A> is `False`, Visual Basic throws an <xref:System.InvalidOperationException> exception.</span></span> <span data-ttu-id="e3485-141">L’exemple suivant montre la méthode recommandée pour lire la variable `numberOfChildren` des exemples précédents.</span><span class="sxs-lookup"><span data-stu-id="e3485-141">The following example shows the recommended way to read the variable `numberOfChildren` of the previous examples.</span></span>

[!code-vb[VbVbalrNullableValue#5](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#5)]

## <a name="comparing-nullable-types"></a><span data-ttu-id="e3485-142">Comparaison de Types Nullable</span><span class="sxs-lookup"><span data-stu-id="e3485-142">Comparing Nullable Types</span></span>

<span data-ttu-id="e3485-143">Lorsque nullable `Boolean` variables sont utilisées dans les expressions booléennes, le résultat peut être `True`, `False`, ou `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="e3485-143">When nullable `Boolean` variables are used in Boolean expressions, the result can be `True`, `False`, or `Nothing`.</span></span> <span data-ttu-id="e3485-144">Voici la table de vérité pour `And` et `Or`.</span><span class="sxs-lookup"><span data-stu-id="e3485-144">The following is the truth table for `And` and `Or`.</span></span> <span data-ttu-id="e3485-145">Étant donné que `b1` et `b2` ont maintenant des trois valeurs possibles, il existe neuf combinaisons à évaluer.</span><span class="sxs-lookup"><span data-stu-id="e3485-145">Because `b1` and `b2` now have three possible values, there are nine combinations to evaluate.</span></span>

|<span data-ttu-id="e3485-146">b1</span><span class="sxs-lookup"><span data-stu-id="e3485-146">b1</span></span>|<span data-ttu-id="e3485-147">b2</span><span class="sxs-lookup"><span data-stu-id="e3485-147">b2</span></span>|<span data-ttu-id="e3485-148">B1 et b2</span><span class="sxs-lookup"><span data-stu-id="e3485-148">b1 And b2</span></span>|<span data-ttu-id="e3485-149">B1 ou b2</span><span class="sxs-lookup"><span data-stu-id="e3485-149">b1 Or b2</span></span>|
|--------|--------|---------------|--------------|
|`Nothing`|`Nothing`|`Nothing`|`Nothing`|
|`Nothing`|`True`|`Nothing`|`True`|
|`Nothing`|`False`|`False`|`Nothing`|
|`True`|`Nothing`|`Nothing`|`True`|
|`True`|`True`|`True`|`True`|
|`True`|`False`|`False`|`True`|
|`False`|`Nothing`|`False`|`Nothing`|
|`False`|`True`|`False`|`True`|
|`False`|`False`|`False`|`False`|

<span data-ttu-id="e3485-150">Lorsque la valeur d’une variable ou expression booléenne est `Nothing`, il n’est ni `true` ni `false`.</span><span class="sxs-lookup"><span data-stu-id="e3485-150">When the value of a Boolean variable or expression is `Nothing`, it is neither `true` nor `false`.</span></span> <span data-ttu-id="e3485-151">Prenons l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e3485-151">Consider the following example.</span></span>

[!code-vb[VbVbalrNullableValue#6](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#6)]

<span data-ttu-id="e3485-152">Dans cet exemple, `b1 And b2` prend la valeur `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="e3485-152">In this example, `b1 And b2` evaluates to `Nothing`.</span></span> <span data-ttu-id="e3485-153">Par conséquent, le `Else` clause est exécutée dans chaque `If` instruction et la sortie est comme suit :</span><span class="sxs-lookup"><span data-stu-id="e3485-153">As a result, the `Else` clause is executed in each `If` statement, and the output is as follows:</span></span>

`Expression is not true`

`Expression is not false`

> [!NOTE]
> `AndAlso` <span data-ttu-id="e3485-154">et `OrElse`, qui utilisent l’évaluation de court-circuit doivent évaluer leurs opérandes deuxième lorsque le premier prend la valeur `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="e3485-154">and `OrElse`, which use short-circuit evaluation, must evaluate their second operands when the first evaluates to `Nothing`.</span></span>

## <a name="propagation"></a><span data-ttu-id="e3485-155">Propagation</span><span class="sxs-lookup"><span data-stu-id="e3485-155">Propagation</span></span>

<span data-ttu-id="e3485-156">Si une ou les deux opérandes d’une arithmétique, comparaison, MAJ ou une opération de type est nullable, le résultat de l’opération est également nullable.</span><span class="sxs-lookup"><span data-stu-id="e3485-156">If one or both of the operands of an arithmetic, comparison, shift, or type operation is nullable, the result of the operation is also nullable.</span></span> <span data-ttu-id="e3485-157">Si les deux opérandes ont des valeurs qui ne sont pas `Nothing`, l’opération est effectuée sur les valeurs sous-jacentes des opérandes, comme si aucune n’était un type nullable.</span><span class="sxs-lookup"><span data-stu-id="e3485-157">If both operands have values that are not `Nothing`, the operation is performed on the underlying values of the operands, as if neither were a nullable type.</span></span> <span data-ttu-id="e3485-158">Dans l’exemple suivant, les variables `compare1` et `sum1` sont implicitement typées.</span><span class="sxs-lookup"><span data-stu-id="e3485-158">In the following example, variables `compare1` and `sum1` are implicitly typed.</span></span> <span data-ttu-id="e3485-159">Si vous placez le pointeur de la souris au-dessus d’eux, vous verrez que le compilateur déduit les types nullable pour les deux.</span><span class="sxs-lookup"><span data-stu-id="e3485-159">If you rest the mouse pointer over them, you will see that the compiler infers nullable types for both of them.</span></span>

[!code-vb[VbVbalrNullableValue#7](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#7)]

<span data-ttu-id="e3485-160">Si un ou deux opérandes ont la valeur `Nothing`, le résultat sera `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="e3485-160">If one or both operands have a value of `Nothing`, the result will be `Nothing`.</span></span>

[!code-vb[VbVbalrNullableValue#8](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#8)]

## <a name="using-nullable-types-with-data"></a><span data-ttu-id="e3485-161">Utilisation de Types Nullable avec des données</span><span class="sxs-lookup"><span data-stu-id="e3485-161">Using Nullable Types with Data</span></span>

<span data-ttu-id="e3485-162">Une base de données est un des emplacements plus importants pour utiliser des types nullables.</span><span class="sxs-lookup"><span data-stu-id="e3485-162">A database is one of the most important places to use nullable types.</span></span> <span data-ttu-id="e3485-163">Pas tous les objets de base de données prend actuellement en charge les types nullable, mais que faire les adaptateurs de table généré par le concepteur.</span><span class="sxs-lookup"><span data-stu-id="e3485-163">Not all database objects currently support nullable types, but the designer-generated table adapters do.</span></span> <span data-ttu-id="e3485-164">Consultez [prise en charge du TableAdapter pour les types nullables](/visualstudio/data-tools/fill-datasets-by-using-tableadapters#tableadapter-support-for-nullable-types).</span><span class="sxs-lookup"><span data-stu-id="e3485-164">See [TableAdapter support for nullable types](/visualstudio/data-tools/fill-datasets-by-using-tableadapters#tableadapter-support-for-nullable-types).</span></span>

## <a name="see-also"></a><span data-ttu-id="e3485-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3485-165">See also</span></span>

- <xref:System.InvalidOperationException>
- <xref:System.Nullable%601.HasValue%2A>
- [<span data-ttu-id="e3485-166">Utilisation de types Nullable</span><span class="sxs-lookup"><span data-stu-id="e3485-166">Using Nullable Types</span></span>](../../../../csharp/programming-guide/nullable-types/using-nullable-types.md)
- [<span data-ttu-id="e3485-167">Types de données</span><span class="sxs-lookup"><span data-stu-id="e3485-167">Data Types</span></span>](index.md)
- [<span data-ttu-id="e3485-168">Types valeur et types référence</span><span class="sxs-lookup"><span data-stu-id="e3485-168">Value Types and Reference Types</span></span>](value-types-and-reference-types.md)
- [<span data-ttu-id="e3485-169">Dépannage des types de données</span><span class="sxs-lookup"><span data-stu-id="e3485-169">Troubleshooting Data Types</span></span>](troubleshooting-data-types.md)
- [<span data-ttu-id="e3485-170">Remplir des datasets à l’aide de TableAdapters</span><span class="sxs-lookup"><span data-stu-id="e3485-170">Fill datasets by using TableAdapters</span></span>](/visualstudio/data-tools/fill-datasets-by-using-tableadapters)
- [<span data-ttu-id="e3485-171">If, opérateur</span><span class="sxs-lookup"><span data-stu-id="e3485-171">If Operator</span></span>](../../../language-reference/operators/if-operator.md)
- [<span data-ttu-id="e3485-172">Inférence de type local</span><span class="sxs-lookup"><span data-stu-id="e3485-172">Local Type Inference</span></span>](../variables/local-type-inference.md)
- [<span data-ttu-id="e3485-173">Is, opérateur</span><span class="sxs-lookup"><span data-stu-id="e3485-173">Is Operator</span></span>](../../../language-reference/operators/is-operator.md)
- [<span data-ttu-id="e3485-174">IsNot, opérateur</span><span class="sxs-lookup"><span data-stu-id="e3485-174">IsNot Operator</span></span>](../../../language-reference/operators/isnot-operator.md)