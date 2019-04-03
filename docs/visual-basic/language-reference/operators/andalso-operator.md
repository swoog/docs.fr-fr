---
title: Opérateur AndAlso (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.AndAlso
- AndAlso
helpviewer_keywords:
- short-circuiting
- AndAlso operator [Visual Basic]
- operators [Visual Basic], short-circuiting
- operators [Visual Basic], conjunction
- short-circuit evaluation
ms.assetid: bbc15191-b374-495b-9b8f-7b8c2f4388eb
ms.openlocfilehash: 3876fd9c32d486b8ebecc9ee2428486a687a1624
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58817121"
---
# <a name="andalso-operator-visual-basic"></a><span data-ttu-id="29701-102">Opérateur AndAlso (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="29701-102">AndAlso Operator (Visual Basic)</span></span>
<span data-ttu-id="29701-103">Effectue une conjonction logique sur deux expressions de court-circuit.</span><span class="sxs-lookup"><span data-stu-id="29701-103">Performs short-circuiting logical conjunction on two expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="29701-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29701-104">Syntax</span></span>  
  
```  
result = expression1 AndAlso expression2  
```  
  
## <a name="parts"></a><span data-ttu-id="29701-105">Composants</span><span class="sxs-lookup"><span data-stu-id="29701-105">Parts</span></span>  
  
|<span data-ttu-id="29701-106">Terme</span><span class="sxs-lookup"><span data-stu-id="29701-106">Term</span></span>|<span data-ttu-id="29701-107">Définition</span><span class="sxs-lookup"><span data-stu-id="29701-107">Definition</span></span>|  
|---|---|  
|`result`|<span data-ttu-id="29701-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="29701-108">Required.</span></span> <span data-ttu-id="29701-109">Toute expression `Boolean` .</span><span class="sxs-lookup"><span data-stu-id="29701-109">Any `Boolean` expression.</span></span> <span data-ttu-id="29701-110">Le résultat est le `Boolean` résultat de la comparaison des deux expressions.</span><span class="sxs-lookup"><span data-stu-id="29701-110">The result is the `Boolean` result of comparison of the two expressions.</span></span>|  
|`expression1`|<span data-ttu-id="29701-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="29701-111">Required.</span></span> <span data-ttu-id="29701-112">Toute expression `Boolean` .</span><span class="sxs-lookup"><span data-stu-id="29701-112">Any `Boolean` expression.</span></span>|  
|`expression2`|<span data-ttu-id="29701-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="29701-113">Required.</span></span> <span data-ttu-id="29701-114">Toute expression `Boolean` .</span><span class="sxs-lookup"><span data-stu-id="29701-114">Any `Boolean` expression.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="29701-115">Notes</span><span class="sxs-lookup"><span data-stu-id="29701-115">Remarks</span></span>  
 <span data-ttu-id="29701-116">Une opération logique est dite *court-circuit* si le code compilé peut ignorer l’évaluation d’une expression en fonction du résultat d’une autre expression.</span><span class="sxs-lookup"><span data-stu-id="29701-116">A logical operation is said to be *short-circuiting* if the compiled code can bypass the evaluation of one expression depending on the result of another expression.</span></span> <span data-ttu-id="29701-117">Si le résultat de la première expression évaluée détermine le résultat final de l’opération, il n’est pas nécessaire pour évaluer la deuxième expression, car elle ne peut pas changer le résultat final.</span><span class="sxs-lookup"><span data-stu-id="29701-117">If the result of the first expression evaluated determines the final result of the operation, there is no need to evaluate the second expression, because it cannot change the final result.</span></span> <span data-ttu-id="29701-118">Un court-circuit peut améliorer les performances si l’expression ignorée est complexe, ou si elle implique des appels de procédure.</span><span class="sxs-lookup"><span data-stu-id="29701-118">Short-circuiting can improve performance if the bypassed expression is complex, or if it involves procedure calls.</span></span>  
  
 <span data-ttu-id="29701-119">Si les deux expressions ont `True`, `result` est `True`.</span><span class="sxs-lookup"><span data-stu-id="29701-119">If both expressions evaluate to `True`, `result` is `True`.</span></span> <span data-ttu-id="29701-120">Le tableau suivant illustre comment `result` est déterminée.</span><span class="sxs-lookup"><span data-stu-id="29701-120">The following table illustrates how `result` is determined.</span></span>  
  
|<span data-ttu-id="29701-121">Si `expression1` est</span><span class="sxs-lookup"><span data-stu-id="29701-121">If `expression1` is</span></span>|<span data-ttu-id="29701-122">Et `expression2` est</span><span class="sxs-lookup"><span data-stu-id="29701-122">And `expression2` is</span></span>|<span data-ttu-id="29701-123">La valeur de `result` est</span><span class="sxs-lookup"><span data-stu-id="29701-123">The value of `result` is</span></span>|  
|---|---|---|  
|`True`|`True`|`True`|  
|`True`|`False`|`False`|  
|`False`|<span data-ttu-id="29701-124">(non évalué)</span><span class="sxs-lookup"><span data-stu-id="29701-124">(not evaluated)</span></span>|`False`|  
  
## <a name="data-types"></a><span data-ttu-id="29701-125">Types de données</span><span class="sxs-lookup"><span data-stu-id="29701-125">Data Types</span></span>  
 <span data-ttu-id="29701-126">Le `AndAlso` opérateur est défini uniquement pour le [Type de données booléen](../../../visual-basic/language-reference/data-types/boolean-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="29701-126">The `AndAlso` operator is defined only for the [Boolean Data Type](../../../visual-basic/language-reference/data-types/boolean-data-type.md).</span></span> <span data-ttu-id="29701-127">Visual Basic convertit chaque opérande si nécessaire en `Boolean` et effectue l’opération entièrement en `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="29701-127">Visual Basic converts each operand as necessary to `Boolean` and performs the operation entirely in `Boolean`.</span></span> <span data-ttu-id="29701-128">Si vous affectez le résultat à un type numérique, Visual Basic convertit à partir de `Boolean` à ce type.</span><span class="sxs-lookup"><span data-stu-id="29701-128">If you assign the result to a numeric type, Visual Basic converts it from `Boolean` to that type.</span></span> <span data-ttu-id="29701-129">Cela peut entraîner un comportement inattendu.</span><span class="sxs-lookup"><span data-stu-id="29701-129">This could produce unexpected behavior.</span></span> <span data-ttu-id="29701-130">Par exemple, `5 AndAlso 12` entraîne `–1` lorsque converti en `Integer`.</span><span class="sxs-lookup"><span data-stu-id="29701-130">For example, `5 AndAlso 12` results in `–1` when converted to `Integer`.</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="29701-131">Surcharge</span><span class="sxs-lookup"><span data-stu-id="29701-131">Overloading</span></span>  
 <span data-ttu-id="29701-132">Le [opérateur et](../../../visual-basic/language-reference/operators/and-operator.md) et le [opérateur IsFalse](../../../visual-basic/language-reference/operators/isfalse-operator.md) peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir leur comportement lorsqu’un opérande a le type de ce classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="29701-132">The [And Operator](../../../visual-basic/language-reference/operators/and-operator.md) and the [IsFalse Operator](../../../visual-basic/language-reference/operators/isfalse-operator.md) can be *overloaded*, which means that a class or structure can redefine their behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="29701-133">La surcharge la `And` et `IsFalse` opérateurs affecte le comportement de la `AndAlso` opérateur.</span><span class="sxs-lookup"><span data-stu-id="29701-133">Overloading the `And` and `IsFalse` operators affects the behavior of the `AndAlso` operator.</span></span> <span data-ttu-id="29701-134">Si votre code utilise `AndAlso` sur une classe ou structure qui surcharge `And` et `IsFalse`, vérifiez que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="29701-134">If your code uses `AndAlso` on a class or structure that overloads `And` and `IsFalse`, be sure you understand their redefined behavior.</span></span> <span data-ttu-id="29701-135">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="29701-135">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="29701-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="29701-136">Example</span></span>  
 <span data-ttu-id="29701-137">L’exemple suivant utilise le `AndAlso` opérateur effectue une conjonction logique sur deux expressions.</span><span class="sxs-lookup"><span data-stu-id="29701-137">The following example uses the `AndAlso` operator to perform a logical conjunction on two expressions.</span></span> <span data-ttu-id="29701-138">Le résultat est un `Boolean` valeur qui indique si l’ensemble unies expression a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="29701-138">The result is a `Boolean` value that represents whether the entire conjoined expression is true.</span></span> <span data-ttu-id="29701-139">Si la première expression est `False`, la seconde n’est pas évaluée.</span><span class="sxs-lookup"><span data-stu-id="29701-139">If the first expression is `False`, the second is not evaluated.</span></span>  
  
 [!code-vb[VbVbalrOperators#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#24)]  
  
 <span data-ttu-id="29701-140">L’exemple précédent produit des résultats de `True`, `False`, et `False`, respectivement.</span><span class="sxs-lookup"><span data-stu-id="29701-140">The preceding example produces results of `True`, `False`, and `False`, respectively.</span></span> <span data-ttu-id="29701-141">Dans le calcul de `secondCheck`, la seconde expression n’est pas évaluée, car le premier est déjà `False`.</span><span class="sxs-lookup"><span data-stu-id="29701-141">In the calculation of `secondCheck`, the second expression is not evaluated because the first is already `False`.</span></span> <span data-ttu-id="29701-142">Toutefois, la seconde expression est évaluée dans le calcul de `thirdCheck`.</span><span class="sxs-lookup"><span data-stu-id="29701-142">However, the second expression is evaluated in the calculation of `thirdCheck`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="29701-143">Exemple</span><span class="sxs-lookup"><span data-stu-id="29701-143">Example</span></span>  
 <span data-ttu-id="29701-144">L’exemple suivant montre un `Function` procédure recherche une valeur donnée parmi les éléments d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="29701-144">The following example shows a `Function` procedure that searches for a given value among the elements of an array.</span></span> <span data-ttu-id="29701-145">Si le tableau est vide ou si la longueur du tableau a été dépassée, le `While` instruction ne teste pas l’élément de tableau par rapport à la valeur de recherche.</span><span class="sxs-lookup"><span data-stu-id="29701-145">If the array is empty, or if the array length has been exceeded, the `While` statement does not test the array element against the search value.</span></span>  
  
 [!code-vb[VbVbalrOperators#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#25)]  
  
## <a name="see-also"></a><span data-ttu-id="29701-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29701-146">See also</span></span>

- [<span data-ttu-id="29701-147">Opérateurs logiques/de bits (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="29701-147">Logical/Bitwise Operators (Visual Basic)</span></span>](../../../visual-basic/language-reference/operators/logical-bitwise-operators.md)
- [<span data-ttu-id="29701-148">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="29701-148">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="29701-149">Opérateurs répertoriés par fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="29701-149">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="29701-150">And (opérateur)</span><span class="sxs-lookup"><span data-stu-id="29701-150">And Operator</span></span>](../../../visual-basic/language-reference/operators/and-operator.md)
- [<span data-ttu-id="29701-151">IsFalse (opérateur)</span><span class="sxs-lookup"><span data-stu-id="29701-151">IsFalse Operator</span></span>](../../../visual-basic/language-reference/operators/isfalse-operator.md)
- [<span data-ttu-id="29701-152">Opérateurs logiques et au niveau du bit en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="29701-152">Logical and Bitwise Operators in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
