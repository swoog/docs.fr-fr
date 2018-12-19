---
title: '||, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 11/06/2018
f1_keywords:
- '||_CSharpKeyword'
helpviewer_keywords:
- logical OR operator [C#]
- conditional-OR operator (||) [C#]
- '|| operator [C#]'
ms.assetid: 7d442d8e-400d-421f-b4d2-034bf82bcbdc
ms.openlocfilehash: f4bb7ada12fbcebcb90fb7cd22d6e6bccad5fb57
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53244568"
---
# <a name="-operator-c-reference"></a>||, opérateur (référence C#)

L’opérateur logique conditionnel OR `||`, également appelé opérateur logique OR de « court-circuit », calcule l’opération logique OR de ses opérandes [bool](../keywords/bool.md). Le résultat de `x || y` est `true` si `x` ou `y` prend la valeur `true`. Sinon, le résultat est `false`. Si le premier opérande prend la valeur `true`, le deuxième n’est pas évalué. Le résultat de l’opération est donc `true`. L’exemple suivant illustre ce comportement :

[!code-csharp-interactive[conditional logical OR](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#Or)]

[L’opérateur logique OR](or-operator.md) `|` calcule également l’opération logique OR de ses opérandes `bool`, mais il évalue toujours les deux opérandes.

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Un type défini par l’utilisateur ne peut pas surcharger l’opérateur logique conditionnel OR. Toutefois, si un type défini par l’utilisateur surcharge l’opérateur [logique OR](or-operator.md) et [les opérateurs true et false](../keywords/true-false-operators.md) d’une certaine manière, l’opération `||` peut être évaluée pour les opérandes de ce type. Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels définis par l’utilisateur](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels](~/_csharplang/spec/expressions.md#conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [&&, opérateur](conditional-and-operator.md)
- [!, opérateur](logical-negation-operator.md)
- [|, opérateur](or-operator.md)
