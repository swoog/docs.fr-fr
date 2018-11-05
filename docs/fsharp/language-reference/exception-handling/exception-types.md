---
title: Types d'exceptions (F#)
description: Découvrez comment définir et utiliser des types d’exception F#.
ms.date: 05/16/2016
ms.openlocfilehash: b8d648a3649153a3604856deb61ce41db8c40bf2
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "43858819"
---
# <a name="exception-types"></a>Types d'exceptions

Il existe deux catégories d’exceptions en F#: types d’exceptions .NET et les types d’exception F#. Cette rubrique décrit comment définir et utiliser des types d’exception F#.

## <a name="syntax"></a>Syntaxe

```fsharp
exception exception-type of argument-type
```

## <a name="remarks"></a>Notes

Dans la syntaxe précédente, *type d’exception* est le nom d’un type d’exception F# nouveau, et *type d’argument* représente le type d’un argument qui peut être fourni lorsque vous déclenchez une exception de ce type. Vous pouvez spécifier plusieurs arguments à l’aide d’un type de tuple pour *type d’argument*.

Une définition classique pour une exception F# ressemble à ce qui suit.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5501.fs)]

Vous pouvez générer une exception de ce type à l’aide de la `raise` de fonction, comme suit.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5502.fs)]

Vous pouvez utiliser un type d’exception F# directement dans les filtres dans un `try...with` expression, comme illustré dans l’exemple suivant.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5503.fs)]

Le type d’exception que vous définissez avec le `exception` mot-clé dans F# est un nouveau type qui hérite de `System.Exception`.

## <a name="see-also"></a>Voir aussi

- [Gestion des exceptions](index.md)
- [Exceptions : fonction `raise`](the-raise-function.md)
- [Hiérarchie des exceptions](https://msdn.microsoft.com/library/z4c5tckx.aspx)
