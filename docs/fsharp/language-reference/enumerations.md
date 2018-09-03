---
title: Énumérations (F#)
description: 'Découvrez comment utiliser les énumérations F # à la place de littéraux pour rendre votre code plus lisible et plus facile à gérer.'
ms.date: 05/16/2016
ms.openlocfilehash: b51df53caf2e193496cb3694c913cbae08f7eaf5
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43481706"
---
# <a name="enumerations"></a>Énumérations

*Énumérations*, également appelé *enums*,, sont des types intégraux où les étiquettes sont affectées à un sous-ensemble des valeurs. Vous pouvez les utiliser à la place de littéraux pour rendre le code plus lisible et plus facile à gérer.


## <a name="syntax"></a>Syntaxe

```fsharp
type enum-name =
| value1 = integer-literal1
| value2 = integer-literal2
...
```

## <a name="remarks"></a>Notes
Une énumération ressemble beaucoup à une union discriminée qui a des valeurs simples, à ceci près que les valeurs peuvent être spécifiées. Les valeurs sont généralement des entiers qui commencent à 0 ou 1, ou des entiers qui représentent des positions de bits. Si une énumération est destinée à représenter des positions de bits, vous devez également utiliser le [indicateurs](xref:System.FlagsAttribute) attribut.

Le type sous-jacent de l’énumération est déterminé à partir du littéral est utilisé, afin que, par exemple, vous pouvez utiliser des littéraux avec un suffixe, tel que `1u`, `2u`, et ainsi de suite, pour un entier non signé (`uint32`) type.

Lorsque vous faites référence aux valeurs nommées, vous devez utiliser le nom du type énumération lui-même en tant que qualificateur, autrement dit, `enum-name.value1`, pas seulement `value1`. Ce comportement est différent de celui des unions discriminées. Il s’agit, car les énumérations ont toujours la [RequireQualifiedAccess](https://msdn.microsoft.com/library/8b9b6ade-0471-4413-ac5d-638cd0de5f15) attribut.

Le code suivant montre la déclaration et l’utilisation d’une énumération.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2101.fs)]

Vous pouvez facilement convertir des énumérations au type sous-jacent à l’aide de l’opérateur approprié, comme indiqué dans le code suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2102.fs)]

Types énumérés peuvent avoir un des types sous-jacents suivants : `sbyte`, `byte`, `int16`, `uint16`, `int32`, `uint32`, `int64`, `uint16`, `uint64`, et `char`. Types énumération sont représentés dans le .NET Framework en tant que types qui sont héritées de `System.Enum`, qui à son tour est hérité de `System.ValueType`. Par conséquent, ils sont des types valeur qui sont trouvent sur la pile ou inline dans l’objet conteneur, et toute valeur du type sous-jacent est une valeur valide de l’énumération. Ceci est important lorsque les critères spéciaux sur l’énumération des valeurs, car vous devez fournir un modèle qui intercepte les valeurs sans nom.

Le `enum` fonction dans la bibliothèque F # peut servir à générer une valeur d’énumération, même une valeur autre que prédéfinis, valeurs nommées. Vous utilisez le `enum` fonctionnent comme suit.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2103.fs)]

La valeur par défaut `enum` fonction fonctionne avec le type `int32`. Par conséquent, il ne peut pas être utilisé avec les types d’énumération qui ont d’autres types sous-jacents. Au lieu de cela, utilisez ce qui suit.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2104.fs)]

En outre, les cas pour les enums sont toujours émis en tant que `public`. Il s’agit afin qu’ils s’intègrent avec c# et le reste de la plate-forme .NET.
    
## <a name="see-also"></a>Voir aussi
[Informations de référence du langage F#](index.md)

[Casts et conversions](casting-and-conversions.md)
