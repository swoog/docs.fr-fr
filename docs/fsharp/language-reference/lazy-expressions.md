---
title: Expressions différées
description: Découvrez comment F# expressions différées peuvent améliorer les performances de vos applications et les bibliothèques.
ms.date: 03/13/2019
ms.openlocfilehash: 6d53d53093f4e93f53e1c956b94e2f1e4a1bbd55
ms.sourcegitcommit: 69bf8b719d4c289eec7b45336d0b933dd7927841
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57853323"
---
# <a name="lazy-expressions"></a>Expressions différées

*Expressions différées* sont des expressions qui ne sont pas évaluées immédiatement, mais sont évaluées à la place lorsque le résultat est nécessaire. Cela peut contribuer à améliorer les performances de votre code.

## <a name="syntax"></a>Syntaxe

```fsharp
let identifier = lazy ( expression )
```

## <a name="remarks"></a>Notes

Dans la syntaxe précédente, *expression* est le code qui est évaluée uniquement lorsqu’un résultat est requis, et *identificateur* est une valeur qui stocke le résultat. La valeur est de type [ `Lazy<'T>` ](https://msdn.microsoft.com/library/b29d0af5-6efb-4a55-a278-2662a4ecc489), où le type réel qui est utilisé pour `'T` est déterminé à partir du résultat de l’expression.

Expressions différées permettent d’améliorer les performances en limitant l’exécution de des expressions aux seules situations dans lesquelles un résultat est nécessaire.

Pour forcer les expressions à effectuer, vous appelez la méthode `Force`. `Force` entraîne l’exécution à effectuer qu’une seule fois. Les appels suivants à `Force` retournent le même résultat, mais n’exécutent pas le code.

Le code suivant illustre l’utilisation d’expressions différées et l’utilisation de `Force`. Dans ce code, le type de `result` est `Lazy<int>`et le `Force` méthode retourne un `int`.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet73011.fs)]

L’évaluation différée, mais pas le `Lazy` type, est également utilisé pour les séquences. Pour plus d’informations, consultez [séquences](sequences.md).

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [LazyExtensions (module)](https://msdn.microsoft.com/library/86671f40-84a0-402a-867d-ae596218d948)
