---
title: Interfaces (F#)
description: Découvrez comment F# Interfaces spécifient des jeux de membres associés qui implémentent des autres classes.
ms.date: 05/16/2016
ms.openlocfilehash: 6d7f8ee9ea17d2294933f88577c30a96975ae5d4
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "47231438"
---
# <a name="interfaces"></a>Interfaces

*Interfaces* spécifient les jeux de membres connexes que d’autres classes implémentent.

## <a name="syntax"></a>Syntaxe

```fsharp
// Interface declaration:
[ attributes ]
type [accessibility-modifier] interface-name =
    [ interface ]     [ inherit base-interface-name ...]
    abstract member1 : [ argument-types1 -> ] return-type1
    abstract member2 : [ argument-types2 -> ] return-type2
    ...
[ end ]

// Implementing, inside a class type definition:
interface interface-name with
    member self-identifier.member1argument-list = method-body1
    member self-identifier.member2argument-list = method-body2

// Implementing, by using an object expression:
[ attributes ]
let class-name (argument-list) =
    { new interface-name with
        member self-identifier.member1argument-list = method-body1
        member self-identifier.member2argument-list = method-body2
        [ base-interface-definitions ]
    }
    member-list
```

## <a name="remarks"></a>Notes

Déclarations d’interface ressemblent aux déclarations de classe, à ceci près qu’aucun membre n’est implémentées. Au lieu de cela, tous les membres sont abstraits, comme indiqué par le mot clé `abstract`. Vous ne fournissez pas un corps de méthode pour les méthodes abstraites. Toutefois, vous pouvez fournir une implémentation par défaut en incluant une définition séparée du membre comme une méthode avec le `default` mot clé. Cela équivaut à la création d’une méthode virtuelle dans une classe de base dans d’autres langages .NET. Une telle méthode virtuelle peut être substituée dans les classes qui implémentent l’interface.

L’accessibilité par défaut pour les interfaces est `public`.

Vous pouvez éventuellement nommer chaque paramètre de méthode à l’aide de la syntaxe normale F# :

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet24032.fs)]

Dans l’exemple ci-dessus `ISprintable` exemple, le `Print` méthode a un paramètre unique du type `string` portant le nom `format`.

Il existe deux façons d’implémenter les interfaces : à l’aide d’expressions d’objet et à l’aide des types de classe. Dans les deux cas, l’expression de type ou un objet de classe fournit le corps de méthode pour les méthodes abstraites de l’interface. Les implémentations sont spécifiques à chaque type qui implémente l’interface. Par conséquent, les méthodes d’interface sur différents types peuvent différer entre eux.

Les mots clés `interface` et `end`, qui marquent le début et la fin de la définition, sont facultatifs lorsque vous utilisez la syntaxe simplifiée. Si vous n’utilisez pas ces mots clés, le compilateur tente de déduire si le type est une classe ou une interface en analysant les constructions que vous utilisez. Si vous définissez un membre ou que vous utilisez la syntaxe de la classe, le type est interprété comme une classe.

Style de codage .NET consiste à commencer à toutes les interfaces avec une majuscule `I`.

## <a name="implementing-interfaces-by-using-class-types"></a>Implémentation des Interfaces à l’aide de Types de classe

Vous pouvez implémenter une ou plusieurs interfaces dans un type de classe à l’aide de la `interface` mot clé, le nom de l’interface et le `with` mot clé, suivi par les définitions de membre d’interface, comme illustré dans le code suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2801.fs)]

Implémentations d’interface sont héritées, donc toutes les classes dérivées n’êtes pas obligé de les implémenter de nouveau.

## <a name="calling-interface-methods"></a>Appel de méthodes d’Interface

Méthodes d’interface peuvent être appelées uniquement par le biais de l’interface, non par le biais de n’importe quel objet du type qui implémente l’interface. Par conséquent, vous devrez peut-être un upcast vers le type d’interface à l’aide de la `:>` opérateur ou la `upcast` opérateur afin d’appeler ces méthodes.

Pour appeler la méthode d’interface lorsque vous avez un objet de type `SomeClass`, vous devez effectuer un upcast l’objet pour le type d’interface, comme indiqué dans le code suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2802.fs)]

Une alternative consiste à déclarer une méthode sur l’objet qui effectue un upcast et appelle la méthode d’interface, comme dans l’exemple suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2803.fs)]

## <a name="implementing-interfaces-by-using-object-expressions"></a>Implémentation des Interfaces à l’aide d’Expressions d’objet

Expressions d’objet fournissent une méthode rapide pour implémenter une interface. Elles sont utiles lorsque vous n’êtes pas obligé de créer un type nommé, et que vous souhaitez qu’un objet qui prend en charge les méthodes d’interface, sans méthodes supplémentaires. Une expression d’objet est illustrée dans le code suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2804.fs)]

## <a name="interface-inheritance"></a>Héritage de l'interface

Les interfaces peuvent hériter d’une ou plusieurs interfaces de base.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2805.fs)]

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Expressions d'objet](object-expressions.md)
- [Classes](classes.md)
