---
title: Xor, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Xor
helpviewer_keywords:
- exclusive OR operator [Visual Basic]
- logical exclusion
- operators [Visual Basic], exclusive or
- exclusion operator [Visual Basic]
- operators [Visual Basic], bitwise
- bitwise operators [Visual Basic], XOR operator
- Xor operator [Visual Basic]
- Xor keyword [Visual Basic]
- bitwise comparison [Visual Basic]
ms.assetid: 036000a9-3934-4e7f-a9d0-a816de3d84a6
ms.openlocfilehash: 0cba3a995fb1ab774c8a5308e58f0b6905fc23f3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58827066"
---
# <a name="xor-operator-visual-basic"></a><span data-ttu-id="e2a4c-102">Xor, opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e2a4c-102">Xor Operator (Visual Basic)</span></span>
<span data-ttu-id="e2a4c-103">Effectue une exclusion logique sur deux `Boolean` expressions ou une exclusion au niveau du bit sur deux expressions numériques.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-103">Performs a logical exclusion on two `Boolean` expressions, or a bitwise exclusion on two numeric expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2a4c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2a4c-104">Syntax</span></span>  
  
```  
result = expression1 Xor expression2  
```  
  
## <a name="parts"></a><span data-ttu-id="e2a4c-105">Composants</span><span class="sxs-lookup"><span data-stu-id="e2a4c-105">Parts</span></span>  
 `result`  
 <span data-ttu-id="e2a4c-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-106">Required.</span></span> <span data-ttu-id="e2a4c-107">N’importe quel `Boolean` ou variable numérique.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-107">Any `Boolean` or numeric variable.</span></span> <span data-ttu-id="e2a4c-108">Pour une comparaison booléenne, `result` est l’exclusion logique (disjonction logique exclusive) de deux `Boolean` valeurs.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-108">For Boolean comparison, `result` is the logical exclusion (exclusive logical disjunction) of two `Boolean` values.</span></span> <span data-ttu-id="e2a4c-109">Pour les opérations au niveau du bit, `result` est une valeur numérique représentant l’exclusion de bits (disjonction de bits exclusive) de deux modèles binaires numériques.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-109">For bitwise operations, `result` is a numeric value that represents the bitwise exclusion (exclusive bitwise disjunction) of two numeric bit patterns.</span></span>  
  
 `expression1`  
 <span data-ttu-id="e2a4c-110">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-110">Required.</span></span> <span data-ttu-id="e2a4c-111">N’importe quel `Boolean` ou expression numérique.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-111">Any `Boolean` or numeric expression.</span></span>  
  
 `expression2`  
 <span data-ttu-id="e2a4c-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-112">Required.</span></span> <span data-ttu-id="e2a4c-113">N’importe quel `Boolean` ou expression numérique.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-113">Any `Boolean` or numeric expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e2a4c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e2a4c-114">Remarks</span></span>  
 <span data-ttu-id="e2a4c-115">Pour une comparaison booléenne, `result` est `True` si et seulement si un seul des `expression1` et `expression2` prend la valeur `True`.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-115">For Boolean comparison, `result` is `True` if and only if exactly one of `expression1` and `expression2` evaluates to `True`.</span></span> <span data-ttu-id="e2a4c-116">Autrement dit, si et seulement si `expression1` et `expression2` évaluer opposé à `Boolean` valeurs.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-116">That is, if and only if `expression1` and `expression2` evaluate to opposite `Boolean` values.</span></span> <span data-ttu-id="e2a4c-117">Le tableau suivant illustre comment `result` est déterminée.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-117">The following table illustrates how `result` is determined.</span></span>  
  
|<span data-ttu-id="e2a4c-118">Si `expression1` est</span><span class="sxs-lookup"><span data-stu-id="e2a4c-118">If `expression1` is</span></span>|<span data-ttu-id="e2a4c-119">Et `expression2` est</span><span class="sxs-lookup"><span data-stu-id="e2a4c-119">And `expression2` is</span></span>|<span data-ttu-id="e2a4c-120">La valeur de `result` est</span><span class="sxs-lookup"><span data-stu-id="e2a4c-120">The value of `result` is</span></span>|  
|-------------------------|--------------------------|------------------------------|  
|`True`|`True`|`False`|  
|`True`|`False`|`True`|  
|`False`|`True`|`True`|  
|`False`|`False`|`False`|  
  
> [!NOTE]
>  <span data-ttu-id="e2a4c-121">Dans une comparaison booléenne, le `Xor` opérateur évalue toujours les deux expressions, ce qui peut inclure des appels de procédure.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-121">In a Boolean comparison, the `Xor` operator always evaluates both expressions, which could include making procedure calls.</span></span> <span data-ttu-id="e2a4c-122">Il n’existe aucun équivalent court-circuit `Xor`, car le résultat dépend toujours des deux opérandes.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-122">There is no short-circuiting counterpart to `Xor`, because the result always depends on both operands.</span></span> <span data-ttu-id="e2a4c-123">Pour *court-circuit* des opérateurs logiques, consultez [opérateur AndAlso](../../../visual-basic/language-reference/operators/andalso-operator.md) et [OrElse Operator](../../../visual-basic/language-reference/operators/orelse-operator.md).</span><span class="sxs-lookup"><span data-stu-id="e2a4c-123">For *short-circuiting* logical operators, see [AndAlso Operator](../../../visual-basic/language-reference/operators/andalso-operator.md) and [OrElse Operator](../../../visual-basic/language-reference/operators/orelse-operator.md).</span></span>  
  
 <span data-ttu-id="e2a4c-124">Pour les opérations au niveau du bit, les `Xor` opérateur effectue une comparaison au niveau du bit de position identique dans deux expressions numériques et définit le bit dans correspondant `result` conformément au tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-124">For bitwise operations, the `Xor` operator performs a bitwise comparison of identically positioned bits in two numeric expressions and sets the corresponding bit in `result` according to the following table.</span></span>  
  
|<span data-ttu-id="e2a4c-125">Si de transmission en `expression1` est</span><span class="sxs-lookup"><span data-stu-id="e2a4c-125">If bit in `expression1` is</span></span>|<span data-ttu-id="e2a4c-126">Et que le bit dans `expression2` est</span><span class="sxs-lookup"><span data-stu-id="e2a4c-126">And bit in `expression2` is</span></span>|<span data-ttu-id="e2a4c-127">Le bit `result` est</span><span class="sxs-lookup"><span data-stu-id="e2a4c-127">The bit in `result` is</span></span>|  
|--------------------------------|---------------------------------|----------------------------|  
|<span data-ttu-id="e2a4c-128">1</span><span class="sxs-lookup"><span data-stu-id="e2a4c-128">1</span></span>|<span data-ttu-id="e2a4c-129">1</span><span class="sxs-lookup"><span data-stu-id="e2a4c-129">1</span></span>|<span data-ttu-id="e2a4c-130">0</span><span class="sxs-lookup"><span data-stu-id="e2a4c-130">0</span></span>|  
|<span data-ttu-id="e2a4c-131">1</span><span class="sxs-lookup"><span data-stu-id="e2a4c-131">1</span></span>|<span data-ttu-id="e2a4c-132">0</span><span class="sxs-lookup"><span data-stu-id="e2a4c-132">0</span></span>|<span data-ttu-id="e2a4c-133">1</span><span class="sxs-lookup"><span data-stu-id="e2a4c-133">1</span></span>|  
|<span data-ttu-id="e2a4c-134">0</span><span class="sxs-lookup"><span data-stu-id="e2a4c-134">0</span></span>|<span data-ttu-id="e2a4c-135">1</span><span class="sxs-lookup"><span data-stu-id="e2a4c-135">1</span></span>|<span data-ttu-id="e2a4c-136">1</span><span class="sxs-lookup"><span data-stu-id="e2a4c-136">1</span></span>|  
|<span data-ttu-id="e2a4c-137">0</span><span class="sxs-lookup"><span data-stu-id="e2a4c-137">0</span></span>|<span data-ttu-id="e2a4c-138">0</span><span class="sxs-lookup"><span data-stu-id="e2a4c-138">0</span></span>|<span data-ttu-id="e2a4c-139">0</span><span class="sxs-lookup"><span data-stu-id="e2a4c-139">0</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="e2a4c-140">Étant donné que les opérateurs logiques et au niveau du bit ont une priorité inférieure à celle des opérateurs arithmétiques et relationnels, toutes les opérations au niveau du bit doivent être mises entre parenthèses pour garantir une exécution précise.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-140">Since the logical and bitwise operators have a lower precedence than other arithmetic and relational operators, any bitwise operations should be enclosed in parentheses to ensure accurate execution.</span></span>  
  
 <span data-ttu-id="e2a4c-141">Par exemple, 5 `Xor` 3 est 6.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-141">For example, 5 `Xor` 3 is 6.</span></span> <span data-ttu-id="e2a4c-142">Pour voir pourquoi il s’agit, convertissez 5 et 3 en leurs représentations sous forme binaire, 101 et 011.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-142">To see why this is so, convert 5 and 3 to their binary representations, 101 and 011.</span></span> <span data-ttu-id="e2a4c-143">Puis utilisez le tableau précédent pour déterminer que 101 Xor 011 est 110, ce qui est la représentation binaire du nombre décimal 6.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-143">Then use the previous table to determine that 101 Xor 011 is 110, which is the binary representation of the decimal number 6.</span></span>  
  
## <a name="data-types"></a><span data-ttu-id="e2a4c-144">Types de données</span><span class="sxs-lookup"><span data-stu-id="e2a4c-144">Data Types</span></span>  
 <span data-ttu-id="e2a4c-145">Si les opérandes se composent d’une `Boolean` expression et une expression numérique, Visual Basic convertit le `Boolean` expression à une valeur numérique (-1 pour `True` et 0 pour `False`) et effectue une opération au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-145">If the operands consist of one `Boolean` expression and one numeric expression, Visual Basic converts the `Boolean` expression to a numeric value (–1 for `True` and 0 for `False`) and performs a bitwise operation.</span></span>  
  
 <span data-ttu-id="e2a4c-146">Pour un `Boolean` comparaison, le type de données du résultat est `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-146">For a `Boolean` comparison, the data type of the result is `Boolean`.</span></span> <span data-ttu-id="e2a4c-147">Pour obtenir une comparaison au niveau du bit, le type de données de résultat est un type numérique approprié pour les types de données de `expression1` et `expression2`.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-147">For a bitwise comparison, the result data type is a numeric type appropriate for the data types of `expression1` and `expression2`.</span></span> <span data-ttu-id="e2a4c-148">Consultez le tableau « Relationnelles et au niveau du bit des comparaisons » dans [Types de données de résultats de l’opérateur](../../../visual-basic/language-reference/operators/data-types-of-operator-results.md).</span><span class="sxs-lookup"><span data-stu-id="e2a4c-148">See the "Relational and Bitwise Comparisons" table in [Data Types of Operator Results](../../../visual-basic/language-reference/operators/data-types-of-operator-results.md).</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="e2a4c-149">Surcharge</span><span class="sxs-lookup"><span data-stu-id="e2a4c-149">Overloading</span></span>  
 <span data-ttu-id="e2a4c-150">Le `Xor` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-150">The `Xor` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="e2a4c-151">Si votre code utilise cet opérateur sur une telle classe ou structure, assurez-vous que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-151">If your code uses this operator on such a class or structure, make sure you understand its redefined behavior.</span></span> <span data-ttu-id="e2a4c-152">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="e2a4c-152">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="e2a4c-153">Exemple</span><span class="sxs-lookup"><span data-stu-id="e2a4c-153">Example</span></span>  
 <span data-ttu-id="e2a4c-154">L’exemple suivant utilise le `Xor` opérateur pour effectuer une exclusion logique (disjonction logique exclusive) sur deux expressions.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-154">The following example uses the `Xor` operator to perform logical exclusion (exclusive logical disjunction) on two expressions.</span></span> <span data-ttu-id="e2a4c-155">Le résultat est un `Boolean` valeur qui indique si une des expressions exactement est `True`.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-155">The result is a `Boolean` value that represents whether exactly one of the expressions is `True`.</span></span>  
  
 [!code-vb[VbVbalrOperators#40](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#40)]  
  
 <span data-ttu-id="e2a4c-156">L’exemple précédent produit des résultats de `False`, `True`, et `False`, respectivement.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-156">The previous example produces results of `False`, `True`, and `False`, respectively.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e2a4c-157">Exemple</span><span class="sxs-lookup"><span data-stu-id="e2a4c-157">Example</span></span>  
 <span data-ttu-id="e2a4c-158">L’exemple suivant utilise le `Xor` opérateur pour effectuer une exclusion logique (disjonction logique exclusive) sur les bits individuels de deux expressions numériques.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-158">The following example uses the `Xor` operator to perform logical exclusion (exclusive logical disjunction) on the individual bits of two numeric expressions.</span></span> <span data-ttu-id="e2a4c-159">Le bit du modèle de résultat est défini si un seul des bits correspondants dans les opérandes est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-159">The bit in the result pattern is set if exactly one of the corresponding bits in the operands is set to 1.</span></span>  
  
 [!code-vb[VbVbalrOperators#41](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#41)]  
  
 <span data-ttu-id="e2a4c-160">L’exemple précédent produit les résultats de 2, 12 et 14, respectivement.</span><span class="sxs-lookup"><span data-stu-id="e2a4c-160">The previous example produces results of 2, 12, and 14, respectively.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2a4c-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2a4c-161">See also</span></span>

- [<span data-ttu-id="e2a4c-162">Opérateurs logiques/de bits (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e2a4c-162">Logical/Bitwise Operators (Visual Basic)</span></span>](../../../visual-basic/language-reference/operators/logical-bitwise-operators.md)
- [<span data-ttu-id="e2a4c-163">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e2a4c-163">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="e2a4c-164">Opérateurs répertoriés par fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="e2a4c-164">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="e2a4c-165">Opérateurs logiques et au niveau du bit en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e2a4c-165">Logical and Bitwise Operators in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
