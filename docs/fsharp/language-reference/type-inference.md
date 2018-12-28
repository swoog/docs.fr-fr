---
title: Inférence de type
description: Découvrez comment la F# compilateur déduit les types de valeurs, variables, paramètres et valeurs de retour.
ms.date: 05/16/2016
ms.openlocfilehash: 3e61d5c81fde0a48af66a47745123a842dc04cb1
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612788"
---
# <a name="type-inference"></a>Inférence de type

Cette rubrique décrit comment la F# compilateur déduit les types de valeurs, variables, paramètres et valeurs de retour.

## <a name="type-inference-in-general"></a>En général l’inférence de type

L’idée d’inférence de type est que vous n’êtes pas obligé de spécifier les types de F# constructions, sauf lorsque le compilateur ne peut pas déduire ait le type. Omettre les informations de type explicite ne signifie pas que F# est un langage saisi dynamiquement ou que les valeurs de F# sont faiblement typée. F#est un langage statiquement typé, ce qui signifie que le compilateur déduit un type exact pour chaque construction pendant la compilation. S’il n’est pas suffisamment d’informations pour le compilateur de déduire les types de chaque construction, vous devez fournir les informations de type supplémentaires, généralement en ajoutant des annotations de type explicite quelque part dans le code.

## <a name="inference-of-parameter-and-return-types"></a>Inférence des Types de retour et de paramètre

Dans une liste de paramètres, il est inutile de spécifier le type de chaque paramètre. Et pourtant, F# est un langage typé statiquement, et par conséquent, chaque valeur et chaque expression ont un type défini au moment de la compilation. Pour ces types que vous ne spécifiez pas explicitement, le compilateur déduit le type en fonction du contexte. Si le type n’est pas un spécifiée autrement, il est déduit de manière générique. Si le code utilise une valeur de façon incohérente, de sorte qu’il n’existe pas d’une seule déduit le type qui satisfait à toutes les utilisations d’une valeur, que le compilateur signale une erreur.

Le type de retour d’une fonction est déterminé par le type de la dernière expression dans la fonction.

Par exemple, dans le code suivant, les types de paramètres `a` et `b` et le type de retour sont déduits à être `int` , car le littéral `100` est de type `int`.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet301.fs)]

Vous pouvez influencer l’inférence de type en modifiant les littéraux. Si vous effectuez la `100` un `uint32` en ajoutant le suffixe `u`, les types de `a`, `b`, et la valeur de retour sont déduits pour être `uint32`.

Vous pouvez également influencer l’inférence de type à l’aide d’autres constructions qui impliquent des restrictions sur le type, tel que les fonctions et méthodes qui fonctionnent avec uniquement un type particulier.

En outre, vous pouvez appliquer des annotations de type explicite aux paramètres de fonction ou une méthode ou à des variables dans les expressions, comme indiqué dans les exemples suivants. Erreurs entraînent des conflits entre différentes contraintes.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet302.fs)]

Vous pouvez également spécifier explicitement la valeur de retour d’une fonction en fournissant une annotation de type après tout les paramètres.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet303.fs)]

Un cas courant où une annotation de type est utile sur un paramètre est lorsque le paramètre est un type d’objet et que vous souhaitez utiliser un membre.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet304.fs)]

## <a name="automatic-generalization"></a>Généralisation automatique

Si le code de fonction n’est pas dépendant du type d’un paramètre, le compilateur considère que le paramètre de manière générique. Il s’agit *généralisation automatique*, et il peut être très utile pour écrire du code générique sans accroître la complexité.

Par exemple, la fonction suivante combine deux paramètres de n’importe quel type en un tuple.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-3/snippet305.fs)]

Le type est déduit pour être

```fsharp
'a -> 'b -> 'a * 'b
```

## <a name="additional-information"></a>Informations supplémentaires

Inférence de type est décrite plus en détail dans le F# spécification du langage.

## <a name="see-also"></a>Voir aussi

- [Généralisation automatique](generics/automatic-generalization.md)