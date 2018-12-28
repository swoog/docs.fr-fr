---
title: Valeurs Null
description: Découvrez comment la valeur null est utilisée dans le F# langage de programmation.
ms.date: 05/16/2016
ms.openlocfilehash: 58c54065a98a84c4d4e912cbc42d59cfea8c6de1
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53610994"
---
# <a name="null-values"></a>Valeurs Null

Cette rubrique décrit la façon dont la valeur null est utilisée dans F#.

## <a name="null-value"></a>Valeur null

La valeur null n’est pas utilisée normalement dans F# des valeurs ou des variables. Toutefois, null apparaît comme une valeur anormale dans certaines situations. Si un type est défini dans F#, null n’est pas autorisée comme valeur normale, sauf si le [AllowNullLiteral](https://msdn.microsoft.com/library/4f315196-f444-4cca-ba07-1176ff71eb0f) attribut est appliqué au type. Si un type est défini dans un autre langage .NET, null est une valeur possible, et lorsque vous interagissez avec ces types, votre F# code peut rencontrer des valeurs null.

Pour un type défini dans F# et utilisé strictement à partir de F#, la seule façon pour créer une valeur null à l’aide de la F# bibliothèque directement consiste à utiliser [Unchecked.defaultof](https://msdn.microsoft.com/library/9ff97f2a-1bd4-4f4c-afbe-5886a74ab977) ou [Array.zeroCreate](https://msdn.microsoft.com/library/fa5b8e7a-1b5b-411c-8622-b58d7a14d3b2). Toutefois, pour un F# type qui est utilisé à partir d’autres langages .NET, ou si vous utilisez ce type avec une API qui n’est pas écrite dans F#, tels que le .NET Framework, les valeurs null peuvent se produire.

Vous pouvez utiliser la `option` tapez F# lorsque vous utilisez peut-être une variable de référence avec une valeur null possible dans un autre langage .NET. Au lieu de null, avec un F# `option` type, vous utilisez la valeur de l’option `None` s’il n’existe aucun objet. Vous utilisez la valeur de l’option `Some(obj)` avec un objet `obj` lorsqu’il existe un objet. Pour plus d’informations, consultez [Options](../options.md).

Le `null` mot clé est un mot clé valide dans le F# langue et vous devez l’utiliser lorsque vous travaillez avec des API .NET Framework ou d’autres API qui est écrits dans un autre langage .NET. Les deux situations dans lesquelles vous devrez peut-être une valeur null sont lorsque vous appelez une API .NET et que vous passez une valeur null en tant qu’argument, et lorsque vous interprétez la valeur de retour ou paramètre de sortie d’un appel de méthode .NET.

Pour passer une valeur null à une méthode .NET, utilisez simplement le `null` mot clé dans le code appelant. L'exemple de code suivant illustre ceci.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet701.fs)]

Pour interpréter une valeur null est obtenue à partir d’une méthode .NET, utiliser les critères spéciaux si vous le pouvez. L’exemple de code suivant montre comment utiliser les critères spéciaux pour interpréter la valeur null est retournée à partir de `ReadLine` quand il tente de lire au-delà de la fin d’un flux d’entrée.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet702.fs)]

Valeurs null F# types peuvent également être générés dans d’autres méthodes, comme lorsque vous utilisez `Array.zeroCreate`, qui appelle `Unchecked.defaultof`. Vous devez être prudent avec ce code pour conserver les valeurs null encapsulées. Dans une bibliothèque destinée uniquement au F#, vous n’êtes pas obligé de vérifier les valeurs null dans chaque fonction. Si vous écrivez une bibliothèque pour l’interopérabilité avec d’autres langages .NET, vous devrez peut-être ajouter des paramètres d’entrée de vérifications pour la valeur null et levant une `ArgumentNullException`, tout comme vous le feriez dans le code c# ou Visual Basic.

Vous pouvez utiliser le code suivant pour vérifier si une valeur arbitraire est null.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet703.fs)]

## <a name="see-also"></a>Voir aussi

- [Valeurs](index.md)
- [Expressions match](../match-expressions.md)