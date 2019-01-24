---
title: =, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Assign
- vb.=
helpviewer_keywords:
- = operator [Visual Basic]
- = assignment statements [Visual Basic]
ms.assetid: 2dac2e49-86c8-42f8-80c1-458452fb5e29
ms.openlocfilehash: 58dcdfd21fd8701c6ac391672e768819f696aab9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54643547"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="54a64-102">=, opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="54a64-102">= Operator (Visual Basic)</span></span>
<span data-ttu-id="54a64-103">Assigne une valeur à une variable ou une propriété.</span><span class="sxs-lookup"><span data-stu-id="54a64-103">Assigns a value to a variable or property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="54a64-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54a64-104">Syntax</span></span>  
  
```  
variableorproperty = value  
```  
  
## <a name="parts"></a><span data-ttu-id="54a64-105">Composants</span><span class="sxs-lookup"><span data-stu-id="54a64-105">Parts</span></span>  
 `variableorproperty`  
 <span data-ttu-id="54a64-106">N’importe quelle variable accessible en écriture ou toute propriété.</span><span class="sxs-lookup"><span data-stu-id="54a64-106">Any writable variable or any property.</span></span>  
  
 `value`  
 <span data-ttu-id="54a64-107">N’importe quel littéral, une constante ou une expression.</span><span class="sxs-lookup"><span data-stu-id="54a64-107">Any literal, constant, or expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="54a64-108">Notes</span><span class="sxs-lookup"><span data-stu-id="54a64-108">Remarks</span></span>  
 <span data-ttu-id="54a64-109">L’élément situé à gauche du signe égal (`=`) peut être une simple variable scalaire, une propriété ou un élément d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="54a64-109">The element on the left side of the equal sign (`=`) can be a simple scalar variable, a property, or an element of an array.</span></span> <span data-ttu-id="54a64-110">La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span><span class="sxs-lookup"><span data-stu-id="54a64-110">The variable or property cannot be [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span></span> <span data-ttu-id="54a64-111">Le `=` opérateur assigne la valeur située à droite vers la variable ou propriété du côté gauche.</span><span class="sxs-lookup"><span data-stu-id="54a64-111">The `=` operator assigns the value on its right to the variable or property on its left.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="54a64-112">Le `=` opérateur est également utilisé comme un opérateur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="54a64-112">The `=` operator is also used as a comparison operator.</span></span> <span data-ttu-id="54a64-113">Pour plus d’informations, consultez [opérateurs de comparaison](../../../visual-basic/language-reference/operators/comparison-operators.md).</span><span class="sxs-lookup"><span data-stu-id="54a64-113">For details, see [Comparison Operators](../../../visual-basic/language-reference/operators/comparison-operators.md).</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="54a64-114">Surcharge</span><span class="sxs-lookup"><span data-stu-id="54a64-114">Overloading</span></span>  
 <span data-ttu-id="54a64-115">Le `=` opérateur permettre être surchargée uniquement comme un opérateur de comparaison relationnel, et non comme un opérateur d’assignation.</span><span class="sxs-lookup"><span data-stu-id="54a64-115">The `=` operator can be overloaded only as a relational comparison operator, not as an assignment operator.</span></span> <span data-ttu-id="54a64-116">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="54a64-116">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="54a64-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="54a64-117">Example</span></span>  
 <span data-ttu-id="54a64-118">L’exemple suivant illustre l’opérateur d’assignation.</span><span class="sxs-lookup"><span data-stu-id="54a64-118">The following example demonstrates the assignment operator.</span></span> <span data-ttu-id="54a64-119">La valeur de droite est assignée à la variable sur la gauche.</span><span class="sxs-lookup"><span data-stu-id="54a64-119">The value on the right is assigned to the variable on the left.</span></span>  
  
 [!code-vb[VbVbalrOperators#9](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/assignment-operator_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="54a64-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54a64-120">See also</span></span>
- [<span data-ttu-id="54a64-121">&= (opérateur)</span><span class="sxs-lookup"><span data-stu-id="54a64-121">&= Operator</span></span>](../../../visual-basic/language-reference/operators/and-assignment-operator.md)
- [<span data-ttu-id="54a64-122">\*= (opérateur)</span><span class="sxs-lookup"><span data-stu-id="54a64-122">\*= Operator</span></span>](../../../visual-basic/language-reference/operators/multiplication-assignment-operator.md)
- [<span data-ttu-id="54a64-123">+= (opérateur)</span><span class="sxs-lookup"><span data-stu-id="54a64-123">+= Operator</span></span>](../../../visual-basic/language-reference/operators/addition-assignment-operator.md)
- [<span data-ttu-id="54a64-124">-=, Opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="54a64-124">-= Operator (Visual Basic)</span></span>](../../../visual-basic/language-reference/operators/subtraction-assignment-operator.md)
- [<span data-ttu-id="54a64-125">/ =, Opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="54a64-125">/= Operator (Visual Basic)</span></span>](../../../visual-basic/language-reference/operators/floating-point-division-assignment-operator.md)
- [<span data-ttu-id="54a64-126">\\=, Opérateur</span><span class="sxs-lookup"><span data-stu-id="54a64-126">\\= Operator</span></span>](../../../visual-basic/language-reference/operators/integer-division-assignment-operator.md)
- [<span data-ttu-id="54a64-127">^= (opérateur)</span><span class="sxs-lookup"><span data-stu-id="54a64-127">^= Operator</span></span>](../../../visual-basic/language-reference/operators/exponentiation-assignment-operator.md)
- [<span data-ttu-id="54a64-128">Instructions</span><span class="sxs-lookup"><span data-stu-id="54a64-128">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
- [<span data-ttu-id="54a64-129">Opérateurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="54a64-129">Comparison Operators</span></span>](../../../visual-basic/language-reference/operators/comparison-operators.md)
- [<span data-ttu-id="54a64-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="54a64-130">ReadOnly</span></span>](../../../visual-basic/language-reference/modifiers/readonly.md)
- [<span data-ttu-id="54a64-131">Inférence de type local</span><span class="sxs-lookup"><span data-stu-id="54a64-131">Local Type Inference</span></span>](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
