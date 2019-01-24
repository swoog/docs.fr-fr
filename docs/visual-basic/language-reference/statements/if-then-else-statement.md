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
# <a name="ifthenelse-statement-visual-basic"></a>If...Then...Else, instruction (Visual Basic)
Exécute un groupe d'instructions soumises à une condition, en fonction de la valeur d'une expression.  
  
## <a name="syntax"></a>Syntaxe  
  
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

## <a name="quick-links-to-example-code"></a>Liens rapides pour l’exemple de code

Cet article inclut plusieurs exemples qui illustrent des utilisations de la `If`... `Then`... `Else` instruction :

* [Exemple de syntaxe multiligne](#multi-line)
* [Exemple de syntaxe imbriquée](#nested)
* [Exemple de syntaxe de ligne](#single-line)

## <a name="parts"></a>Composants  
 `condition`  
 Obligatoire. expression. Doit correspondre à `True` ou `False`, ou à un type de données qui est implicitement convertible en `Boolean`.  
  
 Si l’expression est un [Nullable](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md) `Boolean` variable qui prend la valeur [rien](../../../visual-basic/language-reference/nothing.md), la condition est traitée comme si l’expression est `False` et `Else` bloc est exécuté.  
  
 `Then`  
 Requis dans la syntaxe de ligne ; facultatif dans la syntaxe multiligne.  
  
 `statements`  
 Facultatif. Une ou plusieurs instructions qui suivent `If`... `Then` qui sont exécutées si `condition` prend la valeur `True`.  
  
 `elseifcondition`  
 Obligatoire si `ElseIf` est présent. expression. Doit correspondre à `True` ou `False`, ou à un type de données qui est implicitement convertible en `Boolean`.  
  
 `elseifstatements`  
 Facultatif. Une ou plusieurs instructions qui suivent `ElseIf`... `Then` qui sont exécutées si `elseifcondition` prend la valeur `True`.  
  
 `elsestatements`  
 Facultatif. Une ou plusieurs instructions sont exécutées si aucune `condition` ou `elseifcondition` expression prend la valeur `True`.  
  
 `End If`  
 Met fin à la version multiligne de `If`... `Then`... `Else` bloc.  
  
## <a name="remarks"></a>Notes  
  
### <a name="multiline-syntax"></a>Syntaxe multiligne  
 Quand un `If`... `Then`... `Else` est rencontrée, `condition` est testée. Si `condition` est `True`, les instructions qui suivent `Then` sont exécutées. Si `condition` est `False`, chaque `ElseIf` instruction (le cas échéant) est évaluée dans l’ordre. Quand un `True` `elseifcondition` est trouvée, les instructions qui suit immédiatement la `ElseIf` sont exécutées. Si aucun `elseifcondition` prend la valeur `True`, ou s’il existe aucune `ElseIf` instructions, les instructions qui suivent `Else` sont exécutées. Après avoir exécuté les instructions situées après `Then`, `ElseIf`, ou `Else`, l’exécution se poursuit avec l’instruction qui suit `End If`.  
  
 Le `ElseIf` et `Else` clauses sont facultatifs. Vous pouvez avoir autant `ElseIf` clauses que vous voulez dans un `If`... `Then`... `Else` instruction, mais pas `ElseIf` clause peut apparaître après un `Else` clause. `If`... `Then`... `Else` instructions peuvent être imbriquées dans d’autres.  
  
 Dans la syntaxe multiligne, la `If` instruction doit être la seule instruction sur la première ligne. Le `ElseIf`, `Else`, et `End If` instructions peuvent être précédées que par une étiquette de ligne. Le `If`... `Then`... `Else` bloc doit se terminer par un `End If` instruction.  
  
> [!TIP]
>  Le [sélectionnez... Instruction case](../../../visual-basic/language-reference/statements/select-case-statement.md) peut être plus utile lorsque vous évaluez une expression unique qui possède plusieurs valeurs possibles.  
  
### <a name="single-line-syntax"></a>Syntaxe de ligne  
 Vous pouvez utiliser la syntaxe de ligne pour une seule condition avec le code à exécuter si c’est vrai. Toutefois, la syntaxe de plusieurs lignes fournit plus de structure et de flexibilité et est plus facile à lire, gérer et déboguer.  
  
 Ce qui suit le `Then` mot clé est examinée pour déterminer si une instruction est une seule ligne `If`. Si autre chose qu’un commentaire apparaît après `Then` sur la même ligne, l’instruction est traitée comme une seule ligne `If` instruction. Si `Then` est absent, il doit être le début d’une ligne de plusieurs `If`... `Then`... `Else`.  
  
 Dans la syntaxe de ligne simple, vous pouvez avoir plusieurs instructions exécutées en tant que le résultat d’une `If`... `Then` décision. Toutes les instructions doivent se trouver sur la même ligne et être séparées par le signe deux-points.  

## <a name="multiline-syntax-example"></a>Exemple de syntaxe multiligne

<a name="multi-line"></a>
 
 L’exemple suivant illustre l’utilisation de la syntaxe multiligne de la `If`... `Then`... `Else` instruction.  
  
 [!code-vb[VbVbalrStatements#101](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/if-then-else-statement_1.vb?highlight=11,14,17,19)]

## <a name="nested-syntax-example"></a>Exemple de syntaxe imbriquée

<a name="nested"></a>

 L’exemple suivant contient imbriquée `If`... `Then`... `Else` instructions.  
  
 [!code-vb[VbVbalrStatements#102](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/if-then-else-statement_2.vb?highlight=14,15,17,19,20,21,23,25,26,28)]

## <a name="single-line-syntax-example"></a>Exemple de syntaxe de ligne
  
<a name="single-line"></a> L’exemple suivant illustre l’utilisation de la syntaxe de ligne simple.  
  
 [!code-vb[VbVbalrStatements#103](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/if-then-else-statement_3.vb?highlight=18)]
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.Interaction.Choose%2A>
- <xref:Microsoft.VisualBasic.Interaction.Switch%2A>
- [#If...Then...#Else, directives](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
- [Select...Case (instruction)](../../../visual-basic/language-reference/statements/select-case-statement.md)
- [Structures de contrôle imbriquées](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)
- [Structures de décision](../../../visual-basic/programming-guide/language-features/control-flow/decision-structures.md)
- [Opérateurs logiques et au niveau du bit en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
- [If (opérateur)](../../../visual-basic/language-reference/operators/if-operator.md)
