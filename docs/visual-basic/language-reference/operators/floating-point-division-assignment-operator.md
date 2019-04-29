---
title: /=, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb./=
helpviewer_keywords:
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- /= operator [Visual Basic]
- operator /=
- compound assignment statements [Visual Basic]
ms.assetid: a1e22d0e-8380-4761-9da1-84fb51c34821
ms.openlocfilehash: d9d3fa021654d3be1b9d304beb83caa737660264
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778467"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="957d9-102">/=, opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="957d9-102">/= Operator (Visual Basic)</span></span>
<span data-ttu-id="957d9-103">Divise la valeur d’une variable ou une propriété par la valeur d’une expression et assigne le résultat à virgule flottante à la variable ou propriété.</span><span class="sxs-lookup"><span data-stu-id="957d9-103">Divides the value of a variable or property by the value of an expression and assigns the floating-point result to the variable or property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="957d9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="957d9-104">Syntax</span></span>  
  
```  
variableorproperty /= expression  
```  
  
## <a name="parts"></a><span data-ttu-id="957d9-105">Composants</span><span class="sxs-lookup"><span data-stu-id="957d9-105">Parts</span></span>  
 `variableorproperty`  
 <span data-ttu-id="957d9-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="957d9-106">Required.</span></span> <span data-ttu-id="957d9-107">Toute variable ou propriété numérique.</span><span class="sxs-lookup"><span data-stu-id="957d9-107">Any numeric variable or property.</span></span>  
  
 `expression`  
 <span data-ttu-id="957d9-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="957d9-108">Required.</span></span> <span data-ttu-id="957d9-109">Toute expression numérique.</span><span class="sxs-lookup"><span data-stu-id="957d9-109">Any numeric expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="957d9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="957d9-110">Remarks</span></span>  
 <span data-ttu-id="957d9-111">L’élément sur le côté gauche de la `/=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="957d9-111">The element on the left side of the `/=` operator can be a simple scalar variable, a property, or an element of an array.</span></span> <span data-ttu-id="957d9-112">La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span><span class="sxs-lookup"><span data-stu-id="957d9-112">The variable or property cannot be [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span></span>  
  
 <span data-ttu-id="957d9-113">Le `/=` opérateur divise tout d’abord la valeur de la variable ou une propriété (sur le côté gauche de l’opérateur) par la valeur de l’expression (sur le côté droit de l’opérateur).</span><span class="sxs-lookup"><span data-stu-id="957d9-113">The `/=` operator first divides the value of the variable or property (on the left-hand side of the operator) by the value of the expression (on the right-hand side of the operator).</span></span> <span data-ttu-id="957d9-114">L’opérateur assigne ensuite le résultat à virgule flottante de cette opération à la variable ou la propriété.</span><span class="sxs-lookup"><span data-stu-id="957d9-114">The operator then assigns the floating-point result of that operation to the variable or property.</span></span>  
  
 <span data-ttu-id="957d9-115">Cette instruction assigne un `Double` valeur à la variable ou une propriété sur la gauche.</span><span class="sxs-lookup"><span data-stu-id="957d9-115">This statement assigns a `Double` value to the variable or property on the left.</span></span> <span data-ttu-id="957d9-116">Si `Option Strict` est `On`, `variableorproperty` doit être un `Double`.</span><span class="sxs-lookup"><span data-stu-id="957d9-116">If `Option Strict` is `On`, `variableorproperty` must be a `Double`.</span></span> <span data-ttu-id="957d9-117">Si `Option Strict` est `Off`, Visual Basic exécute une conversion implicite et assigne la valeur obtenue vers `variableorproperty`, avec une erreur possible au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="957d9-117">If `Option Strict` is `Off`, Visual Basic performs an implicit conversion and assigns the resulting value to `variableorproperty`, with a possible error at run time.</span></span> <span data-ttu-id="957d9-118">Pour plus d’informations, consultez [Widening and Narrowing Conversions](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md) et [Option Strict, instruction](../../../visual-basic/language-reference/statements/option-strict-statement.md).</span><span class="sxs-lookup"><span data-stu-id="957d9-118">For more information, see [Widening and Narrowing Conversions](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md) and [Option Strict Statement](../../../visual-basic/language-reference/statements/option-strict-statement.md).</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="957d9-119">Surcharge</span><span class="sxs-lookup"><span data-stu-id="957d9-119">Overloading</span></span>  
 <span data-ttu-id="957d9-120">Le [/, opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/floating-point-division-operator.md) peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="957d9-120">The [/ Operator (Visual Basic)](../../../visual-basic/language-reference/operators/floating-point-division-operator.md) can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="957d9-121">La surcharge la `/` opérateur affecte le comportement de la `/=` opérateur.</span><span class="sxs-lookup"><span data-stu-id="957d9-121">Overloading the `/` operator affects the behavior of the `/=` operator.</span></span> <span data-ttu-id="957d9-122">Si votre code utilise `/=` sur une classe ou structure qui surcharge `/`, assurez-vous que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="957d9-122">If your code uses `/=` on a class or structure that overloads `/`, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="957d9-123">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="957d9-123">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="957d9-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="957d9-124">Example</span></span>  
 <span data-ttu-id="957d9-125">L’exemple suivant utilise le `/=` opérateur pour diviser une `Integer` variable par une autre et assigner le quotient à la première variable.</span><span class="sxs-lookup"><span data-stu-id="957d9-125">The following example uses the `/=` operator to divide one `Integer` variable by a second and assign the quotient to the first variable.</span></span>  
  
 [!code-vb[VbVbalrOperators#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#17)]  
  
## <a name="see-also"></a><span data-ttu-id="957d9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="957d9-126">See also</span></span>

- [<span data-ttu-id="957d9-127">/, Opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="957d9-127">/ Operator (Visual Basic)</span></span>](../../../visual-basic/language-reference/operators/floating-point-division-operator.md)
- [<span data-ttu-id="957d9-128">\\=, Opérateur</span><span class="sxs-lookup"><span data-stu-id="957d9-128">\\= Operator</span></span>](../../../visual-basic/language-reference/operators/integer-division-assignment-operator.md)
- [<span data-ttu-id="957d9-129">Opérateurs d’assignation</span><span class="sxs-lookup"><span data-stu-id="957d9-129">Assignment Operators</span></span>](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [<span data-ttu-id="957d9-130">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="957d9-130">Arithmetic Operators</span></span>](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [<span data-ttu-id="957d9-131">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="957d9-131">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="957d9-132">Opérateurs répertoriés par fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="957d9-132">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="957d9-133">Instructions</span><span class="sxs-lookup"><span data-stu-id="957d9-133">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
