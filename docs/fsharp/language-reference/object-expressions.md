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
# <a name="object-expressions"></a><span data-ttu-id="57acf-103">Expressions d'objet</span><span class="sxs-lookup"><span data-stu-id="57acf-103">Object Expressions</span></span>

<span data-ttu-id="57acf-104">Un *objet expression* est une expression qui crée une nouvelle instance d’un type d’objet créé dynamiquement, anonyme qui est basée sur un type existant de base, une interface ou un ensemble d’interfaces.</span><span class="sxs-lookup"><span data-stu-id="57acf-104">An *object expression* is an expression that creates a new instance of a dynamically created, anonymous object type that is based on an existing base type, interface, or set of interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="57acf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57acf-105">Syntax</span></span>

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

## <a name="remarks"></a><span data-ttu-id="57acf-106">Notes</span><span class="sxs-lookup"><span data-stu-id="57acf-106">Remarks</span></span>

<span data-ttu-id="57acf-107">Dans la syntaxe précédente, le *typename* représente un type de classe existant ou un type d’interface.</span><span class="sxs-lookup"><span data-stu-id="57acf-107">In the previous syntax, the *typename* represents an existing class type or interface type.</span></span> <span data-ttu-id="57acf-108">*type-params* décrit les paramètres de type générique facultatifs.</span><span class="sxs-lookup"><span data-stu-id="57acf-108">*type-params* describes the optional generic type parameters.</span></span> <span data-ttu-id="57acf-109">Le *arguments* sont utilisés uniquement pour les types de classe, qui nécessitent des paramètres de constructeur.</span><span class="sxs-lookup"><span data-stu-id="57acf-109">The *arguments* are used only for class types, which require constructor parameters.</span></span> <span data-ttu-id="57acf-110">Le *-des définitions de membre* sont des remplacements des méthodes de classe de base ou des implémentations de méthodes abstraites d’une classe de base ou une interface.</span><span class="sxs-lookup"><span data-stu-id="57acf-110">The *member-definitions* are overrides of base class methods, or implementations of abstract methods from either a base class or an interface.</span></span>

<span data-ttu-id="57acf-111">L’exemple suivant illustre les différents types d’expressions d’objet.</span><span class="sxs-lookup"><span data-stu-id="57acf-111">The following example illustrates several different types of object expressions.</span></span>

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

## <a name="using-object-expressions"></a><span data-ttu-id="57acf-112">À l’aide d’Expressions d’objet</span><span class="sxs-lookup"><span data-stu-id="57acf-112">Using Object Expressions</span></span>

<span data-ttu-id="57acf-113">Vous utilisez des expressions d’objet lorsque vous souhaitez éviter le code supplémentaire et la surcharge qui est nécessaire pour créer un nouveau type nommé.</span><span class="sxs-lookup"><span data-stu-id="57acf-113">You use object expressions when you want to avoid the extra code and overhead that is required to create a new, named type.</span></span> <span data-ttu-id="57acf-114">Si vous utilisez des expressions d’objet pour réduire le nombre de types créés dans un programme, vous pouvez réduire le nombre de lignes de code et empêcher la prolifération inutile de types.</span><span class="sxs-lookup"><span data-stu-id="57acf-114">If you use object expressions to minimize the number of types created in a program, you can reduce the number of lines of code and prevent the unnecessary proliferation of types.</span></span> <span data-ttu-id="57acf-115">Au lieu de créer de nombreux types pour gérer des situations spécifiques seulement, vous pouvez utiliser une expression d’objet qui personnalise un type existant ou fournit une implémentation appropriée d’une interface pour le cas spécifique à portée de main.</span><span class="sxs-lookup"><span data-stu-id="57acf-115">Instead of creating many types just to handle specific situations, you can use an object expression that customizes an existing type or provides an appropriate implementation of an interface for the specific case at hand.</span></span>

## <a name="see-also"></a><span data-ttu-id="57acf-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57acf-116">See also</span></span>

- [<span data-ttu-id="57acf-117">Informations de référence sur le langage F#</span><span class="sxs-lookup"><span data-stu-id="57acf-117">F# Language Reference</span></span>](index.md)
