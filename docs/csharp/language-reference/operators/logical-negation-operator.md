---
title: '! opérateur - Référence C#'
ms.custom: seodec18
ms.date: 02/14/2019
f1_keywords:
- '!_CSharpKeyword'
helpviewer_keywords:
- '! operator [C#]'
- logical negation operator (!) [C#]
- NOT operator [C#]
ms.assetid: f5ae133f-8f64-4560-b34f-cd9cd5eed4ad
ms.openlocfilehash: 464bd658c9bf430191d84d3d5ad8d57173ab87c5
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56303710"
---
# <a name="-operator-c-reference"></a>! operator (référence C#)

L’opérateur de négation logique `!` est un opérateur unaire qui calcule la négation logique de son opérande [bool](../keywords/bool.md). Autrement dit, il génère `true` si l’opérande est `false`, et `false` si l’opérande est `true` :

[!code-csharp-interactive[logical negation](~/samples/snippets/csharp/language-reference/operators/LogicalNegationExamples.cs#Example)]

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `!`.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, voir la section [Opérateur de négation logique](~/_csharplang/spec/expressions.md#logical-negation-operator) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)