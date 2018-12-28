---
title: Propriétés indexées
description: En savoir plus sur les propriétés indexées dans F#, qui permettent l’accès de type tableau aux données ordonnées.
ms.date: 10/17/2018
ms.openlocfilehash: 3817290505339803814e981cd5408cd4df6bd283
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53611774"
---
# <a name="indexed-properties"></a>Propriétés indexées

Lorsque vous définissez une classe qui effectue l’abstraction sur le tri des données, il peut parfois être utile de fournir un accès indexé à ces données sans exposer l’implémentation sous-jacente. Cette opération est effectuée avec la `Index` membre.

## <a name="syntax"></a>Syntaxe

```fsharp
// Indexed property that has both get and set defined.
member self-identifier.Index
    with get(index-values) =
        get-member-body
    and set index-values values-to-set =
        set-member-body

// Indexed property with get only
member self-identifier.Index
    with get(index-values) =
        get-member-body

// Indexed property that has set only.
member self-identifier.Index
    with set index-values values-to-set =
        set-member-body
```

## <a name="remarks"></a>Notes

Les formes de la syntaxe précédente montrent comment définir des propriétés indexées qui ont les deux un `get` et un `set` (méthode), ont un `get` méthode uniquement, ou avoir un `set` méthode uniquement. Vous pouvez également combiner les deux la syntaxe indiquée pour get uniquement et la syntaxe indiquée pour set uniquement et produire une propriété qui possède à la fois get et set. Cette dernière forme vous permet de placer des modificateurs d’accessibilité différente et des attributs sur la méthode get et de définir des méthodes.

En utilisant le nom `Item`, le compilateur traite la propriété comme une propriété indexée par défaut. Un *propriété indexée par défaut* est une propriété que vous pouvez accéder à l’aide de la syntaxe de type tableau sur l’instance d’objet. Par exemple, si `o` est un objet du type qui définit cette propriété, la syntaxe `o.[index]` est utilisé pour accéder à la propriété.

La syntaxe permettant d’accéder à une propriété indexée par défaut consiste à fournir le nom de la propriété et l’index entre parenthèses, comme un membre régulier. Par exemple, si la propriété sur `o` est appelée `Ordinal`, vous écrivez `o.Ordinal(index)` pour y accéder.

Quelle que soit la forme que vous utilisez, vous devez toujours utiliser la forme curryfiée pour la méthode set sur une propriété indexée. Pour plus d’informations sur les fonctions curryfiées, consultez [fonctions](../functions/index.md).

## <a name="example"></a>Exemple

L’exemple de code suivant illustre la définition et l’utilisation de la valeur par défaut et les propriétés indexées par défaut qui ont get et définir des méthodes.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3301.fs)]

## <a name="output"></a>Sortie

```console
ONE two three four five six seven eight nine ten
ONE first two second three third four fourth five fifth six 6th
seven seventh eight eighth nine ninth ten tenth
```

## <a name="indexed-properties-with-multiple-index-variables"></a>Propriétés indexées avec plusieurs Variables d’Index

Propriétés indexées peuvent avoir plus d’une variable d’index. Dans ce cas, les variables sont séparées par des virgules lorsque la propriété est utilisée. La méthode set dans une telle propriété doit avoir deux arguments curryfiés, le premier d'entre eux est un tuple qui contient les clés et le second est la valeur définie.

Le code suivant illustre l’utilisation d’une propriété indexée avec plusieurs variables d’index.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3302.fs)]

## <a name="see-also"></a>Voir aussi

- [Membres](index.md)