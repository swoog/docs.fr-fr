---
title: Expressions d'objet
description: Découvrez comment utiliser F# expressions d’objet lorsque vous souhaitez éviter le code supplémentaire et la surcharge requise pour créer un nouveau type nommé.
ms.date: 02/08/2019
ms.openlocfilehash: 63f2c1d7128721b7b8c744e4cf02d73c2a8b4a07
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59157845"
---
# <a name="object-expressions"></a>Expressions d'objet

Un *objet expression* est une expression qui crée une nouvelle instance d’un type d’objet créé dynamiquement, anonyme qui est basée sur un type existant de base, une interface ou un ensemble d’interfaces.

## <a name="syntax"></a>Syntaxe

```fsharp
// When typename is a class:
{ new typename [type-params]arguments with
    member-definitions
    [ additional-interface-definitions ]
}
// When typename is not a class:
{ new typename [generic-type-args] with
    member-definitions
    [ additional-interface-definitions ]
}
```

## <a name="remarks"></a>Notes

Dans la syntaxe précédente, le *typename* représente un type de classe existant ou un type d’interface. *type-params* décrit les paramètres de type générique facultatifs. Le *arguments* sont utilisés uniquement pour les types de classe, qui nécessitent des paramètres de constructeur. Le *-des définitions de membre* sont des remplacements des méthodes de classe de base ou des implémentations de méthodes abstraites d’une classe de base ou une interface.

L’exemple suivant illustre les différents types d’expressions d’objet.

```fsharp
// This object expression specifies a System.Object but overrides the
// ToString method.
let obj1 = { new System.Object() with member x.ToString() = "F#" }
printfn "%A" obj1

// This object expression implements the IFormattable interface.
let delimiter(delim1: string, delim2: string, value: string) =
    { new System.IFormattable with
        member x.ToString(format: string, provider: System.IFormatProvider) =
            if format = "D" then
                delim1 + value + delim2
            else
                value }

let obj2 = delimiter("{","}", "Bananas!");

printfn "%A" (System.String.Format("{0:D}", obj2))

// Define two interfaces
type IFirst =
  abstract F : unit -> unit
  abstract G : unit -> unit

type ISecond =
  inherit IFirst
  abstract H : unit -> unit
  abstract J : unit -> unit

// This object expression implements both interfaces.
let implementer() =
    { new ISecond with
        member this.H() = ()
        member this.J() = ()
      interface IFirst with
        member this.F() = ()
        member this.G() = () }
```

## <a name="using-object-expressions"></a>À l’aide d’Expressions d’objet

Vous utilisez des expressions d’objet lorsque vous souhaitez éviter le code supplémentaire et la surcharge qui est nécessaire pour créer un nouveau type nommé. Si vous utilisez des expressions d’objet pour réduire le nombre de types créés dans un programme, vous pouvez réduire le nombre de lignes de code et empêcher la prolifération inutile de types. Au lieu de créer de nombreux types pour gérer des situations spécifiques seulement, vous pouvez utiliser une expression d’objet qui personnalise un type existant ou fournit une implémentation appropriée d’une interface pour le cas spécifique à portée de main.

## <a name="see-also"></a>Voir aussi

- [Informations de référence sur le langage F#](index.md)
