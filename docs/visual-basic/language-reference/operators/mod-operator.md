---
title: Mod, opérateur (Visual Basic)
ms.date: 04/24/2018
f1_keywords:
- vb.Mod
helpviewer_keywords:
- remainder (Mod operator)
- division operator [Visual Basic], Mod operator
- modulus operator [Visual Basic], Visual Basic
- Mod operator [Visual Basic]
- operators [Visual Basic], division
- arithmetic operators [Visual Basic], Mod
- math operators [Visual Basic]
ms.assetid: 6ff7e40e-cec8-4c77-bff6-8ddd2791c25b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 456c19fc8e28517a0662b58e338028e1c75cd8c8
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2018
ms.locfileid: "45585862"
---
# <a name="mod-operator-visual-basic"></a><span data-ttu-id="c7811-102">Mod, opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c7811-102">Mod operator (Visual Basic)</span></span>
<span data-ttu-id="c7811-103">Divise deux nombres et retourne uniquement le reste.</span><span class="sxs-lookup"><span data-stu-id="c7811-103">Divides two numbers and returns only the remainder.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7811-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7811-104">Syntax</span></span>  
  
```  
number1 Mod number2  
```  
  
## <a name="parts"></a><span data-ttu-id="c7811-105">Composants</span><span class="sxs-lookup"><span data-stu-id="c7811-105">Parts</span></span>  
 `number1`  
 <span data-ttu-id="c7811-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c7811-106">Required.</span></span> <span data-ttu-id="c7811-107">Toute expression numérique.</span><span class="sxs-lookup"><span data-stu-id="c7811-107">Any numeric expression.</span></span>  
  
 `number2`  
 <span data-ttu-id="c7811-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c7811-108">Required.</span></span> <span data-ttu-id="c7811-109">Toute expression numérique.</span><span class="sxs-lookup"><span data-stu-id="c7811-109">Any numeric expression.</span></span>  
  
## <a name="supported-types"></a><span data-ttu-id="c7811-110">Types pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7811-110">Supported types</span></span>  
 <span data-ttu-id="c7811-111">Tous les types numériques.</span><span class="sxs-lookup"><span data-stu-id="c7811-111">All numeric types.</span></span> <span data-ttu-id="c7811-112">Cela inclut les types non signés et à virgule flottante et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="c7811-112">This includes the unsigned and floating-point types and `Decimal`.</span></span>  
  
## <a name="result"></a><span data-ttu-id="c7811-113">Résultat</span><span class="sxs-lookup"><span data-stu-id="c7811-113">Result</span></span>

<span data-ttu-id="c7811-114">Le résultat est le reste après `number1` est divisé par `number2`.</span><span class="sxs-lookup"><span data-stu-id="c7811-114">The result is the remainder after `number1` is divided by `number2`.</span></span> <span data-ttu-id="c7811-115">Par exemple, l’expression `14 Mod 4` renvoie la valeur 2.</span><span class="sxs-lookup"><span data-stu-id="c7811-115">For example, the expression `14 Mod 4` evaluates to 2.</span></span>  

> [!NOTE]
> <span data-ttu-id="c7811-116">Il existe une différence entre *reste* et *modulo* en mathématiques, avec des résultats différents pour les nombres négatifs.</span><span class="sxs-lookup"><span data-stu-id="c7811-116">There is a difference between *remainder* and *modulus* in mathematics, with different results for negative numbers.</span></span> <span data-ttu-id="c7811-117">Le `Mod` opérateur en Visual Basic, le .NET Framework `op_Modulus` opérateur et sous-jacent [rem](<xref:System.Reflection.Emit.OpCodes.Rem>) instruction IL tous effectuer une opération de reste.</span><span class="sxs-lookup"><span data-stu-id="c7811-117">The `Mod` operator in Visual Basic, the .NET Framework `op_Modulus` operator, and the underlying [rem](<xref:System.Reflection.Emit.OpCodes.Rem>) IL instruction all perform a remainder operation.</span></span>

<span data-ttu-id="c7811-118">Le résultat d’une `Mod` opération conserve le signe du dividende, `number1`, et par conséquent, il peut être positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="c7811-118">The result of a `Mod` operation retains the sign of the dividend, `number1`, and so it may be positive or negative.</span></span> <span data-ttu-id="c7811-119">Le résultat est toujours dans la plage (-`number2`, `number2`), de manière exclusive.</span><span class="sxs-lookup"><span data-stu-id="c7811-119">The result is always in the range (-`number2`, `number2`), exclusive.</span></span> <span data-ttu-id="c7811-120">Exemple :</span><span class="sxs-lookup"><span data-stu-id="c7811-120">For example:</span></span>

```vb
Public Module Example
   Public Sub Main()
      Console.WriteLine($" 8 Mod  3 = {8 Mod 3}")
      Console.WriteLine($"-8 Mod  3 = {-8 Mod 3}")
      Console.WriteLine($" 8 Mod -3 = {8 Mod -3}")
      Console.WriteLine($"-8 Mod -3 = {-8 Mod -3}")
   End Sub
End Module
' The example displays the following output:
'       8 Mod  3 = 2
'      -8 Mod  3 = -2
'       8 Mod -3 = 2
'      -8 Mod -3 = -2
```

## <a name="remarks"></a><span data-ttu-id="c7811-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c7811-121">Remarks</span></span>  
 <span data-ttu-id="c7811-122">Si `number1` ou `number2` est une valeur à virgule flottante, le reste de la division à virgule flottante est retourné.</span><span class="sxs-lookup"><span data-stu-id="c7811-122">If either `number1` or `number2` is a floating-point value, the floating-point remainder of the division is returned.</span></span> <span data-ttu-id="c7811-123">Le type de données du résultat est le plus petit type de données qui peut contenir toutes les valeurs possibles qui résultent de la division avec les types de données de `number1` et `number2`.</span><span class="sxs-lookup"><span data-stu-id="c7811-123">The data type of the result is the smallest data type that can hold all possible values that result from division with the data types of `number1` and `number2`.</span></span>  
  
 <span data-ttu-id="c7811-124">Si `number1` ou `number2` prend la valeur [rien](../../../visual-basic/language-reference/nothing.md), il est considéré comme égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c7811-124">If `number1` or `number2` evaluates to [Nothing](../../../visual-basic/language-reference/nothing.md), it is treated as zero.</span></span>  
  
 <span data-ttu-id="c7811-125">Les opérateurs connexes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c7811-125">Related operators include the following:</span></span>  
  
-   <span data-ttu-id="c7811-126">Le [\, opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/integer-division-operator.md) renvoie le quotient entier d’une division.</span><span class="sxs-lookup"><span data-stu-id="c7811-126">The [\ Operator (Visual Basic)](../../../visual-basic/language-reference/operators/integer-division-operator.md) returns the integer quotient of a division.</span></span> <span data-ttu-id="c7811-127">Par exemple, l’expression `14 \ 4` prend la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="c7811-127">For example, the expression `14 \ 4` evaluates to 3.</span></span>  
  
-   <span data-ttu-id="c7811-128">Le [/, opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/floating-point-division-operator.md) retourne le quotient complet, y compris le reste, comme un nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="c7811-128">The [/ Operator (Visual Basic)](../../../visual-basic/language-reference/operators/floating-point-division-operator.md) returns the full quotient, including the remainder, as a floating-point number.</span></span> <span data-ttu-id="c7811-129">Par exemple, l’expression `14 / 4` prend la valeur 3.5.</span><span class="sxs-lookup"><span data-stu-id="c7811-129">For example, the expression `14 / 4` evaluates to 3.5.</span></span>  
  
## <a name="attempted-division-by-zero"></a><span data-ttu-id="c7811-130">Tentative de division par zéro</span><span class="sxs-lookup"><span data-stu-id="c7811-130">Attempted division by zero</span></span>  
 <span data-ttu-id="c7811-131">Si `number2` prend la valeur zéro, le comportement de la `Mod` opérateur varie selon le type de données des opérandes.</span><span class="sxs-lookup"><span data-stu-id="c7811-131">If `number2` evaluates to zero, the behavior of the `Mod` operator depends on the data type of the operands.</span></span> <span data-ttu-id="c7811-132">Une division intégrale lève un <xref:System.DivideByZeroException> exception.</span><span class="sxs-lookup"><span data-stu-id="c7811-132">An integral division throws a <xref:System.DivideByZeroException> exception.</span></span> <span data-ttu-id="c7811-133">Retourne une division à virgule flottante <xref:System.Double.NaN>.</span><span class="sxs-lookup"><span data-stu-id="c7811-133">A floating-point division returns <xref:System.Double.NaN>.</span></span>  
  
## <a name="equivalent-formula"></a><span data-ttu-id="c7811-134">Formule équivalente</span><span class="sxs-lookup"><span data-stu-id="c7811-134">Equivalent formula</span></span>  
 <span data-ttu-id="c7811-135">L’expression `a Mod b` correspond à une des formules suivantes :</span><span class="sxs-lookup"><span data-stu-id="c7811-135">The expression `a Mod b` is equivalent to either of the following formulas:</span></span>  
  
 `a - (b * (a \ b))`  
  
 `a - (b * Fix(a / b))`  
  
## <a name="floating-point-imprecision"></a><span data-ttu-id="c7811-136">À virgule flottante imprécision</span><span class="sxs-lookup"><span data-stu-id="c7811-136">Floating-point imprecision</span></span>  
 <span data-ttu-id="c7811-137">Lorsque vous travaillez avec des nombres à virgule flottante, n’oubliez pas qu’ils n’ont pas toujours de représentation décimale précise dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="c7811-137">When you work with floating-point numbers, remember that they do not always have a precise decimal representation in memory.</span></span> <span data-ttu-id="c7811-138">Cela peut entraîner des résultats inattendus à partir de certaines opérations, comme la comparaison de valeurs et les `Mod` opérateur.</span><span class="sxs-lookup"><span data-stu-id="c7811-138">This can lead to unexpected results from certain operations, such as value comparison and the `Mod` operator.</span></span> <span data-ttu-id="c7811-139">Pour plus d’informations, consultez [dépannage des Types de données](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="c7811-139">For more information, see [Troubleshooting Data Types](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md).</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="c7811-140">Surcharge</span><span class="sxs-lookup"><span data-stu-id="c7811-140">Overloading</span></span>  
 <span data-ttu-id="c7811-141">Le `Mod` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement.</span><span class="sxs-lookup"><span data-stu-id="c7811-141">The `Mod` operator can be *overloaded*, which means that a class or structure can redefine its behavior.</span></span> <span data-ttu-id="c7811-142">Si votre code s’applique `Mod` à une instance d’une classe ou une structure qui inclut une telle surcharge, assurez-vous que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="c7811-142">If your code applies `Mod` to an instance of a class or structure that includes such an overload, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="c7811-143">Pour plus d’informations, consultez [procédures d’opérateur](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="c7811-143">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="c7811-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="c7811-144">Example</span></span>  
 <span data-ttu-id="c7811-145">L’exemple suivant utilise le `Mod` opérateur diviser deux nombres et retourner uniquement le reste.</span><span class="sxs-lookup"><span data-stu-id="c7811-145">The following example uses the `Mod` operator to divide two numbers and return only the remainder.</span></span> <span data-ttu-id="c7811-146">Si des nombres sont un nombre à virgule flottante, le résultat est un nombre à virgule flottante qui représente le reste.</span><span class="sxs-lookup"><span data-stu-id="c7811-146">If either number is a floating-point number, the result is a floating-point number that represents the remainder.</span></span>  
  
 [!code-vb[VbVbalrOperators#31](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/mod-operator_1.vb)]  
  
## <a name="example"></a><span data-ttu-id="c7811-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="c7811-147">Example</span></span>  
 <span data-ttu-id="c7811-148">L’exemple suivant montre l’imprécision potentielle des opérandes à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="c7811-148">The following example demonstrates the potential imprecision of floating-point operands.</span></span> <span data-ttu-id="c7811-149">Dans la première instruction, les opérandes sont `Double`, et 0,2 représente une fraction binaire se répétant avec une valeur stockée de 0,20000000000000001.</span><span class="sxs-lookup"><span data-stu-id="c7811-149">In the first statement, the operands are `Double`, and 0.2 is an infinitely repeating binary fraction with a stored value of 0.20000000000000001.</span></span> <span data-ttu-id="c7811-150">Dans la deuxième instruction, le littéral de type caractère `D` force les deux opérandes de `Decimal`, et 0,2 a une représentation précise.</span><span class="sxs-lookup"><span data-stu-id="c7811-150">In the second statement, the literal type character `D` forces both operands to `Decimal`, and 0.2 has a precise representation.</span></span>  
  
 [!code-vb[VbVbalrOperators#32](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/mod-operator_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="c7811-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7811-151">See also</span></span>  
 <xref:Microsoft.VisualBasic.Conversion.Int%2A>  
 <xref:Microsoft.VisualBasic.Conversion.Fix%2A>  
 [<span data-ttu-id="c7811-152">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="c7811-152">Arithmetic Operators</span></span>](../../../visual-basic/language-reference/operators/arithmetic-operators.md)  
 [<span data-ttu-id="c7811-153">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c7811-153">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)  
 [<span data-ttu-id="c7811-154">Opérateurs répertoriés par fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="c7811-154">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)  
 [<span data-ttu-id="c7811-155">Dépannage des types de données</span><span class="sxs-lookup"><span data-stu-id="c7811-155">Troubleshooting Data Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)  
 [<span data-ttu-id="c7811-156">Opérateurs arithmétiques en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c7811-156">Arithmetic Operators in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)  
 [<span data-ttu-id="c7811-157">\, Opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c7811-157">\ Operator (Visual Basic)</span></span>](../../../visual-basic/language-reference/operators/integer-division-operator.md)
