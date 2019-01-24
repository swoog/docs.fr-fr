---
title: Comparaisons de valeurs (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], comparing values
- Visual Basic code, operators
- Visual Basic code, expressions
- comparison operators [Visual Basic], comparing expressions
- numeric expressions
- operators [Visual Basic], comparison
- expressions [Visual Basic], comparing
ms.assetid: 60da0c76-9458-4afc-97e9-44a7939c064c
ms.openlocfilehash: 23733741a79506730187d5735a20f3848e43da1d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54724812"
---
# <a name="value-comparisons-visual-basic"></a><span data-ttu-id="639e1-102">Comparaisons de valeurs (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="639e1-102">Value Comparisons (Visual Basic)</span></span>
<span data-ttu-id="639e1-103">Opérateurs de comparaison peuvent être utilisés pour construire des expressions qui comparent les valeurs de variables numériques.</span><span class="sxs-lookup"><span data-stu-id="639e1-103">Comparison operators can be used to construct expressions that compare the values of numeric variables.</span></span> <span data-ttu-id="639e1-104">Ces expressions retournent un `Boolean` valeur selon que la comparaison est true ou false.</span><span class="sxs-lookup"><span data-stu-id="639e1-104">These expressions return a `Boolean` value based on whether the comparison is true or false.</span></span> <span data-ttu-id="639e1-105">Voici quelques exemples de ce type d’expression.</span><span class="sxs-lookup"><span data-stu-id="639e1-105">Examples of such an expression are as follows.</span></span>  
  
 `45 > 26`  
  
 `26 > 45`  
  
 <span data-ttu-id="639e1-106">La première expression prend la valeur `True`, car 45 est supérieur à 26.</span><span class="sxs-lookup"><span data-stu-id="639e1-106">The first expression evaluates to `True`, because 45 is greater than 26.</span></span> <span data-ttu-id="639e1-107">Le deuxième exemple prend la valeur `False`, car 26 n’est pas supérieure à 45.</span><span class="sxs-lookup"><span data-stu-id="639e1-107">The second example evaluates to `False`, because 26 is not greater than 45.</span></span>  
  
 <span data-ttu-id="639e1-108">Vous pouvez également comparer des expressions numériques de cette façon.</span><span class="sxs-lookup"><span data-stu-id="639e1-108">You can also compare numeric expressions in this fashion.</span></span> <span data-ttu-id="639e1-109">Les expressions que vous comparez peuvent être des expressions complexes, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="639e1-109">The expressions you compare can themselves be complex expressions, as in the following example.</span></span>  
  
 `x / 45 * (y +17) >= System.Math.Sqrt(z) / (p - (x * 16))`  
  
 <span data-ttu-id="639e1-110">L’expression précédente complexe inclut des littéraux, des variables et des appels de fonction.</span><span class="sxs-lookup"><span data-stu-id="639e1-110">The preceding complex expression includes literals, variables, and function calls.</span></span> <span data-ttu-id="639e1-111">Les expressions des deux côtés de l’opérateur de comparaison sont évaluées et les valeurs résultantes sont ensuite comparés à l’aide de la `>=` opérateur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="639e1-111">The expressions on both sides of the comparison operator are evaluated, and the resulting values are then compared using the `>=` comparison operator.</span></span> <span data-ttu-id="639e1-112">Si la valeur de l’expression sur le côté gauche est supérieure ou égal à la valeur de l’expression de droite, l’ensemble de l’expression prend la valeur `True`; sinon, il renvoie la valeur `False`.</span><span class="sxs-lookup"><span data-stu-id="639e1-112">If the value of the expression on the left side is greater than or equal to the value of the expression on the right, the entire expression evaluates to `True`; otherwise, it evaluates to `False`.</span></span>  
  
 <span data-ttu-id="639e1-113">Les expressions qui comparent des valeurs sont couramment utilisées dans `If...Then` constructions, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="639e1-113">Expressions that compare values are most commonly used in `If...Then` constructions, as in the following example.</span></span>  
  
 [!code-vb[VbVbalrOperators#84](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/value-comparisons_1.vb)]  
  
 <span data-ttu-id="639e1-114">Le `=` signe est un opérateur de comparaison ainsi que d’un opérateur d’assignation.</span><span class="sxs-lookup"><span data-stu-id="639e1-114">The `=` sign is a comparison operator as well as an assignment operator.</span></span> <span data-ttu-id="639e1-115">Lorsqu’il est utilisé comme un opérateur de comparaison, il évalue si la valeur sur la gauche est égale à la valeur à droite, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="639e1-115">When used as a comparison operator, it evaluates whether the value on the left is equal to the value on the right, as shown in the following example.</span></span>  
  
 [!code-vb[VbVbalrOperators#85](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/value-comparisons_2.vb)]  
  
 <span data-ttu-id="639e1-116">Vous pouvez également utiliser une expression de comparaison n’importe où un `Boolean` valeur est nécessaire, comme dans un `If`, `While`, `Loop`, ou `ElseIf` instruction, ou lors de l’assignation ou du passage d’une valeur à une `Boolean` variable.</span><span class="sxs-lookup"><span data-stu-id="639e1-116">You can also use a comparison expression anywhere a `Boolean` value is needed, such as in an `If`, `While`, `Loop`, or `ElseIf` statement, or when assigning to or passing a value to a `Boolean` variable.</span></span> <span data-ttu-id="639e1-117">Dans l’exemple suivant, la valeur retournée par l’expression de comparaison est assignée à un `Boolean` variable.</span><span class="sxs-lookup"><span data-stu-id="639e1-117">In the following example, the value returned by the comparison expression is assigned to a `Boolean` variable.</span></span>  
  
 [!code-vb[VbVbalrOperators#86](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/value-comparisons_3.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="639e1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="639e1-118">See also</span></span>
- [<span data-ttu-id="639e1-119">Expressions booléennes</span><span class="sxs-lookup"><span data-stu-id="639e1-119">Boolean Expressions</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/boolean-expressions.md)
- [<span data-ttu-id="639e1-120">Opérateurs et expressions</span><span class="sxs-lookup"><span data-stu-id="639e1-120">Operators and Expressions</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
- [<span data-ttu-id="639e1-121">Opérateurs de comparaison en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="639e1-121">Comparison Operators in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
- [<span data-ttu-id="639e1-122">Guide pratique pour Calculer des valeurs numériques</span><span class="sxs-lookup"><span data-stu-id="639e1-122">How to: Calculate Numeric Values</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/how-to-calculate-numeric-values.md)
- [<span data-ttu-id="639e1-123">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="639e1-123">Operator Precedence in Visual Basic</span></span>](../../../../visual-basic/language-reference/operators/operator-precedence.md)
