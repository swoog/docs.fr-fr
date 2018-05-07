---
title: 'Expressions lambda : mot clé fun (F#)'
description: "Découvrez comment utiliser le mot clé F # 'fun' pour définir une expression lambda, qui est une fonction anonyme."
ms.date: 05/16/2016
ms.openlocfilehash: 433451fb9bf89bfabdcd8e71560105317771d251
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="lambda-expressions-the-fun-keyword-f"></a>Expressions lambda : mot clé fun (F#)

Le `fun` est utilisé pour définir une expression lambda, autrement dit, une fonction anonyme.


## <a name="syntax"></a>Syntaxe

```fsharp
fun parameter-list -> expression
```

## <a name="remarks"></a>Notes
Le *la liste des paramètres* se compose généralement de noms et, éventuellement, de types de paramètres. En règle générale, les *la liste des paramètres* peuvent être composées de n’importe quel modèle F #. Pour obtenir une liste complète des modèles possibles, consultez [recherche de correspondance](../pattern-matching.md). Les listes de paramètres valides incluent les exemples suivants.

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

Le *expression* est le corps de la fonction, la dernière expression qui génère une valeur de retour. Exemples d’expressions lambda valides sont les suivantes :

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet301.fs)]
    
## <a name="using-lambda-expressions"></a>Utilisation d’expressions lambda
Expressions lambda sont particulièrement utiles lorsque vous souhaitez effectuer des opérations sur une liste ou un autre regroupement et souhaitez éviter la définition d’une fonction. De nombreuses fonctions de bibliothèque F # prennent les valeurs de fonction en tant qu’arguments, et il peut être particulièrement pratique d’utiliser une expression lambda dans ces cas. Le code suivant applique une expression lambda aux éléments d’une liste. Dans ce cas, la fonction anonyme ajoute 1 à chaque élément d’une liste.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet302.fs)]
    
## <a name="see-also"></a>Voir aussi
[Fonctions](index.md)
