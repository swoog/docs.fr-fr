---
title: Abréviations de types (F#)
description: 'Découvrez les abréviations de type F # pour donner un nom plus significatif à un type afin de faciliter la lecture du code.'
ms.date: 05/16/2016
ms.openlocfilehash: 259cd6c84e22fc7c98e08255d3e0ded5b87af352
ms.sourcegitcommit: 67de6cb5dd66a19f2180ba7e4d7aecc697f8a963
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44336470"
---
# <a name="type-abbreviations"></a>Abréviations de types

Un *abréviation de type* est un alias ou un autre nom pour un type.

## <a name="syntax"></a>Syntaxe

```fsharp
type [accessibility-modifier] type-abbreviation = type-name
```

## <a name="remarks"></a>Notes

Vous pouvez utiliser les abréviations de type pour donner un nom plus explicite, à un type afin de faciliter la lecture du code. Vous pouvez également les utiliser pour créer un nom facile à utiliser pour un type fastidieux à écrire. En outre, vous pouvez utiliser les abréviations de type pour le rendre plus facile de modifier un type sous-jacent sans modifier tout le code qui utilise le type. Voici une abréviation de type simple.

Accessibilité des abréviations de types valeur par défaut est `public`.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2301.fs)]

Abréviations de types peuvent inclure des paramètres génériques, comme dans le code suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2302.fs)]

Dans le code précédent, `Transform` est une abréviation de type qui représente une fonction qui accepte un argument unique de n’importe quel type et qui retourne une valeur unique du même type.

Abréviations de types ne sont pas conservées dans le code MSIL .NET Framework. Par conséquent, lorsque vous utilisez un assembly F # à partir d’un autre langage .NET Framework, vous devez utiliser le nom de type sous-jacent pour une abréviation de type.

Abréviations de type peuvent également servir sur des unités de mesure. Pour plus d’informations, consultez [unités](units-of-measure.md).

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
