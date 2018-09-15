---
title: Types flexibles (F#)
description: 'Découvrez comment utiliser F # annotation de type flexible, ce qui indique qu’un paramètre, une variable ou une valeur a un type qui est compatible avec un type spécifié.'
ms.date: 05/16/2016
ms.openlocfilehash: b6c97c3cc19f15b2c8db74b2c55660a16b2858f7
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2018
ms.locfileid: "45615558"
---
# <a name="flexible-types"></a>Types flexibles

Un *annotation de type flexible* indique qu’un paramètre, une variable ou une valeur a un type qui est compatible avec un type spécifié, où la compatibilité est déterminée par la position dans une hiérarchie orientée objet de classes ou interfaces. Types flexibles sont particulièrement utiles lorsque la conversion automatique en types plus hauts dans la hiérarchie de type ne se produit pas, mais vous souhaitez toujours activer votre fonctionnalité de fonctionner avec n’importe quel type dans la hiérarchie ou n’importe quel type qui implémente une interface.

## <a name="syntax"></a>Syntaxe

```fsharp
#type
```

## <a name="remarks"></a>Notes

Dans la syntaxe précédente, *type* représente un type de base ou une interface.

Un type flexible est équivalent à un type générique qui a une contrainte qui limite les types autorisés pour les types qui sont compatibles avec le type de base ou interface. Autrement dit, les deux lignes de code suivantes sont équivalentes.

```fsharp
#SomeType

'T when 'T :> SomeType
```

Types flexibles sont utiles dans plusieurs types de situations. Par exemple, lorsque vous avez une fonction d’ordre supérieur (une fonction qui accepte une fonction comme argument), il est souvent utile d’avoir la fonction retourne un type flexible. Dans l’exemple suivant, l’utilisation d’un type flexible avec un argument de séquence dans `iterate2` permet à la fonction d’ordre plus élevée travailler avec des fonctions qui génèrent des séquences, tableaux, listes et autres types énumérables.

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

En F #, comme dans d’autres langages orientés objet, il existe les contextes dans lequel types dérivés ou des types qui implémentent les interfaces sont automatiquement convertis en un type de base ou d’un type d’interface. Ces conversions automatiques se produisent dans les arguments directs, mais pas lorsque le type est dans une position subordonnée, dans le cadre d’un type plus complexe comme un type de retour d’un type de fonction, ou un argument de type. Par conséquent, la notation de type flexible est particulièrement utile lorsque le type que vous l’appliquez fait partie d’un type plus complexe.

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Génériques](generics/index.md)
