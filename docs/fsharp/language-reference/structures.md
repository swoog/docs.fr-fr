---
title: Structures
description: En savoir plus sur les F# structure, un type d’objet compact souvent plus efficace qu’une classe pour les types avec une petite quantité de données et un comportement simple.
ms.date: 05/16/2016
ms.openlocfilehash: c091dc91765d6e828426de21e9bc5f79bfdebc6c
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612151"
---
# <a name="structures"></a>Structures

Un *structure* est un type d’objet compact qui peut être plus efficace qu’une classe pour les types qui ont une petite quantité de données et un comportement simple.

## <a name="syntax"></a>Syntaxe

```fsharp
[ attributes ]
type [accessibility-modifier] type-name =
    struct
        type-definition-elements-and-members
    end
// or
[ attributes ]
[<StructAttribute>]
type [accessibility-modifier] type-name =
    type-definition-elements-and-members
```

## <a name="remarks"></a>Notes

Les structures sont *types valeur*, ce qui signifie qu’elles sont stockées directement sur la pile ou, lorsqu’ils sont utilisés en tant que champs ou les éléments de tableau, inline dans le parent de type. Contrairement aux classes et aux enregistrements, les structures ont une sémantique de passage par valeur. Cela signifie qu'elles sont principalement utilisées pour les petits volumes de données qui sont fréquemment sollicités et copiés.

Dans la syntaxe précédente, deux formes sont présentes. La première n'est pas la syntaxe simplifiée, mais elle est néanmoins fréquemment utilisée, car quand vous employez les mots clés `struct` et `end`, vous pouvez omettre l'attribut `StructAttribute` qui apparaît dans la seconde forme. Vous pouvez abréger `StructAttribute` en `Struct`.

Le *-definition-éléments-et-membres de type* dans la syntaxe précédente représente les définitions et déclarations de membre. Les structures peuvent avoir des constructeurs et des champs modifiables et non modifiables, et peuvent déclarer des membres et des implémentations d'interface. Pour plus d’informations, consultez [membres](members/index.md).

Les structures ne peuvent pas participer à l’héritage, ne peuvent pas contenir les liaisons `let` ou `do`, et ne peuvent pas comporter de manière récursive les champs de leur propre type (bien qu’elles puissent contenir des cellules de référence qui référencent leur propre type).

Étant donné que les structures n'autorisent pas les liaisons `let`, vous devez déclarer leurs champs à l'aide du mot clé `val`. Le mot clé `val` définit un champ et son type, mais n'autorise pas l'initialisation. À la place, les déclarations `val` sont initialisées à la valeur zéro ou null. Pour cette raison, les structures ayant un constructeur implicite (c'est-à-dire les paramètres qui sont fournis immédiatement après le nom de la structure dans la déclaration) requièrent que les déclarations `val` soient annotées avec l'attribut `DefaultValue`. Les structures ayant un constructeur défini prennent toujours en charge l'initialisation à zéro. Par conséquent, l'attribut `DefaultValue` est une déclaration selon laquelle une telle valeur égale à zéro est valide pour le champ. Les constructeurs implicites pour les structures n'exécutent aucune action, car les liaisons `let` et `do` ne sont pas autorisées sur le type, mais les valeurs de paramètre de constructeur implicite passées sont disponibles en tant que champs privés.

Les constructeurs explicites peuvent impliquer l'initialisation des valeurs de champ. Quand une structure a un constructeur explicite, elle prend toujours en charge l'initialisation à zéro ; toutefois, vous n'utilisez pas l'attribut `DefaultValue` sur les déclarations `val`, car il est en conflit avec le constructeur explicite. Pour plus d’informations sur `val` déclarations, consultez [champs explicites : Le `val` mot clé](members/explicit-fields-the-val-keyword.md).

Les attributs et les modificateurs d'accessibilité sont autorisés sur les structures et suivent les mêmes règles que celles des autres types. Pour plus d’informations, consultez [attributs](attributes.md) et [contrôle d’accès](access-control.md).

Les exemples de code suivants illustrent des définitions de structure.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2501.fs)]

## <a name="byreflike-structs"></a>Structures ByRefLike

Vous pouvez définir vos propres structs peuvent adhérer à `byref`-comme sémantique : consultez [ByRef](byrefs.md) pour plus d’informations. Cette opération est effectuée avec la <xref:System.Runtime.CompilerServices.IsByRefLikeAttribute> attribut :

```fsharp
open System
open System.Runtime.CompilerServices

[<IsByRefLike; Struct>]
type S(count1: Span<int>, count2: Span<int>) =
    member x.Count1 = count1
    member x.Count2 = count2
```

`IsByRefLike` n’implique pas `Struct`. Les deux doivent être présents sur le type.

Un «`byref`-comme « struct dans F# est un type de valeur de limite de la pile. Elle n’est jamais allouée sur le tas managé. Un `byref`-comme struct est utile pour la programmation de hautes performances, car elle est appliquée avec l’ensemble de vérifications fortes sur la durée de vie et de non capture. Les règles sont :

* Elles peuvent servir comme paramètres de fonction, les paramètres de méthode, les variables locales, méthode est retournée.
* Ils ne peuvent pas être statiques ou membres d’une classe ou un struct normal d’instance.
* Ils ne peuvent pas être capturés par n’importe quelle construction de fermeture (`async` méthodes ou expressions lambda).
* Ils ne peuvent pas être utilisés comme un paramètre générique.

Bien que ces règles limiter fortement l’utilisation, elles ne remplissent la promesse de l’informatique hautes performances de manière sécurisée.

## <a name="readonly-structs"></a>Structs en lecture seule

Vous pouvez annoter des structs avec le <xref:System.Runtime.CompilerServices.IsReadOnlyAttribute> attribut. Exemple :

```fsharp
[<IsReadOnly; Struct>]
type S(count1: int, count2: int) =
    member x.Count1 = count1
    member x.Count2 = count2
```

`IsReadOnly` n’implique pas `Struct`. Vous devez ajouter les deux avoir un `IsReadOnly` struct.

Utilisation de cet attribut émet vous permettant de métadonnées F# et C# savoir pour le traiter comme `inref<'T>` et `in ref`, respectivement.

Définition d’une valeur mutable à l’intérieur d’un struct en lecture seule génère une erreur.

## <a name="struct-records-and-discriminated-unions"></a>Enregistrements de struct et les Unions discriminées

Vous pouvez représenter [enregistrements](records.md) et [Unions discriminées](discriminated-unions.md) en tant que de structs avec le `[<Struct>]` attribut.  Consultez chaque article pour en savoir plus.

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Classes](classes.md)
- [Enregistrements](records.md)
- [Membres](members/index.md)