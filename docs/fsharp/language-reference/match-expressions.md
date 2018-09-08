---
title: 'Expressions de correspondance (F #)'
description: 'Découvrez comment l’expression de correspondance F # fournit le contrôle de branchement basé sur la comparaison d’une expression avec un jeu de modèles.'
ms.date: 04/19/2018
ms.openlocfilehash: e4cb82f20fe82bff562736557c2346562c557f59
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44132037"
---
# <a name="match-expressions"></a>Expressions de correspondance

Le `match` expression fournit le contrôle de branchement basé sur la comparaison d’une expression avec un jeu de modèles.

## <a name="syntax"></a>Syntaxe

```fsharp
// Match expression.
match test-expression with
| pattern1 [ when condition ] -> result-expression1
| pattern2 [ when condition ] -> result-expression2
| ...

// Pattern matching function.
function
| pattern1 [ when condition ] -> result-expression1
| pattern2 [ when condition ] -> result-expression2
| ...
```

## <a name="remarks"></a>Notes

Les expressions de critères spéciaux permettent des branchements complexes basés sur la comparaison d’une expression de test avec un jeu de modèles. Dans le `match` expression, le *expression de test* est comparée à chaque modèle à son tour, et lorsqu’une correspondance est trouvée, correspondants *expression de résultat* est évaluée et la valeur résultante est retourné en tant que la valeur de l’expression de correspondance.

Les critères spéciaux (fonction) indiquée dans la syntaxe précédente est une expression lambda dans laquelle des critères spéciaux sont exécutés immédiatement sur l’argument. Les critères spéciaux (fonction) indiquée dans la syntaxe précédente est équivalente à la suivante.

```fsharp
fun arg ->
    match arg with
    | pattern1 [ when condition ] -> result-expression1
    | pattern2 [ when condition ] -> result-expression2
    | ...
```

Pour plus d’informations sur les expressions lambda, consultez [Expressions Lambda : le `fun` mot clé](functions/lambda-expressions-the-fun-keyword.md).

L’ensemble de modèles doit couvrir toutes les correspondances possibles de la variable d’entrée. Vous utilisez fréquemment, le modèle de caractère générique (`_`) en tant que le dernier modèle pour faire correspondre les valeurs d’entrée précédemment sans correspondance.

Le code suivant illustre quelques-unes des façons dans lequel le `match` expression est utilisée. Pour une référence et des exemples de tous les modèles qui peuvent être utilisées, consultez [critères spéciaux](pattern-matching.md).

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4601.fs)]

## <a name="guards-on-patterns"></a>Gardes sur des modèles

Vous pouvez utiliser un `when` clause pour spécifier une condition supplémentaire que la variable doit satisfaire pour correspondre à un modèle. Une telle clause est appelée un *protéger*. L’expression qui suit le `when` mot clé n’est pas évaluée, sauf si une correspondance est établie pour le modèle associé à ce garde.

L’exemple suivant illustre l’utilisation d’un garde pour spécifier une plage numérique pour un modèle de variable. Notez que plusieurs conditions sont combinées à l’aide d’opérateurs booléens.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4602.fs)]

Notez qu’étant donné que les valeurs autres que des littéraux ne peut pas être utilisés dans le modèle, vous devez utiliser un `when` clause si vous devez comparer une partie de l’entrée par rapport à une valeur. Ceci est illustré dans le code suivant :

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4603.fs)]

Notez que lorsqu’un modèle d’union est couvert par un garde, le module de protection s’applique à **tous les** des modèles, pas seulement celui dernier. Par exemple, prenons le code suivant, le module de protection `when a > 12` s’applique aux deux `A a` et `B a`:

```fsharp
type Union =
    | A of int
    | B of int

let foo() =
    let test = A 42
    match test with
    | A a
    | B a when a > 41 -> a // the guard applies to both patterns
    | _ -> 1

foo() // returns 42
```

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)  
- [Modèles actifs](active-patterns.md)  
- [Critères spéciaux](pattern-matching.md)  
