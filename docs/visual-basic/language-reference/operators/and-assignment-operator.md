---
title: '&amp;=, Opérateur (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.&=
helpviewer_keywords:
- operator &=
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- '&= operator [Visual Basic]'
- compound assignment statements [Visual Basic]
ms.assetid: 0cf262fc-1a05-419a-a503-60013f111c8a
ms.openlocfilehash: dee30096f244adc34b83fdfdc6af0baabd372b4a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672407"
---
# <a name="amp-operator-visual-basic"></a><span data-ttu-id="598f8-102">&amp;=, Opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="598f8-102">&amp;= Operator (Visual Basic)</span></span>
<span data-ttu-id="598f8-103">Concatène une `String` expression à une `String` variable ou propriété et assigne le résultat à la variable ou propriété.</span><span class="sxs-lookup"><span data-stu-id="598f8-103">Concatenates a `String` expression to a `String` variable or property and assigns the result to the variable or property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="598f8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="598f8-104">Syntax</span></span>  
  
```  
variableorproperty &= expression  
```  
  
## <a name="parts"></a><span data-ttu-id="598f8-105">Composants</span><span class="sxs-lookup"><span data-stu-id="598f8-105">Parts</span></span>  
 `variableorproperty`  
 <span data-ttu-id="598f8-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="598f8-106">Required.</span></span> <span data-ttu-id="598f8-107">N’importe quel `String` variable ou propriété.</span><span class="sxs-lookup"><span data-stu-id="598f8-107">Any `String` variable or property.</span></span>  
  
 `expression`  
 <span data-ttu-id="598f8-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="598f8-108">Required.</span></span> <span data-ttu-id="598f8-109">Toute expression `String` .</span><span class="sxs-lookup"><span data-stu-id="598f8-109">Any `String` expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="598f8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="598f8-110">Remarks</span></span>  
 <span data-ttu-id="598f8-111">L’élément sur le côté gauche de la `&=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="598f8-111">The element on the left side of the `&=` operator can be a simple scalar variable, a property, or an element of an array.</span></span> <span data-ttu-id="598f8-112">La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span><span class="sxs-lookup"><span data-stu-id="598f8-112">The variable or property cannot be [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span></span> <span data-ttu-id="598f8-113">Le `&=` opérateur concatène le `String` expression située à droite vers le `String` variable ou propriété du côté gauche et assigne le résultat à la variable ou la propriété situé à sa gauche.</span><span class="sxs-lookup"><span data-stu-id="598f8-113">The `&=` operator concatenates the `String` expression on its right to the `String` variable or property on its left, and assigns the result to the variable or property on its left.</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="598f8-114">Surcharge</span><span class="sxs-lookup"><span data-stu-id="598f8-114">Overloading</span></span>  
 <span data-ttu-id="598f8-115">Le [& opérateur](../../../visual-basic/language-reference/operators/concatenation-operator.md) peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="598f8-115">The [& Operator](../../../visual-basic/language-reference/operators/concatenation-operator.md) can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="598f8-116">La surcharge la `&` opérateur affecte le comportement de la `&=` opérateur.</span><span class="sxs-lookup"><span data-stu-id="598f8-116">Overloading the `&` operator affects the behavior of the `&=` operator.</span></span> <span data-ttu-id="598f8-117">Si votre code utilise `&=` sur une classe ou structure qui surcharge `&`, assurez-vous que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="598f8-117">If your code uses `&=` on a class or structure that overloads `&`, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="598f8-118">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="598f8-118">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="598f8-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="598f8-119">Example</span></span>  
 <span data-ttu-id="598f8-120">L’exemple suivant utilise le `&=` pour concaténer deux `String` variables et assigner le résultat à la première variable.</span><span class="sxs-lookup"><span data-stu-id="598f8-120">The following example uses the `&=` operator to concatenate two `String` variables and assign the result to the first variable.</span></span>  
  
 [!code-vb[VbVbalrOperators#3](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/and-assignment-operator_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="598f8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="598f8-121">See also</span></span>
- [<span data-ttu-id="598f8-122">& (opérateur)</span><span class="sxs-lookup"><span data-stu-id="598f8-122">& Operator</span></span>](../../../visual-basic/language-reference/operators/concatenation-operator.md)
- [<span data-ttu-id="598f8-123">+= (opérateur)</span><span class="sxs-lookup"><span data-stu-id="598f8-123">+= Operator</span></span>](../../../visual-basic/language-reference/operators/addition-assignment-operator.md)
- [<span data-ttu-id="598f8-124">Opérateurs d’assignation</span><span class="sxs-lookup"><span data-stu-id="598f8-124">Assignment Operators</span></span>](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [<span data-ttu-id="598f8-125">opérateur de concaténation</span><span class="sxs-lookup"><span data-stu-id="598f8-125">Concatenation Operators</span></span>](../../../visual-basic/language-reference/operators/concatenation-operators.md)
- [<span data-ttu-id="598f8-126">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="598f8-126">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="598f8-127">Opérateurs répertoriés par fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="598f8-127">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="598f8-128">Instructions</span><span class="sxs-lookup"><span data-stu-id="598f8-128">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
