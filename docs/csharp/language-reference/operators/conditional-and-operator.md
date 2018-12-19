---
title: '&amp;&amp; Opérateur - Référence C#'
ms.custom: seodec18
ms.date: 11/06/2018
f1_keywords:
- '&&_CSharpKeyword'
helpviewer_keywords:
- '&& operator [C#]'
- logical AND operator [C#]
ms.assetid: 2e4f0a1c-92a3-40f8-8e3b-17b607f20c31
ms.openlocfilehash: 82442f50275f21e0a0748951dc50628a8d7e11bb
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243584"
---
# <a name="ampamp-operator-c-reference"></a>&amp;&amp;, opérateur (Informations de référence sur C#)

L’opérateur logique conditionnel AND `&&`, également appelé opérateur logique AND de « court-circuit », calcule l’opération logique AND de ses opérandes [bool](../keywords/bool.md). Le résultat de `x && y` est `true` si `x` et `y` prennent la valeur `true`. Sinon, le résultat est `false`. Si le premier opérande prend la valeur `false`, le deuxième n’est pas évalué. Le résultat de l’opération est donc `false`. L’exemple suivant illustre ce comportement :

[!code-csharp-interactive[conditional logical AND](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#And)]

[L’opérateur logique AND](and-operator.md) `&` calcule également l’opération logique AND de ses opérandes `bool`, mais il évalue toujours les deux opérandes.

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Un type défini par l’utilisateur ne peut pas surcharger l’opérateur logique conditionnel AND. Toutefois, si un type défini par l’utilisateur surcharge l’opérateur [logique AND](and-operator.md) et les [opérateurs true et false](../keywords/true-false-operators.md) d’une certaine manière, l’opération `&&` peut être évaluée pour les opérandes de ce type. Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels définis par l’utilisateur](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels](~/_csharplang/spec/expressions.md#conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [||, opérateur](conditional-or-operator.md)
- [\!, opérateur](logical-negation-operator.md)
- [&, opérateur](and-operator.md)
