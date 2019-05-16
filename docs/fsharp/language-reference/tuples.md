---
title: Tuples
description: En savoir plus sur les F# tuple, un regroupement de valeurs sans nom, mais ordonnées, de types éventuellement différents.
ms.date: 05/16/2016
ms.openlocfilehash: 950451ad1672e0c9fc609773f1bc32fc13636ddb
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65645114"
---
# <a name="tuples"></a>Tuples

Un *tuple* est un regroupement de valeurs sans nom, mais ordonnées, de types éventuellement différents.  Tuples peut être des types référence ou les structs.

## <a name="syntax"></a>Syntaxe

```fsharp
(element, ... , element)
struct(element, ... ,element )
```

## <a name="remarks"></a>Notes

Chaque *élément* dans la syntaxe précédente peut être valide F# expression.

## <a name="examples"></a>Exemples

Les exemples de tuples de paires, triples et ainsi de suite, des types identiques ou différents. Certains exemples sont illustrés dans le code suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/basic-examples.fsx#L6-L21)]

## <a name="obtaining-individual-values"></a>Obtention de valeurs individuelles

Vous pouvez utiliser critères spéciaux pour accéder et affecter des noms pour les éléments de tuple, comme indiqué dans le code suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/basic-examples.fsx#L27-L29)]

Vous pouvez également déconstruire un tuple par le biais de critères spéciaux à l’extérieur d’un `match` expression via `let` liaison :

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/basic-examples.fsx#L34-L37)]

Ou vous pouvez répéter correspondent dans les tuples comme entrées des fonctions :

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/basic-examples.fsx#L43-L47)]

Si vous avez besoin qu’un seul élément du tuple, le caractère générique (trait de soulignement) peut être utilisé pour éviter de créer un nouveau nom pour une valeur que vous n’avez pas besoin.

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/basic-examples.fsx#L53-L54)]

Copie les éléments à partir d’un tuple de référence en un tuple de struct est également simple :

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/basic-examples.fsx#L62-L66)]

Les fonctions `fst` et `snd` (référencer uniquement des tuples) retourne le premier et le second élément d’un tuple, respectivement.

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/basic-examples.fsx#L72-L73)]

Il n’existe aucune fonction intégrée qui retourne le troisième élément d’un triple, mais vous pouvez facilement écrire une comme suit.

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/basic-examples.fsx#L78-L78)]

En règle générale, il est préférable d’utiliser les critères spéciaux pour accéder aux éléments de tuple individuels.

## <a name="using-tuples"></a>À l’aide de Tuples

Ils fournissent un moyen pratique pour retourner plusieurs valeurs à partir d’une fonction, comme indiqué dans l’exemple suivant. Cet exemple effectue une division d’entier et retourne le résultat arrondi de l’opération en tant que premier membre d’une paire de tuple et le reste en tant que deuxième membre de la paire.

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/basic-examples.fsx#L83-L86)]

Tuples peuvent également servir en tant qu’arguments de fonction lorsque vous souhaitez éviter la curryfication implicite des arguments de fonction qui est impliquée par la syntaxe de fonction standard.

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/basic-examples.fsx#L88-L88)]

La syntaxe habituelle pour la définition de la fonction `let sum a b = a + b` vous permet de définir une fonction qui est l’application partielle du premier argument de la fonction, comme indiqué dans le code suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/basic-examples.fsx#L90-L94)]

À l’aide d’un tuple comme paramètre désactive la curryfication. Pour plus d’informations, consultez « Application partielle d’Arguments » dans [fonctions](functions/index.md).

## <a name="names-of-tuple-types"></a>Noms des Types de Tuple

Lorsque vous écrivez le nom d’un type qui est un tuple, vous utilisez le `*` symbole pour séparer les éléments. Pour un tuple qui se compose d’un `int`, un `float`et un `string`, tel que `(10, 10.0, "ten")`, le type est écrit comme suit.

```fsharp
int * float * string
```

## <a name="interoperation-with-c-tuples"></a>Interopérabilité avec des Tuples de c#

C# 7.0 introduit des tuples à la langue.  Les tuples dans C# sont des structs et sont équivalents aux tuples de struct dans F#.  Si vous avez besoin interagir avec c#, vous devez utiliser des tuples de struct.

Il est facile à réaliser.  Par exemple, supposons que vous devez passer un tuple à une classe c# et les utiliser ensuite son résultat, qui est également un tuple :

```csharp
namespace CSharpTupleInterop
{
    public static class Example
    {
        public static (int, int) AddOneToXAndY((int x, int y) a) =>
            (a.x + 1, a.y + 1);
    }
}
```

Dans votre F# code, vous pouvez ensuite transmettre un tuple de struct comme paramètre et consommer le résultat sous forme de tuple struct.

```fsharp
open TupleInterop

let struct (newX, newY) = Example.AddOneToXAndY(struct (1, 2))
// newX is now 2, and newY is now 3
```

### <a name="converting-between-reference-tuples-and-struct-tuples"></a>Conversion entre les Tuples de référence et les Tuples de Struct

Étant donné que les Tuples de référence et les Tuples de Struct ont une représentation sous-jacente complètement différente, ils ne sont pas implicitement convertibles.  Autrement dit, le code suivant n’est pas compilé :

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/interop.fsx#L5-L12)]

Vous devez répéter mettre en correspondance un tuple et construire l’autre avec les éléments constitutifs.  Exemple :

[!code-fsharp[Main](../../../samples/snippets/fsharp/tuples/interop.fsx#L18-L22)]

## <a name="compiled-form-of-reference-tuples"></a>Forme compilée de Tuples de référence

Cette section explique le formulaire de tuples quand elles sont compilées.  Les informations ici n’est pas nécessaire pour lire, sauf si vous ciblez .NET Framework 3.5 ou inférieure.

Tuples sont compilés en objets d’un des divers types génériques, toutes nommées `System.Tuple`, qui sont surchargés sur l’arité, nombre de paramètres de type. Types de tuple s’affichent dans ce formulaire lorsque vous les affichez à partir d’un autre langage, tel que C# ou Visual Basic, ou lorsque vous utilisez un outil qui n’a pas connaissance de F# construit. Le `Tuple` types ont été introduits dans .NET Framework 4. Si vous ciblez une version antérieure du .NET Framework, le compilateur utilise les versions de [System.Tuple](https://msdn.microsoft.com/library/5ac7953d-acdc-4a58-bfb7-c1f6406c0fa3) à partir de la version 2.0 de la F# bibliothèque principale. Les types dans cette bibliothèque sont utilisés uniquement pour les applications qui ciblent le 2.0, 3.0 et les versions du .NET Framework 3.5. Le transfert de type est utilisé pour assurer la compatibilité binaire entre .NET Framework 2.0 et .NET Framework 4 F# composants.

### <a name="compiled-form-of-struct-tuples"></a>Forme compilée de Tuples de Struct

Les tuples de struct (par exemple, `struct (x, y)`), sont fondamentalement différent des tuples de référence.  Ils sont compilés dans le <xref:System.ValueTuple> type, surchargé par une arité, ou le nombre de paramètres de type.  Ils sont équivalents à [c# 7.0 Tuples](../../csharp/tuples.md) et [Visual Basic 2017 Tuples](../../visual-basic/programming-guide/language-features/data-types/tuples.md)et interagir en mode bidirectionnel.

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Types F#](fsharp-types.md)
