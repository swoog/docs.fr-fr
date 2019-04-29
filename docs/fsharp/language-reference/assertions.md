---
title: Assertions
description: Découvrez comment utiliser l’expression « déclarer » comme une fonctionnalité de débogage pour le test des expressions dans le F# langage de programmation.
ms.date: 05/16/2016
ms.openlocfilehash: c2d97386e87e9b915da490a78fff9aedb9def616
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61703216"
---
# <a name="assertions"></a>Assertions

Le `assert` expression est une fonctionnalité de débogage que vous pouvez utiliser pour tester une expression. En cas d’échec en mode débogage, une assertion génère une boîte de dialogue d’erreur système.

## <a name="syntax"></a>Syntaxe

```fsharp
assert condition
```

## <a name="remarks"></a>Notes

Le `assert` expression a le type `bool -> unit`.

Dans la syntaxe précédente, *condition* représente une expression booléenne qui doit être testée. Si l’expression prend la valeur `true`, l’exécution se poursuit normalement. Si elle a la valeur `false`, une boîte de dialogue d’erreur système est générée. La boîte de dialogue d’erreur comprend une légende qui contient la chaîne **Échec de l’Assertion**. La boîte de dialogue contient une trace de pile qui indique où l’échec d’assertion s’est produite.

Vérification de l’assertion est activée uniquement lorsque vous compilez en mode débogage ; Autrement dit, si la constante `DEBUG` est défini. Dans le système de projet, par défaut, le `DEBUG` constante n’est définie dans la configuration Debug, mais pas dans la configuration Release.

L’erreur d’échec d’assertion ne peut pas être interceptée à l’aide de F# gestion des exceptions.

> [!NOTE]
> Le `assert` fonction se résout en <xref:System.Diagnostics.Debug.Assert*?displayProperty=nameWithType>.

## <a name="example"></a>Exemple

L’exemple de code suivant illustre l’utilisation de la `assert` expression.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5401.fs)]

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)