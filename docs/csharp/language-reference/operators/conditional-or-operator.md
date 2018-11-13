---
title: '||, opérateur (référence C#)'
ms.date: 11/06/2018
f1_keywords:
- '||_CSharpKeyword'
helpviewer_keywords:
- logical OR operator [C#]
- conditional-OR operator (||) [C#]
- '|| operator [C#]'
ms.assetid: 7d442d8e-400d-421f-b4d2-034bf82bcbdc
ms.openlocfilehash: a391078372e4ec0a3882bed4515733adedffb547
ms.sourcegitcommit: b5cd9d5d3b75a5537fc9ad8a3f085f0bb1845ee0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "42925538"
---
# <a name="-operator-c-reference"></a>||, opérateur (référence C#)

L’opérateur logique conditionnel OR `||`, également appelé opérateur logique OR de « court-circuit », calcule l’opération logique OR de ses opérandes [bool](../keywords/bool.md). Le résultat de `x || y` est `true` si `x` ou `y` prend la valeur `true`. Sinon, le résultat est `false`. Si le premier opérande prend la valeur `true`, le deuxième n’est pas évalué. Le résultat de l’opération est donc `true`. L’exemple suivant illustre ce comportement :

[!code-csharp-interactive[conditional logical OR](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#Or)]

[L’opérateur logique OR](or-operator.md) `|` calcule également l’opération logique OR de ses opérandes `bool`, mais il évalue toujours les deux opérandes.

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Un type défini par l’utilisateur ne peut pas surcharger l’opérateur logique conditionnel OR. Toutefois, si un type défini par l’utilisateur surcharge l’opérateur [logique OR](or-operator.md) et les opérateurs [true](../keywords/true-operator.md) et [false](../keywords/false-operator.md) d’une certaine manière, l’opération `||` peut être évaluée pour les opérandes de ce type. Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels définis par l’utilisateur](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels](~/_csharplang/spec/expressions.md#conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [&&, opérateur](conditional-and-operator.md)
- [!, opérateur](logical-negation-operator.md)
- [|, opérateur](or-operator.md)
