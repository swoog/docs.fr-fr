---
title: If, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.IfOperator
- IfOperator
helpviewer_keywords:
- ternary operators [Visual Basic]
- conditional execution
- If expressions [Visual Basic]
- conditional operator [Visual Basic]
- If Operator [Visual Basic]
ms.assetid: dd56c9df-7cd4-442c-9ba6-20c70ee44c8f
ms.openlocfilehash: 192309a7ca728feb300e867bf2340e669e9da16c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33603962"
---
# <a name="if-operator-visual-basic"></a>If, opérateur (Visual Basic)
Utilise évaluation de court-circuit pour retourner conditionnellement l’une des deux valeurs. Le `If` opérateur peut être appelé avec trois arguments ou avec deux arguments.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
If( [argument1,] argument2, argument3 )  
```  
  
## <a name="if-operator-called-with-three-arguments"></a>Si l’opérateur est appelé avec trois Arguments  
 Lorsque `If` est appelée à l’aide de trois arguments, le premier argument doit correspondre à une valeur qui peut être castée en un `Boolean`. Que `Boolean` valeur détermine lequel des deux autres arguments est évaluée et retournée. La liste suivante s’applique uniquement lorsque le `If` est appelée à l’aide de trois arguments.  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`argument1`|Obligatoire. `Boolean`. Détermine lequel des autres arguments pour évaluer et retourner.|  
|`argument2`|Obligatoire. `Object`. Évaluée et retournée si `argument1` prend la valeur `True`.|  
|`argument3`|Obligatoire. `Object`. Évaluée et retournée si `argument1` prend la valeur de `False` ou si `argument1` est un [Nullable](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md) `Boolean` variable qui prend la valeur [rien](../../../visual-basic/language-reference/nothing.md).|  
  
 Un `If` opérateur est appelé avec trois arguments fonctionne comme un `IIf` fonction sauf qu’elle utilise l’évaluation de court-circuit. Un `IIf` fonction évalue toujours les trois arguments, alors qu’un `If` opérateur qui a trois arguments évalue seulement deux d'entre elles. La première `If` argument est évalué et le résultat est converti en un `Boolean` valeur, `True` ou `False`. Si la valeur est `True`, `argument2` est évalué et sa valeur est retournée, mais `argument3` n’est pas évaluée. Si la valeur de la `Boolean` expression est `False`, `argument3` est évalué et sa valeur est retournée, mais `argument2` n’est pas évaluée. Les exemples suivants illustrent l’utilisation de `If` lorsque trois arguments sont utilisés :  
  
 [!code-vb[VbVbalrOperators#100](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/if-operator_1.vb)]  
  
 L’exemple suivant illustre la valeur de l’évaluation de court-circuit. L’exemple affiche deux tentatives de diviser la variable `number` par la variable `divisor` sauf lorsque `divisor` est égal à zéro. Dans ce cas, 0 doit être retournée, et aucune tentative pour effectuer la division, car une erreur d’exécution est générée. Étant donné que le `If` expression utilise l’évaluation de court-circuit, elle évalue le deuxième ou le troisième argument, selon la valeur du premier argument. Si le premier argument est true, le diviseur n’est pas nul et évaluer le deuxième argument et la division en toute sécurité. Si le premier argument est false, seul le troisième argument est évalué et un 0 est retourné. Par conséquent, lorsque le diviseur est 0, aucune tentative n’est effectuée pour effectuer la division et aucun résultat de l’erreur. Toutefois, étant donné que `IIf` n’utilise pas l’évaluation de court-circuit, le deuxième argument est évalué même lorsque le premier argument est faux. Cela provoque une erreur de division par zéro d’exécution.  
  
 [!code-vb[VbVbalrOperators#101](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/if-operator_2.vb)]  
  
## <a name="if-operator-called-with-two-arguments"></a>Si l’opérateur est appelé avec deux Arguments  
 Le premier argument de `If` peut être omis. Cela permet à l’opérateur à être appelée en utilisant uniquement deux arguments. La liste suivante s’applique uniquement lorsque le `If` est appelée avec deux arguments.  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`argument2`|Obligatoire. `Object`. Doit être un type référence ou nullable. Évaluée et retournée lorsqu’il évalue à une valeur autre que `Nothing`.|  
|`argument3`|Obligatoire. `Object`. Évaluée et retournée si `argument2` prend la valeur `Nothing`.|  
  
 Lorsque le `Boolean` argument est omis, le premier argument doit être un type référence ou nullable. Si le premier argument prend la valeur `Nothing`, la valeur du deuxième argument est retournée. Dans tous les autres cas, la valeur du premier argument est retournée. L’exemple suivant illustre le fonctionne de cette évaluation.  
  
 [!code-vb[VbVbalrOperators#102](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/if-operator_3.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.Interaction.IIf%2A>  
 [Types valeur Nullable](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)  
 [Nothing](../../../visual-basic/language-reference/nothing.md)
