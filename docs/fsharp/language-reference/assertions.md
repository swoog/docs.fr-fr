---
title: Assertions (F#)
description: "Découvrez comment utiliser l’expression 'assert' comme une fonctionnalité de débogage pour tester des expressions dans le langage de programmation F #."
ms.date: 05/16/2016
ms.openlocfilehash: 83e6cd77bbbb2c32e9b778e5bf6dd9d2e9c8fe32
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="assertions"></a>Assertions

Le `assert` expression est une fonctionnalité de débogage que vous pouvez utiliser pour tester une expression. En cas d’échec en mode débogage, une assertion génère une boîte de dialogue d’erreur système.

## <a name="syntax"></a>Syntaxe

```fsharp
assert condition
```

## <a name="remarks"></a>Notes

Le `assert` l’expression est de type `bool -> unit`.

Dans la syntaxe précédente, *condition* représente une expression booléenne qui doit être testée. Si l’expression prend la valeur `true`, l’exécution se poursuit normalement. Si elle a la valeur `false`, une boîte de dialogue d’erreur système est générée. La boîte de dialogue d’erreur comprend une légende qui contient la chaîne **Échec de l’Assertion**. La boîte de dialogue contient une trace de pile qui indique où l’échec d’assertion s’est produite.

La vérification des assertions est activée uniquement lorsque vous compilez en mode débogage ; Autrement dit, si la constante `DEBUG` est défini. Dans le système de projet, par défaut, le `DEBUG` constante est définie dans la configuration Debug, mais pas dans la configuration Release.

Erreur d’échec de l’assertion ne peut pas être intercepté à l’aide de la gestion des exceptions) (F #.

>[!NOTE]
Le `assert` fonction correspond à <xref:System.Diagnostics.Debug.Assert*?displayProperty=nameWithType>.

## <a name="example"></a>Exemple

L’exemple de code suivant illustre l’utilisation de la `assert` expression.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5401.fs)]
    
## <a name="see-also"></a>Voir aussi

[Informations de référence du langage F#](index.md)
