---
title: Types flexibles (F#)
description: 'Découvrez comment utiliser F # annotation de type flexible, ce qui indique qu’un paramètre, une variable ou une valeur a un type qui est compatible avec un type spécifié.'
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: bee2364a6c30b1fbdc09aa0aac2249e3f0c295e8
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="flexible-types"></a>Types flexibles

A *annotation de type flexible* indique qu’un paramètre, une variable ou une valeur a un type qui est compatible avec un type spécifié, où la compatibilité est déterminée par la position dans une hiérarchie orientée objet de classes ou des interfaces. Types flexibles sont particulièrement utiles lorsque la conversion automatique en types de niveau supérieurs dans la hiérarchie des types ne se produit pas, mais vous souhaitez activer votre fonctionnalité de fonctionner avec n’importe quel type dans la hiérarchie ou n’importe quel type qui implémente une interface.

## <a name="syntax"></a>Syntaxe

```fsharp
#type
```

## <a name="remarks"></a>Notes

Dans la syntaxe précédente, *type* représente un type de base ou une interface.

Un type flexible équivaut à un type générique qui a une contrainte qui limite les types autorisés en types compatibles avec le type de base ou interface. Autrement dit, les deux lignes de code suivantes sont équivalentes.

```fsharp
#SomeType

'T when 'T :> SomeType
```

Types flexibles sont utiles dans plusieurs types de situations. Par exemple, lorsque vous disposez d’une fonction d’ordre supérieur (une fonction qui accepte une fonction en tant qu’argument), il est souvent utile de disposer de la fonction retourne un type flexible. Dans l’exemple suivant, l’utilisation d’un type flexible avec un argument de séquence dans `iterate2` permet à la fonction d’ordre supérieure d’utiliser des fonctions qui génèrent des séquences, tableaux, listes et autres types énumérables.

Considérez les deux fonctions suivantes, une retourne une séquence, l’autre qui retourne un type flexible.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4101.fs)]

Comme autre exemple, prenez le [Seq.concat](https://msdn.microsoft.com/library/2eeb69a9-fc2f-4b7d-8dee-101fa2b00712) fonction de bibliothèque :

```fsharp
val concat: sequences:seq<#seq<'T>> -> seq<'T>
```

Vous pouvez passer les séquences énumérables suivantes à cette fonction :

- Une liste de listes
- Une liste de tableaux
- Un tableau de listes
- Un tableau de séquences
- Toute autre combinaison de séquences énumérables

Le code suivant utilise `Seq.concat` pour montrer les scénarios que vous pouvez prendre en charge à l’aide de types flexibles.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4102.fs)]

La sortie est la suivante.

```
seq [1; 2; 3; 4; ...]
seq [1; 2; 3; 4; ...]
seq [1; 2; 3; 4; ...]
seq [1; 2; 3; 4; ...]
seq [1; 2; 3; 4; ...]
```

En F #, comme dans d’autres langages orientés objet, sont les contextes dans lesquels les types dérivés ou les types qui implémentent les interfaces sont converties automatiquement en un type de base ou interface. Ces conversions automatiques se produisent dans les arguments directs, mais pas lorsque le type est dans une position subordonnée, dans le cadre d’un type plus complexe comme un type de retour d’un type de fonction, ou un argument de type. Par conséquent, la notation de type flexible est particulièrement utile lorsque le type que vous l’appliquez fait partie d’un type plus complexe.

## <a name="see-also"></a>Voir aussi

[Informations de référence du langage F#](index.md)

[Génériques](generics/index.md)
