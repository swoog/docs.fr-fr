---
title: Propriétés indexées (F#)
description: 'En savoir plus sur les propriétés indexées F #, qui sont des propriétés qui fournissent un accès de type tableau aux données classées.'
ms.date: 05/16/2016
ms.openlocfilehash: e56e4e2ea3f35df4c8ec46012357242cb6ce69f3
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "45994258"
---
# <a name="indexed-properties"></a>Propriétés indexées

*Propriétés indexées* propriétés qui fournissent un accès de type tableau aux sont classées les données. Ils se présentent sous trois formes :

* `Item`
* `Ordinal`
* `Cardinal`

Un membre F # doit être nommé un de ces trois noms pour fournir un accès de type tableau. `IndexerName` est utilisé pour représenter l’un des trois options ci-dessous :

## <a name="syntax"></a>Syntaxe

```fsharp
// Indexed property that has both get and set defined.
member self-identifier.IndexerName
    with get(index-variable) =
        get-function-body
    and set index-variablesvalue-variables =
        set-function-body

// Indexed property that has get only.
member self-identifier.IndexerName(index-variable) =
    get-function-body

// Alternative syntax for indexed property with get only
member self-identifier.IndexerName
    with get(index-variables) =
        get-function-body

// Indexed property that has set only.
member self-identifier.IndexerName
    with set index-variablesvalue-variables = 
        set-function-body
```

## <a name="remarks"></a>Notes

Les formes de la syntaxe précédente montrent comment définir des propriétés indexées qui ont les deux un `get` et un `set` (méthode), ont un `get` méthode uniquement, ou avoir un `set` méthode uniquement. Vous pouvez également combiner les deux la syntaxe indiquée pour get uniquement et la syntaxe indiquée pour set uniquement et produire une propriété qui possède à la fois get et set. Cette dernière forme vous permet de placer des modificateurs d’accessibilité différente et des attributs sur la méthode get et de définir des méthodes.

Lorsque le *IndexerName* est `Item`, le compilateur traite la propriété comme une propriété indexée par défaut. Un *propriété indexée par défaut* est une propriété que vous pouvez accéder à l’aide de la syntaxe de type tableau sur l’instance d’objet. Par exemple, si `obj` est un objet du type qui définit cette propriété, la syntaxe `obj.[index]` est utilisé pour accéder à la propriété.

La syntaxe pour l’accès à une propriété indexée par défaut consiste à fournir le nom de la propriété et l’index entre parenthèses. Par exemple, si la propriété est `Ordinal`, vous écrivez `obj.Ordinal(index)` pour y accéder.

Quelle que soit la forme que vous utilisez, vous devez toujours utiliser la forme curryfiée pour la `set` méthode sur une propriété indexée. Pour plus d’informations sur les fonctions curryfiées, consultez [fonctions](../functions/index.md).

## <a name="example"></a>Exemple

L’exemple de code suivant illustre la définition et l’utilisation de la valeur par défaut et les propriétés indexées par défaut qui ont get et définir des méthodes.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3301.fs)]

## <a name="output"></a>Sortie

```
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
