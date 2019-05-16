---
title: 'Exceptions : invalidArg (fonction)'
description: Découvrez comment la F# « invalidArg » fonction génère une exception d’argument.
ms.date: 05/16/2016
ms.openlocfilehash: 1f0cbc9b7e805822544d6d54bc1fc69adf82967a
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65645499"
---
# <a name="exceptions-the-invalidarg-function"></a>Exceptions : invalidArg (fonction)

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
- [Exceptions : Le `try...with` Expression](the-try-with-expression.md)
- [Exceptions : Le `try...finally` Expression](the-try-finally-expression.md)
- [Exceptions : fonction `raise`](the-raise-function.md)
- [Exceptions : Le `failwith` (fonction)](the-failwith-function.md)
