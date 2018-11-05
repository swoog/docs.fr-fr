---
title: 'Expressions conditionnelles : if... then...else (F#)'
description: Apprenez à écrire des expressions conditionnelles en F# pour exécuter différentes branches de code.
ms.date: 05/16/2016
ms.openlocfilehash: 10e4224bef772f00520cf5a0fff2f2920147c2fc
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "44177599"
---
# <a name="conditional-expressions-ifthenelse"></a>Expressions conditionnelles : `if...then...else`

Le `if...then...else` expression exécute différentes branches de code et qui prend une valeur différente selon l’expression booléenne donnée.

## <a name="syntax"></a>Syntaxe

```fsharp
if boolean-expression then expression1 [ else expression2 ]
```

## <a name="remarks"></a>Notes

Dans la syntaxe précédente, *expression1* s’exécute lorsque l’expression booléenne prend la valeur `true`; sinon, *expression2* s’exécute.

Contrairement à d’autres langages, le `if...then...else` construction est une expression, pas une instruction. Cela signifie qu’il génère une valeur, ce qui est la valeur de la dernière expression dans la branche qui s’exécute. Les types des valeurs produites dans chaque branche doivent correspondre. S’il existe non explicite `else` , son type est `unit`. Par conséquent, si le type de la `then` branche est d’un type autre que `unit`, il doit y avoir un `else` branche avec le même type de retour. Lors du chaînage `if...then...else` des expressions, vous pouvez utiliser le mot clé `elif` au lieu de `else if`; ils sont équivalents.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser le `if...then...else` expression.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4501.fs)]

```
10 is less than 20
What is your name? John
How old are you? 9
You are only 9 years old and already learning F#? Wow!
```

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
