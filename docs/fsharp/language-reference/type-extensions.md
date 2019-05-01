---
title: Extensions de type
description: Découvrez comment F# les extensions de type permettent d’ajouter de nouveaux membres à un type d’objet précédemment défini.
ms.date: 02/08/2019
ms.openlocfilehash: 69fb3b771b5334c5771f2ac75341b38c1dad5b90
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61982603"
---
# <a name="type-extensions"></a>Extensions de type

Extensions de type (également appelé _augmentations_) est une famille de fonctionnalités qui vous permettent d’ajouter de nouveaux membres à un type d’objet précédemment défini. Les trois fonctionnalités sont :

* Extensions de type intrinsèques
* Extensions de type facultatif
* Méthodes d’extension

Chacun peut être utilisé dans différents scénarios et a différents compromis.

## <a name="syntax"></a>Syntaxe

```fsharp
// Intrinsic and optional extensions
type typename with
    member self-identifier.member-name =
        body
    ...

// Extension methods
open System.Runtime.CompilerServices

[<Extension>]
type Extensions() =
    [static] member self-identifier.extension-name (ty: typename, [args]) =
        body
    ...
```

## <a name="intrinsic-type-extensions"></a>Extensions de type intrinsèques

Une extension de type intrinsèque est une extension de type qui étend un type défini par l’utilisateur.

Extensions de type intrinsèques doivent être définies dans le même fichier **et** dans le même espace de noms ou module en tant que le type de la société étend. N’importe quel autre définition les entraîne en cours [extensions de type facultatif](type-extensions.md#optional-type-extensions).

Extensions de type intrinsèques sont parfois un moyen plus clair de séparer les fonctionnalités de la déclaration de type. L’exemple suivant montre comment définir une extension de type intrinsèque :

```fsharp
namespace Example

type Variant =
    | Num of int
    | Str of string
  
module Variant =
    let print v =
        match v with
        | Num n -> printf "Num %d" n
        | Str s -> printf "Str %s" s

// Add a member to Variant as an extension
type Variant with
    member x.Print() = Variant.print x
```

À l’aide d’une extension de type vous permet de séparer les éléments suivants :

* La déclaration d’un `Variant` type
* Fonctionnalités pour imprimer la `Variant` classe selon sa « forme »
* Un moyen d’accéder à la fonctionnalité d’impression avec le style de l’objet `.`-notation

Il s’agit d’une alternative à la définition de tous les éléments en tant que membre sur `Variant`. Il n’est pas intrinsèquement une meilleure approche, mais il peut être une représentation plus claire de fonctionnalités dans certaines situations.

Extensions de type intrinsèques sont compilées en tant que membres du type augmenter, ils apparaissent sur le type lorsque le type est examiné par réflexion.

## <a name="optional-type-extensions"></a>Extensions de type facultatif

Une extension de type facultatif est une extension qui s’affiche à l’extérieur du module, espace de noms ou assembly du type étendu d’origine.

Extensions de type facultatives sont utiles pour l’extension d’un type que vous n’avez pas défini vous-même. Exemple :

```fsharp
module Extensions

open System.Collections.Generic

type IEnumerable<'T> with
    /// Repeat each element of the sequence n times
    member xs.RepeatElements(n: int) =
        seq {
            for x in xs do
                for i in 1 .. n do
                    yield x
        }
```

Vous pouvez désormais accéder `RepeatElements` comme s’il est membre de <xref:System.Collections.Generic.IEnumerable%601> tant que le `Extensions` module est ouvert dans l’étendue que vous utilisez.

Des extensions facultatives n’apparaissent pas sur le type étendu quand il est examiné par réflexion. Des extensions facultatives doivent être dans des modules, et ils sont uniquement dans la portée lorsque le module qui contient l’extension est ouvert ou dans la portée.

Membres d’extension facultatifs sont compilés en membres statiques pour lequel l’instance d’objet est passée implicitement comme premier paramètre. Toutefois, ils agissent comme si elles sont membres d’instance ou des membres statiques selon la façon dont elles sont déclarées.

Membres d’extension facultatifs sont également pas visibles par C# ou des consommateurs VB. Ils peuvent uniquement être consommés dans d’autres F# code.

## <a name="generic-limitation-of-intrinsic-and-optional-type-extensions"></a>Limitation générique des extensions de type intrinsèque et facultatifs

Il est possible de déclarer une extension de type sur un type générique, où la variable de type est contraint. L’exigence est que la contrainte de la déclaration de l’extension correspond à la contrainte du type déclaré.

Toutefois, même lorsque les contraintes sont mises en correspondance entre un type déclaré et une extension de type, il est possible pour une contrainte à être déduit par le corps d’un membre d’étendue qui impose des exigences différentes sur le paramètre de type que le type déclaré. Exemple :

```fsharp
open System.Collections.Generic

// NOT POSSIBLE AND FAILS TO COMPILE!
//
// The member 'Sum' has a different requirement on 'T than the type IEnumerable<'T>
type IEnumerable<'T> with
    member this.Sum() = Seq.sum this
```

Il n’existe aucun moyen pour obtenir ce code fonctionne avec une extension de type facultatif :

* En l’état, le `Sum` membre a une contrainte différente `'T` (`static member get_Zero` et `static member (+)`) à ce qui définit l’extension du type.
* Modification de l’extension de type pour avoir la même contrainte en tant que `Sum` n’est pas la contrainte définie sur `IEnumerable<'T>`.
* Modification `member this.Sum` à `member inline this.Sum` générera une erreur d’incompatibilité de contraintes de type.

Ce que vous souhaitez sont des méthodes statiques qui « flottant dans l’espace » et peuvent être présentés comme s’ils vous étendez un type. Il s’agit dans lequel les méthodes d’extension devient nécessaires.

## <a name="extension-methods"></a>Méthodes d’extension

Enfin, les méthodes d’extension (parfois appelé «C# membres d’extension de style ») peuvent être déclarés dans F# comme une méthode de membre statique sur une classe.

Méthodes d’extension sont utiles pour lorsque vous souhaitez définir des extensions sur un type générique qui contrainte la variable de type. Exemple :

```fsharp
namespace Extensions

open System.Runtime.CompilerServices

[<Extension>]
type IEnumerableExtensions() =
    [<Extension>]
    static member inline Sum(xs: IEnumerable<'T>) = Seq.sum xs
```

Lorsqu’il est utilisé, ce code sera faire apparaître comme si `Sum` est défini sur <xref:System.Collections.Generic.IEnumerable%601>, à condition que `Extensions` a été ouvert ou est dans la portée.

## <a name="other-remarks"></a>Autres remarques

Extensions de type ont également les attributs suivants :

* N’importe quel type accessible peut être étendu.
* Définissent des extensions de type intrinsèques et facultatif _n’importe quel_ type de membre, pas seulement méthodes. Par conséquent, les propriétés d’extension sont également possibles, par exemple.
* Le `self-identifier` jeton dans le [syntaxe](type-extensions.md#syntax) représente l’instance du type appelé, comme des membres ordinaires.
* Étendues peuvent être statiques ou membres d’instance.
* Les variables de type sur une extension de type doivent correspondre aux contraintes du type déclaré.

Les limitations suivantes existent également pour les extensions de type :

* Extensions de type ne prennent pas en charge les méthodes virtuelles ou abstraites.
* Extensions de type ne gèrent pas les méthodes override en tant que les augmentations.
* Extensions de type ne gèrent pas [paramètres résolus statiquement Type](generics/statically-resolved-type-parameters.md).
* Les extensions de Type facultatives ne gèrent pas les constructeurs en tant que les augmentations.
* Extensions de type ne peut pas être définies sur [abréviations de types](type-abbreviations.md).
* Extensions de type ne sont pas valides pour `byref<'T>` (même si elles peuvent être déclarées).
* Extensions de type ne sont pas valides pour les attributs (même si elles peuvent être déclarées).
* Vous pouvez définir des extensions qui surchargent les autres méthodes du même nom, mais la F# compilateur donne la préférence aux méthodes d’extension non s’il existe un appel ambigu.

Enfin, si plusieurs extensions de type intrinsèques existent pour un type, tous les membres doivent être uniques. Pour les extensions de type facultatif, les membres dans différentes extensions de type vers le même type peuvent avoir les mêmes noms. Erreurs d’ambiguïté se produisent uniquement si le code client ouvre deux portées différentes qui définissent les mêmes noms de membre.

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Membres](members/index.md)
