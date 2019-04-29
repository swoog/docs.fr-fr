---
title: 'Exceptions : failwith (fonction)'
description: Découvrez comment la fonction « failwith » génère une F# exception.
ms.date: 05/16/2016
ms.openlocfilehash: 05d385ddfc98a910779a6f59949a7187c38f0812
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772682"
---
# <a name="exceptions-the-failwith-function"></a>Exceptions : failwith (fonction)

Le `failwith` fonction génère une F# exception.

## <a name="syntax"></a>Syntaxe

```fsharp
failwith error-message-string
```

## <a name="remarks"></a>Notes

Le *chaîne du message d’erreur* dans la syntaxe précédente est une chaîne littérale ou une valeur de type `string`. Il devient le `Message` propriété de l’exception.

L’exception qui est générée par `failwith` est un `System.Exception` exception, ce qui est une référence qui porte le nom `Failure` dans F# code. Le code suivant illustre l’utilisation de `failwith` pour lever une exception.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet6001.fs)]

## <a name="see-also"></a>Voir aussi

- [Gestion des exceptions](index.md)
- [Types d'exceptions](exception-types.md)
- [Exceptions : Le `try...with` Expression](the-try-with-expression.md)
- [Exceptions : Le `try...finally` Expression](the-try-finally-expression.md)
- [Exceptions : fonction `raise`](the-raise-function.md)