---
title: Abréviations de types (F#)
description: 'Découvrez les abréviations de type F # pour donner un nom plus significatif à un type afin de rendre le code plus facile à lire.'
ms.date: 05/16/2016
ms.openlocfilehash: cd0b2365aecc5d5b73df95a4b94ae4dd8327446d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="type-abbreviations"></a>Abréviations de types

A *abréviation de type* est un alias ou un autre nom pour un type.

## <a name="syntax"></a>Syntaxe

```fsharp
type type-abbreviation = type-name
```

## <a name="remarks"></a>Notes
Vous pouvez utiliser les abréviations de type pour donner un nom plus significatif, à un type afin de rendre le code plus facile à lire. Vous pouvez également les utiliser pour créer un nom facile à utiliser pour un type fastidieux à écrire. En outre, vous pouvez utiliser les abréviations de type pour le rendre plus facile de modifier un type sous-jacent sans modifier tout code qui utilise le type. Voici une abréviation de type simple.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2301.fs)]

Les abréviations de type peuvent inclure des paramètres génériques, comme dans le code suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2302.fs)]

Dans le code précédent, `Transform` est une abréviation de type représentant une fonction qui accepte un argument unique de n’importe quel type et qui retourne une valeur unique du même type.

Les abréviations de type ne sont pas conservées dans le code MSIL .NET Framework. Par conséquent, lorsque vous utilisez un assembly F # à partir d’un autre langage .NET Framework, vous devez utiliser le nom du type sous-jacent pour une abréviation de type.

Les abréviations de type peuvent également servir dans les unités de mesure. Pour plus d’informations, consultez [unités](units-of-measure.md).


## <a name="see-also"></a>Voir aussi
[Informations de référence du langage F#](index.md)

