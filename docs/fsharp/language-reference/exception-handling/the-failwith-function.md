---
title: 'Exceptions : fonction failwith (F#)'
description: Découvrez comment la fonction « failwith » génère une exception F#.
ms.date: 05/16/2016
ms.openlocfilehash: 69a2eb69e0157d3bde8cb8884cb0ae960634dddc
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "43863427"
---
# <a name="exceptions-the-failwith-function"></a>Exceptions : fonction failwith

Le `failwith` fonction génère une exception F#.

## <a name="syntax"></a>Syntaxe

```fsharp
failwith error-message-string
```

## <a name="remarks"></a>Notes

Le *chaîne du message d’erreur* dans la syntaxe précédente est une chaîne littérale ou une valeur de type `string`. Il devient le `Message` propriété de l’exception.

L’exception qui est générée par `failwith` est un `System.Exception` exception, ce qui est une référence qui porte le nom `Failure` dans le code F#. Le code suivant illustre l’utilisation de `failwith` pour lever une exception.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet6001.fs)]

## <a name="see-also"></a>Voir aussi

- [Gestion des exceptions](index.md)
- [Types d'exceptions](exception-types.md)
- [Exceptions : expression `try...with`](the-try-with-expression.md)
- [Exceptions : expression `try...finally`](the-try-finally-expression.md)
- [Exceptions : fonction `raise`](the-raise-function.md)
