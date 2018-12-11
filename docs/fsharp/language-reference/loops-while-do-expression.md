---
title: 'Boucles : expression while...do (F#)'
description: Voir comment l’instruction while... faire expression est utilisée pour effectuer une exécution itérative (boucle) pendant une condition de test spécifiée a la valeur true.
ms.date: 05/16/2016
ms.openlocfilehash: 43e2098ad6c7f103babc2471aebe987040feb989
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53127275"
---
# <a name="loops-whiledo-expression"></a>Boucles : expression while...do

Le `while...do` expression est utilisée pour effectuer une exécution itérative (boucle) pendant une condition de test spécifiée a la valeur true.

## <a name="syntax"></a>Syntaxe

```fsharp
while test-expression do
    body-expression
```

## <a name="remarks"></a>Notes

Le *expression de test* est évaluée ; si elle est `true`, le *expression de corps* est exécutée et l’expression de test est de nouveau évaluée. Le *expression de corps* doit avoir de type `unit`. Si l’expression de test est `false`, l’itération se termine.

L’exemple suivant illustre l’utilisation de la `while...do` expression.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5301.fs)]

La sortie du code précédent est un flux de nombres aléatoires compris entre 1 et 20, la dernière qui est 10.

```
13 19 8 18 16 2 10
Found a 10!
```

> [!NOTE]
> Vous pouvez utiliser `while...do` dans les expressions de séquence et autres expressions de calcul, auquel cas une version personnalisée de la `while...do` expression est utilisée. Pour plus d’informations, consultez [séquences](sequences.md), [flux de travail asynchrones](asynchronous-workflows.md), et [Expressions de calcul](computation-expressions.md).

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Boucles : `for...in` Expression](loops-for-in-expression.md)
- [Boucles : `for...to` Expression](loops-for-to-expression.md)
