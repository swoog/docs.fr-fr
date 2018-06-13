---
title: 'Expressions conditionnelles : if... then...else (F#)'
description: 'Découvrez comment écrire des expressions conditionnelles en F # pour exécuter les différentes branches de code.'
ms.date: 05/16/2016
ms.openlocfilehash: a3ca3c20a659ccf5dc432d0a747ff176ec889e9d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33563131"
---
# <a name="conditional-expressions-ifthenelse"></a>Expressions conditionnelles : `if...then...else`

Le `if...then...else` expression exécute différentes branches de code et prend une valeur différente selon l’expression booléenne donnée.


## <a name="syntax"></a>Syntaxe

```fsharp
if boolean-expression then expression1 [ else expression2 ]
```

## <a name="remarks"></a>Notes
Dans la syntaxe précédente, *expression1* s’exécute lorsque l’expression booléenne renvoie `true`; sinon, *expression2* s’exécute.

Contrairement à d’autres langages, les `if...then...else` construction est une expression, pas une instruction. Cela signifie qu’il génère une valeur, ce qui est la valeur de la dernière expression dans la branche qui s’exécute. Les types des valeurs produites dans chaque branche doivent correspondre. S’il existe n’explicite `else` , son type est `unit`. Par conséquent, si le type de la `then` branche est d’un type autre que `unit`, il doit y avoir un `else` branche avec le même type de retour. Lors du chaînage `if...then...else` expressions ensemble, vous pouvez utiliser le mot clé `elif` au lieu de `else if`; ils sont équivalents.

## <a name="example"></a>Exemple
L’exemple suivant illustre comment utiliser le `if...then...else` expression.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4501.fs)]

```
10 is less than 20
What is your name? John
How old are you? 9
You are only 9 years old and already learning F#? Wow!
```

## <a name="see-also"></a>Voir aussi
[Informations de référence du langage F#](index.md)

