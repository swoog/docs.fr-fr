---
title: 'Exceptions : fonction invalidArg (F#)'
description: "Découvrez comment la fonction 'invalidArg' F # génère une exception d’argument."
ms.date: 05/16/2016
ms.openlocfilehash: 8bf65fae9392a88205e3cdec8b7d7a3ff42f8416
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43798176"
---
# <a name="exceptions-the-invalidarg-function"></a>Exceptions : fonction invalidArg

Le `invalidArg` fonction génère une exception d’argument.

## <a name="syntax"></a>Syntaxe

```fsharp
invalidArg parameter-name error-message-string
```

## <a name="remarks"></a>Notes

Le nom de paramètre dans la syntaxe précédente est une chaîne avec le nom du paramètre dont l’argument n’est pas valide. Le *chaîne du message d’erreur* est une chaîne littérale ou une valeur de type `string`. Il devient le `Message` propriété de l’objet exception.

L’exception générée par `invalidArg` est un `System.ArgumentException` exception. Le code suivant illustre l’utilisation de `invalidArg` pour lever une exception.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet6101.fs)]

La sortie est la suivante, suivie d’une trace de pile (non illustrée).

```
December
January
System.ArgumentException: Month parameter out of range.
```

## <a name="see-also"></a>Voir aussi

- [Gestion des exceptions](index.md)
- [Types d'exceptions](exception-types.md)
- [Exceptions : expression `try...with`](the-try-with-expression.md)
- [Exceptions : expression `try...finally`](the-try-finally-expression.md)
- [Exceptions : fonction `raise`](the-raise-function.md)
- [Exceptions : fonction `failwith`](the-failwith-function.md)
