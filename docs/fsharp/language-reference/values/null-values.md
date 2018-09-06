---
title: Valeurs Null (F#)
description: 'Découvrez comment la valeur null est utilisée dans le langage de programmation F #.'
ms.date: 05/16/2016
ms.openlocfilehash: 8751ac402c43ddb07fb62e08b6c6d5403cbe9acc
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43787896"
---
# <a name="null-values"></a>Valeurs Null

Cette rubrique décrit l’utilisation de la valeur null en F #.

## <a name="null-value"></a>Valeur null

La valeur null n’est pas normalement utilisée en F # pour les valeurs ou des variables. Toutefois, null apparaît comme une valeur anormale dans certaines situations. Si un type est défini en F #, valeur null n’est pas autorisée comme valeur normale, sauf si le [AllowNullLiteral](https://msdn.microsoft.com/library/4f315196-f444-4cca-ba07-1176ff71eb0f) attribut est appliqué au type. Si un type est défini dans un autre langage .NET, null est une valeur possible, et lorsque vous interagissez avec ces types, votre code F # peut rencontrer des valeurs null.

Pour un type défini en F # et utilisé strictement à partir de F #, la seule façon de créer une valeur null à l’aide de la bibliothèque F # directement consiste à utiliser [Unchecked.defaultof](https://msdn.microsoft.com/library/9ff97f2a-1bd4-4f4c-afbe-5886a74ab977) ou [Array.zeroCreate](https://msdn.microsoft.com/library/fa5b8e7a-1b5b-411c-8622-b58d7a14d3b2). Toutefois, pour un type F # qui est utilisé à partir d’autres langages .NET, ou si vous utilisez ce type avec une API qui n’est pas écrite en F #, tels que le .NET Framework, les valeurs null peuvent se produire.

Vous pouvez utiliser la `option` type en F # lorsque vous utilisez une variable de référence avec une valeur null possible dans un autre langage .NET. Au lieu de null, avec F # `option` type, vous utilisez la valeur de l’option `None` s’il n’existe aucun objet. Vous utilisez la valeur de l’option `Some(obj)` avec un objet `obj` lorsqu’il existe un objet. Pour plus d’informations, consultez [Options](../options.md).

Le `null` mot clé est un mot clé valide dans le langage F #, et vous devez l’utiliser lorsque vous travaillez avec des API .NET Framework ou d’autres API qui est écrits dans un autre langage .NET. Les deux situations dans lesquelles vous devrez peut-être une valeur null sont lorsque vous appelez une API .NET et que vous passez une valeur null en tant qu’argument, et lorsque vous interprétez la valeur de retour ou paramètre de sortie d’un appel de méthode .NET.

Pour passer une valeur null à une méthode .NET, utilisez simplement le `null` mot clé dans le code appelant. L'exemple de code suivant illustre ceci.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet701.fs)]

Pour interpréter une valeur null est obtenue à partir d’une méthode .NET, utiliser les critères spéciaux si vous le pouvez. L’exemple de code suivant montre comment utiliser les critères spéciaux pour interpréter la valeur null est retournée à partir de `ReadLine` quand il tente de lire au-delà de la fin d’un flux d’entrée.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet702.fs)]

Valeurs NULL pour les types F # peuvent également être générées d’autres manières, comme lorsque vous utilisez `Array.zeroCreate`, qui appelle `Unchecked.defaultof`. Vous devez être prudent avec ce code pour conserver les valeurs null encapsulées. Dans une bibliothèque destinée uniquement à F #, il est inutile vérifier les valeurs null dans chaque fonction. Si vous écrivez une bibliothèque pour l’interopérabilité avec d’autres langages .NET, vous devrez peut-être ajouter des paramètres d’entrée de vérifications pour la valeur null et levant une `ArgumentNullException`, tout comme vous le feriez dans le code c# ou Visual Basic.

Vous pouvez utiliser le code suivant pour vérifier si une valeur arbitraire est null.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet703.fs)]

## <a name="see-also"></a>Voir aussi

- [Valeurs](index.md)
- [Expressions match](../match-expressions.md)
