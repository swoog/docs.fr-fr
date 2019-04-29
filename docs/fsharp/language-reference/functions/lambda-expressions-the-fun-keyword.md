---
title: 'Expressions lambda : Le mot clé fun'
description: Découvrez comment utiliser le F# mot clé « fun » pour définir une expression lambda, qui est une fonction anonyme.
ms.date: 05/16/2016
ms.openlocfilehash: 6ad15173bb8643bff330e3ca3823cba5d43ad445
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61941022"
---
# <a name="lambda-expressions-the-fun-keyword-f"></a>Expressions lambda : Le mot clé fun (F#)

Le `fun` mot clé est utilisé pour définir une expression lambda, autrement dit, une fonction anonyme.

## <a name="syntax"></a>Syntaxe

```fsharp
fun parameter-list -> expression
```

## <a name="remarks"></a>Notes

Le *liste de paramètres* se compose généralement de noms et, éventuellement, de types de paramètres. En règle générale, le *liste de paramètres* peuvent être composées de n’importe quel F# modèles. Pour obtenir une liste complète des modèles possibles, consultez [critères spéciaux](../pattern-matching.md). Listes de paramètres valides comprennent les exemples suivants.

```fsharp
// Lambda expressions with parameter lists.
fun a b c -> ...
fun (a: int) b c -> ...
fun (a : int) (b : string) (c:float) -> ...

// A lambda expression with a tuple pattern.
fun (a, b) -> …

// A lambda expression with a list pattern.
fun head :: tail -> …
```

Le *expression* est le corps de la fonction, la dernière expression qui génère une valeur de retour. Exemples d’expressions lambda valides sont les suivants :

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet301.fs)]

## <a name="using-lambda-expressions"></a>Utilisation d’expressions lambda

Expressions lambda sont particulièrement utiles lorsque vous souhaitez effectuer des opérations sur une liste ou une autre collection et souhaitez éviter le travail supplémentaire de la définition d’une fonction. Nombreux F# les fonctions de bibliothèque acceptent des valeurs de fonction en tant qu’arguments, et il peut être particulièrement pratique d’utiliser une expression lambda dans ces cas. Le code suivant applique une expression lambda aux éléments d’une liste. Dans ce cas, la fonction anonyme ajoute 1 à chaque élément d’une liste.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet302.fs)]

## <a name="see-also"></a>Voir aussi

- [Fonctions](index.md)