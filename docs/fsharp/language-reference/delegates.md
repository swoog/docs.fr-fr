---
title: Délégués
description: Découvrez comment utiliser des délégués F#.
ms.date: 05/16/2016
ms.openlocfilehash: 772685488b7caef92123979d817929c631248afb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61766075"
---
# <a name="delegates"></a>Délégués

Un délégué représente un appel de fonction en tant qu’objet. Dans F#, vous devez normalement utiliser les valeurs de fonction pour représenter des fonctions comme valeurs de première classe ; Toutefois, les délégués sont utilisés dans le .NET Framework et sont donc nécessaires lorsque vous interagissez avec les API qui attendent les. Ils peuvent également être utilisés lors de la création de bibliothèques conçues pour utiliser d’autres langages .NET Framework.

## <a name="syntax"></a>Syntaxe

```fsharp
type delegate-typename = delegate of type1 -> type2
```

## <a name="remarks"></a>Notes

Dans la syntaxe précédente, `type1` représente le type d’argument ou les types et `type2` représente le type de retour. Les types d’arguments qui sont représentées par `type1` sont automatiquement curryfiés. Cela suggère que pour ce type que vous utilisez une forme de tuple si les arguments de la fonction cible sont curryfiés et un tuple entre parenthèses pour les arguments qui sont déjà sous la forme de tuple. La curryfication automatique supprime un jeu de parenthèses, laissant un argument de tuple qui correspond à la méthode cible. Consultez l’exemple de code pour la syntaxe à utiliser dans chaque cas.

Les délégués peuvent être attachés à F# statiques et les valeurs de fonction ou de méthodes d’instance. F#les valeurs de fonction peuvent être passées directement en tant qu’arguments à déléguer des constructeurs. Pour une méthode statique, vous construisez le délégué en utilisant le nom de la classe et la méthode. Pour une méthode d’instance, vous fournissez l’instance d’objet et la méthode dans un seul argument. Dans les deux cas, opérateur d’accès au membre (`.`) est utilisé.

Le `Invoke` méthode sur le type délégué appelle la fonction encapsulée. En outre, les délégués peuvent être passés en tant que valeurs de fonction en référençant le nom de la méthode Invoke sans les parenthèses.

Le code suivant montre la syntaxe pour créer des délégués qui représentent les différentes méthodes dans une classe. Selon si la méthode est une méthode statique ou une méthode d’instance, et s’il comporte des arguments sous la forme de tuple ou de la forme curryfiée, la syntaxe pour déclarer et affecter le délégué est un peu différente.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4201.fs)]

Le code suivant montre certains des différents modes, que vous pouvez travailler avec les délégués.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4202.fs)]

La sortie de l’exemple de code précédent est comme suit.

```console
aaaaa
bbbbb
ccccc
[|"aaa"; "bbb"|]
```

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Paramètres et arguments](parameters-and-arguments.md)
- [Événements](members/events.md)