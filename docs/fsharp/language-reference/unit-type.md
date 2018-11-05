---
title: Type unit (F#)
description: Découvrez comment le type 'unit' F# est souvent utilisé pour marquer l’emplacement où une valeur est requise par la syntaxe du langage lorsqu’aucune valeur n’est nécessaire ou souhaitée.
ms.date: 05/16/2016
ms.openlocfilehash: c3dfa5f63c25a1e8abc0f75b905c129b311479af
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "44204654"
---
# <a name="unit-type"></a>Unit, type

Le `unit` type est un type qui indique l’absence d’une valeur spécifique ; la `unit` type a uniquement une valeur unique, qui agit comme un espace réservé lorsqu’aucune autre valeur n’existe ou n’est nécessaire.

## <a name="syntax"></a>Syntaxe

```fsharp
// The value of the unit type.
()
```

## <a name="remarks"></a>Notes

Chaque expression F# doit correspondre à une valeur. Pour les expressions qui ne génèrent pas d’une valeur qui est intéressant, la valeur de type `unit` est utilisé. Le `unit` type ressemble à la `void` type dans les langages tels que c# et C++.

Le `unit` type a une valeur unique, et cette valeur est indiquée par le jeton `()`.

La valeur de la `unit` type est souvent utilisé dans la programmation F# pour marquer l’emplacement où une valeur est requise par la syntaxe du langage, mais lorsqu’aucune valeur n’est nécessaire ou souhaitée. Un exemple peut être la valeur de retour d’un `printf` (fonction). Étant donné que les actions importantes de la `printf` opération se produisent dans la fonction, la fonction n’a pas de retourner une valeur réelle. Par conséquent, la valeur de retour est de type `unit`.

Certaines constructions attendent un `unit` valeur. Par exemple, un `do` liaison ou du code au niveau supérieur d’un module est supposée correspondre à un `unit` valeur. Le compilateur émet un avertissement lorsqu’un `do` liaison ou du code au niveau supérieur d’un module produit un résultat autre que le `unit` valeur qui n’est pas utilisé, comme indiqué dans l’exemple suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet901.fs)]

Cet avertissement est une caractéristique de la programmation fonctionnelle ; Il n’apparaît pas dans les autres langages de programmation .NET. Dans un programme purement fonctionnel, dans lequel les fonctions n’ont pas d’effets secondaires, la valeur de retournée finale est le seul résultat d’un appel de fonction. Par conséquent, lorsque le résultat est ignoré, il est une erreur de programmation possible. Bien que F# n’est pas un langage de programmation purement fonctionnel, il est conseillé de suivre le style de programmation fonctionnel chaque fois que possible.

## <a name="see-also"></a>Voir aussi

- [Primitifs](primitive-types.md)
- [Informations de référence du langage F#](index.md)
