---
title: 'Procédure : Appeler une procédure d’opérateur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- operator procedures [Visual Basic], calling
- procedures [Visual Basic], operator
- procedure calls [Visual Basic], operator overloading
- syntax [Visual Basic], Operator procedures
- operators [Visual Basic], overloading
- return values [Visual Basic], Operator procedures
- overloaded operators [Visual Basic], calling
- operator overloading
ms.assetid: 0dce42cc-f0b0-4c14-9f62-018b21f33497
ms.openlocfilehash: fc658dd7ef001c8d3ef7761bd2a7889f70e9e4a3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54667581"
---
# <a name="how-to-call-an-operator-procedure-visual-basic"></a><span data-ttu-id="0ccc8-102">Procédure : Appeler une procédure d’opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0ccc8-102">How to: Call an Operator Procedure (Visual Basic)</span></span>
<span data-ttu-id="0ccc8-103">Vous appelez une procédure d’opérateur en utilisant le symbole d’opérateur dans une expression.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-103">You call an operator procedure by using the operator symbol in an expression.</span></span> <span data-ttu-id="0ccc8-104">Dans le cas d’un opérateur de conversion, vous appelez le [CType Function](../../../../visual-basic/language-reference/functions/ctype-function.md) pour convertir une valeur à partir d’un type de données à un autre.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-104">In the case of a conversion operator, you call the [CType Function](../../../../visual-basic/language-reference/functions/ctype-function.md) to convert a value from one data type to another.</span></span>  
  
 <span data-ttu-id="0ccc8-105">Vous n’appelez pas explicitement de procédures d’opérateur.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-105">You do not call operator procedures explicitly.</span></span> <span data-ttu-id="0ccc8-106">Vous utilisez l’opérateur, ou la `CType` fonction dans une instruction d’assignation ou une expression, la même façon que vous utilisez normalement un opérateur.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-106">You just use the operator, or the `CType` function, in an assignment statement or an expression, the same way you ordinarily use an operator.</span></span> <span data-ttu-id="0ccc8-107">Visual Basic effectue l’appel à la procédure d’opérateur.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-107">Visual Basic makes the call to the operator procedure.</span></span>  
  
 <span data-ttu-id="0ccc8-108">Définition d’un opérateur sur une classe ou structure est également appelée *surcharge* l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-108">Defining an operator on a class or structure is also called *overloading* the operator.</span></span>  
  
### <a name="to-call-an-operator-procedure"></a><span data-ttu-id="0ccc8-109">Pour appeler une procédure d’opérateur</span><span class="sxs-lookup"><span data-stu-id="0ccc8-109">To call an operator procedure</span></span>  
  
1.  <span data-ttu-id="0ccc8-110">Utilisez le symbole d’opérateur dans une expression de la façon habituelle.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-110">Use the operator symbol in an expression in the ordinary way.</span></span>  
  
2.  <span data-ttu-id="0ccc8-111">N’oubliez pas que les types de données des opérandes sont appropriés pour l’opérateur et dans le bon ordre.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-111">Be sure the data types of the operands are appropriate for the operator, and in the correct order.</span></span>  
  
3.  <span data-ttu-id="0ccc8-112">L’opérateur contribue à la valeur de l’expression comme prévu.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-112">The operator contributes to the value of the expression as expected.</span></span>  
  
### <a name="to-call-a-conversion-operator-procedure"></a><span data-ttu-id="0ccc8-113">Pour appeler une procédure d’opérateur de conversion</span><span class="sxs-lookup"><span data-stu-id="0ccc8-113">To call a conversion operator procedure</span></span>  
  
1.  <span data-ttu-id="0ccc8-114">Utilisez `CType` à l’intérieur d’une expression.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-114">Use `CType` inside an expression.</span></span>  
  
2.  <span data-ttu-id="0ccc8-115">N’oubliez pas que les types de données des opérandes sont appropriés pour la conversion et dans le bon ordre.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-115">Be sure the data types of the operands are appropriate for the conversion, and in the correct order.</span></span>  
  
3.  <span data-ttu-id="0ccc8-116">`CType` appelle la procédure d’opérateur de conversion et retourne la valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-116">`CType` calls the conversion operator procedure and returns the converted value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0ccc8-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="0ccc8-117">Example</span></span>  
 <span data-ttu-id="0ccc8-118">L’exemple suivant crée deux <xref:System.TimeSpan> structures, les additionne et stocke le résultat dans une troisième <xref:System.TimeSpan> structure.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-118">The following example creates two <xref:System.TimeSpan> structures, adds them together, and stores the result in a third <xref:System.TimeSpan> structure.</span></span> <span data-ttu-id="0ccc8-119">Le <xref:System.TimeSpan> structure définit des procédures d’opérateur pour surcharger plusieurs opérateurs standards.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-119">The <xref:System.TimeSpan> structure defines operator procedures to overload several standard operators.</span></span>  
  
 [!code-vb[VbVbcnProcedures#29](./codesnippet/VisualBasic/how-to-call-an-operator-procedure_1.vb)]  
  
 <span data-ttu-id="0ccc8-120">Étant donné que <xref:System.TimeSpan> surcharges de la norme `+` opérateur, l’exemple précédent appelle une procédure d’opérateur lorsqu’il calcule la valeur de `combinedSpan`.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-120">Because <xref:System.TimeSpan> overloads the standard `+` operator, the previous example calls an operator procedure when it calculates the value of `combinedSpan`.</span></span>  
  
 <span data-ttu-id="0ccc8-121">Pour obtenir un exemple d’appel de procédure d’opérateur de conversation, consultez [Comment : Utiliser une classe qui définit des opérateurs](./how-to-use-a-class-that-defines-operators.md).</span><span class="sxs-lookup"><span data-stu-id="0ccc8-121">For an example of calling a conversation operator procedure, see [How to: Use a Class that Defines Operators](./how-to-use-a-class-that-defines-operators.md).</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0ccc8-122">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="0ccc8-122">Compiling the Code</span></span>  
 <span data-ttu-id="0ccc8-123">N’oubliez pas de la classe ou structure que vous utilisez définit l’opérateur que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="0ccc8-123">Be sure the class or structure you are using defines the operator you want to use.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ccc8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ccc8-124">See also</span></span>
- [<span data-ttu-id="0ccc8-125">Procédures d’opérateur</span><span class="sxs-lookup"><span data-stu-id="0ccc8-125">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="0ccc8-126">Guide pratique pour Définir un opérateur</span><span class="sxs-lookup"><span data-stu-id="0ccc8-126">How to: Define an Operator</span></span>](./how-to-define-an-operator.md)
- [<span data-ttu-id="0ccc8-127">Guide pratique pour Définir un opérateur de Conversion</span><span class="sxs-lookup"><span data-stu-id="0ccc8-127">How to: Define a Conversion Operator</span></span>](./how-to-define-a-conversion-operator.md)
- [<span data-ttu-id="0ccc8-128">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="0ccc8-128">Operator Statement</span></span>](../../../../visual-basic/language-reference/statements/operator-statement.md)
- [<span data-ttu-id="0ccc8-129">Widening</span><span class="sxs-lookup"><span data-stu-id="0ccc8-129">Widening</span></span>](../../../../visual-basic/language-reference/modifiers/widening.md)
- [<span data-ttu-id="0ccc8-130">Narrowing</span><span class="sxs-lookup"><span data-stu-id="0ccc8-130">Narrowing</span></span>](../../../../visual-basic/language-reference/modifiers/narrowing.md)
- [<span data-ttu-id="0ccc8-131">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="0ccc8-131">Structure Statement</span></span>](../../../../visual-basic/language-reference/statements/structure-statement.md)
- [<span data-ttu-id="0ccc8-132">Guide pratique pour déclarer une structure</span><span class="sxs-lookup"><span data-stu-id="0ccc8-132">How to: Declare a Structure</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [<span data-ttu-id="0ccc8-133">Conversions implicites et explicites</span><span class="sxs-lookup"><span data-stu-id="0ccc8-133">Implicit and Explicit Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
- [<span data-ttu-id="0ccc8-134">Conversions étendues et restrictives</span><span class="sxs-lookup"><span data-stu-id="0ccc8-134">Widening and Narrowing Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
