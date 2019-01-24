---
title: If...Then...Else, instruction (Visual Basic)
ms.date: 04/16/2018
f1_keywords:
- vb.ElseIf
- vb.Then
- vb.If
- vb.EndIf
helpviewer_keywords:
- ElseIf statement [Visual Basic], If...Then...Else
- Then statement [Visual Basic], If...Then...Else
- control flow [Visual Basic], branching
- execution [Visual Basic], conditional
- TypeOf...Is expression, and If...Then...Else statements
- If...Then...Else statements
- If statement [Visual Basic], If...Then...Else
- If statement [Visual Basic]
- Is operator [Visual Basic], in If...Then...Else statements
- If Operator [Visual Basic]
- branching [Visual Basic], conditional
- If function [Visual Basic], and If...Then...Else statements
- Else statement [Visual Basic]
ms.assetid: 790068a2-1307-4e28-8a72-be5ebda099e9
ms.openlocfilehash: ceca58b2d69d72e079a9f2e2791f7f586c459167
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743645"
---
# <a name="ifthenelse-statement-visual-basic"></a><span data-ttu-id="651ac-102">If...Then...Else, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="651ac-102">If...Then...Else Statement (Visual Basic)</span></span>
<span data-ttu-id="651ac-103">Exécute un groupe d'instructions soumises à une condition, en fonction de la valeur d'une expression.</span><span class="sxs-lookup"><span data-stu-id="651ac-103">Conditionally executes a group of statements, depending on the value of an expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="651ac-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="651ac-104">Syntax</span></span>  
  
```  
' Multiline syntax:  
If condition [ Then ]  
    [ statements ]  
[ ElseIf elseifcondition [ Then ]  
    [ elseifstatements ] ]  
[ Else  
    [ elsestatements ] ]  
End If  
  
' Single-line syntax:  
If condition Then [ statements ] [ Else [ elsestatements ] ]  
```  

## <a name="quick-links-to-example-code"></a><span data-ttu-id="651ac-105">Liens rapides pour l’exemple de code</span><span class="sxs-lookup"><span data-stu-id="651ac-105">Quick links to example code</span></span>

<span data-ttu-id="651ac-106">Cet article inclut plusieurs exemples qui illustrent des utilisations de la `If`... `Then`... `Else` instruction :</span><span class="sxs-lookup"><span data-stu-id="651ac-106">This article includes several examples that illustrate uses of the `If`...`Then`...`Else` statement:</span></span>

* [<span data-ttu-id="651ac-107">Exemple de syntaxe multiligne</span><span class="sxs-lookup"><span data-stu-id="651ac-107">Multiline syntax example</span></span>](#multi-line)
* [<span data-ttu-id="651ac-108">Exemple de syntaxe imbriquée</span><span class="sxs-lookup"><span data-stu-id="651ac-108">Nested syntax example</span></span>](#nested)
* [<span data-ttu-id="651ac-109">Exemple de syntaxe de ligne</span><span class="sxs-lookup"><span data-stu-id="651ac-109">Single-line syntax example</span></span>](#single-line)

## <a name="parts"></a><span data-ttu-id="651ac-110">Composants</span><span class="sxs-lookup"><span data-stu-id="651ac-110">Parts</span></span>  
 `condition`  
 <span data-ttu-id="651ac-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="651ac-111">Required.</span></span> <span data-ttu-id="651ac-112">expression.</span><span class="sxs-lookup"><span data-stu-id="651ac-112">Expression.</span></span> <span data-ttu-id="651ac-113">Doit correspondre à `True` ou `False`, ou à un type de données qui est implicitement convertible en `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="651ac-113">Must evaluate to `True` or `False`, or to a data type that is implicitly convertible to `Boolean`.</span></span>  
  
 <span data-ttu-id="651ac-114">Si l’expression est un [Nullable](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md) `Boolean` variable qui prend la valeur [rien](../../../visual-basic/language-reference/nothing.md), la condition est traitée comme si l’expression est `False` et `Else` bloc est exécuté.</span><span class="sxs-lookup"><span data-stu-id="651ac-114">If the expression is a [Nullable](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md) `Boolean` variable that evaluates to [Nothing](../../../visual-basic/language-reference/nothing.md), the condition is treated as if the expression is `False` and the `Else` block is executed.</span></span>  
  
 `Then`  
 <span data-ttu-id="651ac-115">Requis dans la syntaxe de ligne ; facultatif dans la syntaxe multiligne.</span><span class="sxs-lookup"><span data-stu-id="651ac-115">Required in the single-line syntax; optional in the multiline syntax.</span></span>  
  
 `statements`  
 <span data-ttu-id="651ac-116">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="651ac-116">Optional.</span></span> <span data-ttu-id="651ac-117">Une ou plusieurs instructions qui suivent `If`... `Then` qui sont exécutées si `condition` prend la valeur `True`.</span><span class="sxs-lookup"><span data-stu-id="651ac-117">One or more statements following `If`...`Then` that are executed if `condition` evaluates to `True`.</span></span>  
  
 `elseifcondition`  
 <span data-ttu-id="651ac-118">Obligatoire si `ElseIf` est présent.</span><span class="sxs-lookup"><span data-stu-id="651ac-118">Required if `ElseIf` is present.</span></span> <span data-ttu-id="651ac-119">expression.</span><span class="sxs-lookup"><span data-stu-id="651ac-119">Expression.</span></span> <span data-ttu-id="651ac-120">Doit correspondre à `True` ou `False`, ou à un type de données qui est implicitement convertible en `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="651ac-120">Must evaluate to `True` or `False`, or to a data type that is implicitly convertible to `Boolean`.</span></span>  
  
 `elseifstatements`  
 <span data-ttu-id="651ac-121">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="651ac-121">Optional.</span></span> <span data-ttu-id="651ac-122">Une ou plusieurs instructions qui suivent `ElseIf`... `Then` qui sont exécutées si `elseifcondition` prend la valeur `True`.</span><span class="sxs-lookup"><span data-stu-id="651ac-122">One or more statements following `ElseIf`...`Then` that are executed if `elseifcondition` evaluates to `True`.</span></span>  
  
 `elsestatements`  
 <span data-ttu-id="651ac-123">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="651ac-123">Optional.</span></span> <span data-ttu-id="651ac-124">Une ou plusieurs instructions sont exécutées si aucune `condition` ou `elseifcondition` expression prend la valeur `True`.</span><span class="sxs-lookup"><span data-stu-id="651ac-124">One or more statements that are executed if no previous `condition` or `elseifcondition` expression evaluates to `True`.</span></span>  
  
 `End If`  
 <span data-ttu-id="651ac-125">Met fin à la version multiligne de `If`... `Then`... `Else` bloc.</span><span class="sxs-lookup"><span data-stu-id="651ac-125">Terminates the multiline version of `If`...`Then`...`Else` block.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="651ac-126">Notes</span><span class="sxs-lookup"><span data-stu-id="651ac-126">Remarks</span></span>  
  
### <a name="multiline-syntax"></a><span data-ttu-id="651ac-127">Syntaxe multiligne</span><span class="sxs-lookup"><span data-stu-id="651ac-127">Multiline syntax</span></span>  
 <span data-ttu-id="651ac-128">Quand un `If`... `Then`... `Else` est rencontrée, `condition` est testée.</span><span class="sxs-lookup"><span data-stu-id="651ac-128">When an `If`...`Then`...`Else` statement is encountered, `condition` is tested.</span></span> <span data-ttu-id="651ac-129">Si `condition` est `True`, les instructions qui suivent `Then` sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="651ac-129">If `condition` is `True`, the statements following `Then` are executed.</span></span> <span data-ttu-id="651ac-130">Si `condition` est `False`, chaque `ElseIf` instruction (le cas échéant) est évaluée dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="651ac-130">If `condition` is `False`, each `ElseIf` statement (if there are any) is evaluated in order.</span></span> <span data-ttu-id="651ac-131">Quand un `True` `elseifcondition` est trouvée, les instructions qui suit immédiatement la `ElseIf` sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="651ac-131">When a `True` `elseifcondition` is found, the statements immediately following the associated `ElseIf` are executed.</span></span> <span data-ttu-id="651ac-132">Si aucun `elseifcondition` prend la valeur `True`, ou s’il existe aucune `ElseIf` instructions, les instructions qui suivent `Else` sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="651ac-132">If no `elseifcondition` evaluates to `True`, or if there are no `ElseIf` statements, the statements following `Else` are executed.</span></span> <span data-ttu-id="651ac-133">Après avoir exécuté les instructions situées après `Then`, `ElseIf`, ou `Else`, l’exécution se poursuit avec l’instruction qui suit `End If`.</span><span class="sxs-lookup"><span data-stu-id="651ac-133">After executing the statements following `Then`, `ElseIf`, or `Else`, execution continues with the statement following `End If`.</span></span>  
  
 <span data-ttu-id="651ac-134">Le `ElseIf` et `Else` clauses sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="651ac-134">The `ElseIf` and `Else` clauses are both optional.</span></span> <span data-ttu-id="651ac-135">Vous pouvez avoir autant `ElseIf` clauses que vous voulez dans un `If`... `Then`... `Else` instruction, mais pas `ElseIf` clause peut apparaître après un `Else` clause.</span><span class="sxs-lookup"><span data-stu-id="651ac-135">You can have as many `ElseIf` clauses as you want in an `If`...`Then`...`Else` statement, but no `ElseIf` clause can appear after an `Else` clause.</span></span> <span data-ttu-id="651ac-136">`If`... `Then`... `Else` instructions peuvent être imbriquées dans d’autres.</span><span class="sxs-lookup"><span data-stu-id="651ac-136">`If`...`Then`...`Else` statements can be nested within each other.</span></span>  
  
 <span data-ttu-id="651ac-137">Dans la syntaxe multiligne, la `If` instruction doit être la seule instruction sur la première ligne.</span><span class="sxs-lookup"><span data-stu-id="651ac-137">In the multiline syntax, the `If` statement must be the only statement on the first line.</span></span> <span data-ttu-id="651ac-138">Le `ElseIf`, `Else`, et `End If` instructions peuvent être précédées que par une étiquette de ligne.</span><span class="sxs-lookup"><span data-stu-id="651ac-138">The `ElseIf`, `Else`, and `End If` statements can be preceded only by a line label.</span></span> <span data-ttu-id="651ac-139">Le `If`... `Then`... `Else` bloc doit se terminer par un `End If` instruction.</span><span class="sxs-lookup"><span data-stu-id="651ac-139">The `If`...`Then`...`Else` block must end with an `End If` statement.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="651ac-140">Le [sélectionnez... Instruction case](../../../visual-basic/language-reference/statements/select-case-statement.md) peut être plus utile lorsque vous évaluez une expression unique qui possède plusieurs valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="651ac-140">The [Select...Case Statement](../../../visual-basic/language-reference/statements/select-case-statement.md) might be more useful when you evaluate a single expression that has several possible values.</span></span>  
  
### <a name="single-line-syntax"></a><span data-ttu-id="651ac-141">Syntaxe de ligne</span><span class="sxs-lookup"><span data-stu-id="651ac-141">Single-Line syntax</span></span>  
 <span data-ttu-id="651ac-142">Vous pouvez utiliser la syntaxe de ligne pour une seule condition avec le code à exécuter si c’est vrai.</span><span class="sxs-lookup"><span data-stu-id="651ac-142">You can use the single-line syntax for a single condition with code to execute if it's true.</span></span> <span data-ttu-id="651ac-143">Toutefois, la syntaxe de plusieurs lignes fournit plus de structure et de flexibilité et est plus facile à lire, gérer et déboguer.</span><span class="sxs-lookup"><span data-stu-id="651ac-143">However, the multiple-line syntax provides more structure and flexibility and is easier to read, maintain, and debug.</span></span>  
  
 <span data-ttu-id="651ac-144">Ce qui suit le `Then` mot clé est examinée pour déterminer si une instruction est une seule ligne `If`.</span><span class="sxs-lookup"><span data-stu-id="651ac-144">What follows the `Then` keyword is examined to determine whether a statement is a single-line `If`.</span></span> <span data-ttu-id="651ac-145">Si autre chose qu’un commentaire apparaît après `Then` sur la même ligne, l’instruction est traitée comme une seule ligne `If` instruction.</span><span class="sxs-lookup"><span data-stu-id="651ac-145">If anything other than a comment appears after `Then` on the same line, the statement is treated as a single-line `If` statement.</span></span> <span data-ttu-id="651ac-146">Si `Then` est absent, il doit être le début d’une ligne de plusieurs `If`... `Then`... `Else`.</span><span class="sxs-lookup"><span data-stu-id="651ac-146">If `Then` is absent, it must be the start of a multiple-line `If`...`Then`...`Else`.</span></span>  
  
 <span data-ttu-id="651ac-147">Dans la syntaxe de ligne simple, vous pouvez avoir plusieurs instructions exécutées en tant que le résultat d’une `If`... `Then` décision.</span><span class="sxs-lookup"><span data-stu-id="651ac-147">In the single-line syntax, you can have multiple statements executed as the result of an `If`...`Then` decision.</span></span> <span data-ttu-id="651ac-148">Toutes les instructions doivent se trouver sur la même ligne et être séparées par le signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="651ac-148">All statements must be on the same line and be separated by colons.</span></span>  

## <a name="multiline-syntax-example"></a><span data-ttu-id="651ac-149">Exemple de syntaxe multiligne</span><span class="sxs-lookup"><span data-stu-id="651ac-149">Multiline syntax example</span></span>

<a name="multi-line"></a>
 
 <span data-ttu-id="651ac-150">L’exemple suivant illustre l’utilisation de la syntaxe multiligne de la `If`... `Then`... `Else` instruction.</span><span class="sxs-lookup"><span data-stu-id="651ac-150">The following example illustrates the use of the multiline syntax of the `If`...`Then`...`Else` statement.</span></span>  
  
 [!code-vb[VbVbalrStatements#101](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/if-then-else-statement_1.vb?highlight=11,14,17,19)]

## <a name="nested-syntax-example"></a><span data-ttu-id="651ac-151">Exemple de syntaxe imbriquée</span><span class="sxs-lookup"><span data-stu-id="651ac-151">Nested syntax example</span></span>

<a name="nested"></a>

 <span data-ttu-id="651ac-152">L’exemple suivant contient imbriquée `If`... `Then`... `Else` instructions.</span><span class="sxs-lookup"><span data-stu-id="651ac-152">The following example contains nested `If`...`Then`...`Else` statements.</span></span>  
  
 [!code-vb[VbVbalrStatements#102](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/if-then-else-statement_2.vb?highlight=14,15,17,19,20,21,23,25,26,28)]

## <a name="single-line-syntax-example"></a><span data-ttu-id="651ac-153">Exemple de syntaxe de ligne</span><span class="sxs-lookup"><span data-stu-id="651ac-153">Single-Line syntax example</span></span>
  
<a name="single-line"></a> <span data-ttu-id="651ac-154">L’exemple suivant illustre l’utilisation de la syntaxe de ligne simple.</span><span class="sxs-lookup"><span data-stu-id="651ac-154">The following example illustrates the use of the single-line syntax.</span></span>  
  
 [!code-vb[VbVbalrStatements#103](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/if-then-else-statement_3.vb?highlight=18)]
  
## <a name="see-also"></a><span data-ttu-id="651ac-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="651ac-155">See also</span></span>
- <xref:Microsoft.VisualBasic.Interaction.Choose%2A>
- <xref:Microsoft.VisualBasic.Interaction.Switch%2A>
- [<span data-ttu-id="651ac-156">#If...Then...#Else, directives</span><span class="sxs-lookup"><span data-stu-id="651ac-156">#If...Then...#Else Directives</span></span>](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
- [<span data-ttu-id="651ac-157">Select...Case (instruction)</span><span class="sxs-lookup"><span data-stu-id="651ac-157">Select...Case Statement</span></span>](../../../visual-basic/language-reference/statements/select-case-statement.md)
- [<span data-ttu-id="651ac-158">Structures de contrôle imbriquées</span><span class="sxs-lookup"><span data-stu-id="651ac-158">Nested Control Structures</span></span>](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)
- [<span data-ttu-id="651ac-159">Structures de décision</span><span class="sxs-lookup"><span data-stu-id="651ac-159">Decision Structures</span></span>](../../../visual-basic/programming-guide/language-features/control-flow/decision-structures.md)
- [<span data-ttu-id="651ac-160">Opérateurs logiques et au niveau du bit en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="651ac-160">Logical and Bitwise Operators in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
- [<span data-ttu-id="651ac-161">If (opérateur)</span><span class="sxs-lookup"><span data-stu-id="651ac-161">If Operator</span></span>](../../../visual-basic/language-reference/operators/if-operator.md)
