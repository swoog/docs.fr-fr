---
title: '*=, opérateur (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.*=
helpviewer_keywords:
- operator *=
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- '*= operator [Visual Basic]'
- compound assignment statements [Visual Basic]
ms.assetid: 96c86509-6eb8-4682-8226-3852e049376f
ms.openlocfilehash: d672ac147a4d7b2c21f4fcb7ee6cdf91b8b4924b
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56965330"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="c0916-102">\*=, opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c0916-102">\*= Operator (Visual Basic)</span></span>
<span data-ttu-id="c0916-103">Multiplie la valeur d’une variable ou une propriété par la valeur d’une expression et assigne le résultat à la variable ou propriété.</span><span class="sxs-lookup"><span data-stu-id="c0916-103">Multiplies the value of a variable or property by the value of an expression and assigns the result to the variable or property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0916-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0916-104">Syntax</span></span>  
  
```  
variableorproperty *= expression  
```  
  
## <a name="parts"></a><span data-ttu-id="c0916-105">Composants</span><span class="sxs-lookup"><span data-stu-id="c0916-105">Parts</span></span>  
 `variableorproperty`  
 <span data-ttu-id="c0916-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c0916-106">Required.</span></span> <span data-ttu-id="c0916-107">Toute variable ou propriété numérique.</span><span class="sxs-lookup"><span data-stu-id="c0916-107">Any numeric variable or property.</span></span>  
  
 `expression`  
 <span data-ttu-id="c0916-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c0916-108">Required.</span></span> <span data-ttu-id="c0916-109">Toute expression numérique.</span><span class="sxs-lookup"><span data-stu-id="c0916-109">Any numeric expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c0916-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c0916-110">Remarks</span></span>  
 <span data-ttu-id="c0916-111">L’élément sur le côté gauche de la `*=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="c0916-111">The element on the left side of the `*=` operator can be a simple scalar variable, a property, or an element of an array.</span></span> <span data-ttu-id="c0916-112">La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span><span class="sxs-lookup"><span data-stu-id="c0916-112">The variable or property cannot be [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span></span>  
  
 <span data-ttu-id="c0916-113">Le `*=` opérateur multiplie d’abord la valeur de l’expression (sur le côté droit de l’opérateur) par la valeur de la variable ou la propriété (sur le côté gauche de l’opérateur).</span><span class="sxs-lookup"><span data-stu-id="c0916-113">The `*=` operator first multiplies the value of the expression (on the right-hand side of the operator) by the value of the variable or property (on the left-hand side of the operator).</span></span> <span data-ttu-id="c0916-114">L’opérateur assigne ensuite le résultat de cette opération à la variable ou la propriété.</span><span class="sxs-lookup"><span data-stu-id="c0916-114">The operator then assigns the result of that operation to the variable or property.</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="c0916-115">Surcharge</span><span class="sxs-lookup"><span data-stu-id="c0916-115">Overloading</span></span>  
 <span data-ttu-id="c0916-116">Le [\* opérateur](../../../visual-basic/language-reference/operators/multiplication-operator.md) peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="c0916-116">The [\* Operator](../../../visual-basic/language-reference/operators/multiplication-operator.md) can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="c0916-117">La surcharge la `*` opérateur affecte le comportement de la `*=` opérateur.</span><span class="sxs-lookup"><span data-stu-id="c0916-117">Overloading the `*` operator affects the behavior of the `*=` operator.</span></span> <span data-ttu-id="c0916-118">Si votre code utilise `*=` sur une classe ou structure qui surcharge `*`, assurez-vous que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="c0916-118">If your code uses `*=` on a class or structure that overloads `*`, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="c0916-119">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="c0916-119">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="c0916-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="c0916-120">Example</span></span>  
 <span data-ttu-id="c0916-121">L’exemple suivant utilise le `*=` opérateur pour multiplier une `Integer` variable par une autre et assigner le résultat à la première variable.</span><span class="sxs-lookup"><span data-stu-id="c0916-121">The following example uses the `*=` operator to multiply one `Integer` variable by a second and assign the result to the first variable.</span></span>  
  
 [!code-vb[VbVbalrOperators#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#5)]  
  
## <a name="see-also"></a><span data-ttu-id="c0916-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0916-122">See also</span></span>
- [<span data-ttu-id="c0916-123">\* (opérateur)</span><span class="sxs-lookup"><span data-stu-id="c0916-123">\* Operator</span></span>](../../../visual-basic/language-reference/operators/multiplication-operator.md)
- [<span data-ttu-id="c0916-124">Opérateurs d’assignation</span><span class="sxs-lookup"><span data-stu-id="c0916-124">Assignment Operators</span></span>](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [<span data-ttu-id="c0916-125">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="c0916-125">Arithmetic Operators</span></span>](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [<span data-ttu-id="c0916-126">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c0916-126">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="c0916-127">Opérateurs répertoriés par fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="c0916-127">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="c0916-128">Instructions</span><span class="sxs-lookup"><span data-stu-id="c0916-128">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
