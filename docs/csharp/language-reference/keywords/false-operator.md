---
title: false, opérateur (référence C#)
ms.date: 07/20/2015
helpviewer_keywords:
- false operator keyword [C#]
ms.assetid: 81a888fd-011e-4589-b242-6c261fea505e
ms.openlocfilehash: e73113bd37dbb68590267141ad037f78919520bc
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45648923"
---
# <a name="false-operator-c-reference"></a>false, opérateur (référence C#)

Retourne la valeur [bool](bool.md) `true` pour indiquer qu’un opérande est `false`. Sinon, retourne `false`.

Avant C# 2.0, les opérateurs `true` et `false` étaient utilisés pour créer des types valeur Nullable définis par l’utilisateur qui étaient compatibles avec les types tels que `SqlBool`. Maintenant, ce langage offre la prise en charge intégrée des types valeur Nullable. Lorsque cela vous est possible, vous devez utiliser ces types au lieu de surcharger les opérateurs `true` et `false`. Pour plus d’informations, consultez [Types Nullable](../../programming-guide/nullable-types/index.md).

Avec les valeurs booléennes Nullables, l’expression `a != b` n’est pas nécessairement égale à `!(a == b)`, car l’une ou l’autre de ces valeurs (voire les deux) peuvent être Null. Vous devez surcharger les opérateurs `true` et `false` séparément pour gérer correctement les valeurs Null de l’expression. L’exemple suivant montre comment surcharger et utiliser les opérateurs `true` et `false`.

[!code-csharp[csrefKeywordsOperator#16](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#16)]

Un type qui surcharge les opérateurs `true` et `false` peut être utilisé pour l’expression de contrôle des instructions [if](if-else.md), [do](do.md), [while](while.md) et [for](for.md), et des [expressions conditionnelles](../operators/conditional-operator.md).

Si un type définit l’opérateur `false`, il doit aussi définir l’opérateur [true](true.md).

Un type ne peut pas surcharger directement les opérateurs logiques conditionnels [&&](../operators/conditional-and-operator.md) et [&#124;&#124;](../operators/conditional-or-operator.md). Toutefois, vous pouvez obtenir un effet équivalent en surchargeant les opérateurs logiques habituels et les opérateurs `true` et `false`.

## <a name="c-language-specification"></a>spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)  
- [Guide de programmation C#](../../programming-guide/index.md)  
- [Mots clés C#](index.md)  
- [Opérateurs C#](../operators/index.md)  
- [true](true.md)  