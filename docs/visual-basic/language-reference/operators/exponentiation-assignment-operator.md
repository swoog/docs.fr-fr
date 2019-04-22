---
title: ^=, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.^=
helpviewer_keywords:
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- ^= operator [Visual Basic]
- compound assignment statements [Visual Basic]
ms.assetid: 397da132-2d96-4a85-a7bc-f7c730a608c9
ms.openlocfilehash: fe5d7b3dcb55192167512e0934e09cff7dfddb6d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58819648"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="d24c2-102">^=, opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d24c2-102">^= Operator (Visual Basic)</span></span>
<span data-ttu-id="d24c2-103">Élève la valeur d’une variable ou une propriété à la puissance d’une expression et assigne le résultat à la variable ou propriété.</span><span class="sxs-lookup"><span data-stu-id="d24c2-103">Raises the value of a variable or property to the power of an expression and assigns the result back to the variable or property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d24c2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d24c2-104">Syntax</span></span>  
  
```  
variableorproperty ^= expression  
```  
  
## <a name="parts"></a><span data-ttu-id="d24c2-105">Composants</span><span class="sxs-lookup"><span data-stu-id="d24c2-105">Parts</span></span>  
 `variableorproperty`  
 <span data-ttu-id="d24c2-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d24c2-106">Required.</span></span> <span data-ttu-id="d24c2-107">Toute variable ou propriété numérique.</span><span class="sxs-lookup"><span data-stu-id="d24c2-107">Any numeric variable or property.</span></span>  
  
 `expression`  
 <span data-ttu-id="d24c2-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d24c2-108">Required.</span></span> <span data-ttu-id="d24c2-109">Toute expression numérique.</span><span class="sxs-lookup"><span data-stu-id="d24c2-109">Any numeric expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d24c2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d24c2-110">Remarks</span></span>  
 <span data-ttu-id="d24c2-111">L’élément sur le côté gauche de la `^=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="d24c2-111">The element on the left side of the `^=` operator can be a simple scalar variable, a property, or an element of an array.</span></span> <span data-ttu-id="d24c2-112">La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span><span class="sxs-lookup"><span data-stu-id="d24c2-112">The variable or property cannot be [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span></span>  
  
 <span data-ttu-id="d24c2-113">Le `^=` opérateur déclenche tout d’abord la valeur de la variable ou une propriété (sur le côté gauche de l’opérateur) à la puissance de la valeur de l’expression (sur le côté droit de l’opérateur).</span><span class="sxs-lookup"><span data-stu-id="d24c2-113">The `^=` operator first raises the value of the variable or property (on the left-hand side of the operator) to the power of the value of the expression (on the right-hand side of the operator).</span></span> <span data-ttu-id="d24c2-114">Puis, l’opérateur assigne le résultat de cette opération à la variable ou propriété.</span><span class="sxs-lookup"><span data-stu-id="d24c2-114">The operator then assigns the result of that operation back to the variable or property.</span></span>  
  
 <span data-ttu-id="d24c2-115">Visual Basic exécute toujours l’élévation à la puissance dans le [Type de données Double](../../../visual-basic/language-reference/data-types/double-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d24c2-115">Visual Basic always performs exponentiation in the [Double Data Type](../../../visual-basic/language-reference/data-types/double-data-type.md).</span></span> <span data-ttu-id="d24c2-116">Opérandes de tous types sont convertis en `Double`, et le résultat est toujours `Double`.</span><span class="sxs-lookup"><span data-stu-id="d24c2-116">Operands of any different type are converted to `Double`, and the result is always `Double`.</span></span>  
  
 <span data-ttu-id="d24c2-117">La valeur de `expression` peut être fractionnaire, négative ou les deux.</span><span class="sxs-lookup"><span data-stu-id="d24c2-117">The value of `expression` can be fractional, negative, or both.</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="d24c2-118">Surcharge</span><span class="sxs-lookup"><span data-stu-id="d24c2-118">Overloading</span></span>  
 <span data-ttu-id="d24c2-119">Le [^ opérateur](../../../visual-basic/language-reference/operators/exponentiation-operator.md) peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="d24c2-119">The [^ Operator](../../../visual-basic/language-reference/operators/exponentiation-operator.md) can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="d24c2-120">La surcharge la `^` opérateur affecte le comportement de la `^=` opérateur.</span><span class="sxs-lookup"><span data-stu-id="d24c2-120">Overloading the `^` operator affects the behavior of the `^=` operator.</span></span> <span data-ttu-id="d24c2-121">Si votre code utilise `^=` sur une classe ou structure qui surcharge `^`, assurez-vous que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="d24c2-121">If your code uses `^=` on a class or structure that overloads `^`, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="d24c2-122">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="d24c2-122">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d24c2-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="d24c2-123">Example</span></span>  
 <span data-ttu-id="d24c2-124">L’exemple suivant utilise le `^=` opérateur pour déclencher la valeur d’un `Integer` variable à la puissance d’une deuxième variable et assigner le résultat à la première variable.</span><span class="sxs-lookup"><span data-stu-id="d24c2-124">The following example uses the `^=` operator to raise the value of one `Integer` variable to the power of a second variable and assign the result to the first variable.</span></span>  
  
 [!code-vb[VbVbalrOperators#21](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#21)]  
  
## <a name="see-also"></a><span data-ttu-id="d24c2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d24c2-125">See also</span></span>

- [<span data-ttu-id="d24c2-126">^ (opérateur)</span><span class="sxs-lookup"><span data-stu-id="d24c2-126">^ Operator</span></span>](../../../visual-basic/language-reference/operators/exponentiation-operator.md)
- [<span data-ttu-id="d24c2-127">Opérateurs d’assignation</span><span class="sxs-lookup"><span data-stu-id="d24c2-127">Assignment Operators</span></span>](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [<span data-ttu-id="d24c2-128">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="d24c2-128">Arithmetic Operators</span></span>](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [<span data-ttu-id="d24c2-129">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d24c2-129">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="d24c2-130">Opérateurs répertoriés par fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="d24c2-130">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="d24c2-131">Instructions</span><span class="sxs-lookup"><span data-stu-id="d24c2-131">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
