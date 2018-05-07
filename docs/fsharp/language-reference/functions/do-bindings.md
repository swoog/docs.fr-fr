---
title: Liaisons do (F#)
description: "Découvrir comment une liaison de ' do' F # est utilisé pour exécuter du code sans définir de fonction ou une valeur."
ms.date: 05/16/2016
ms.openlocfilehash: 6fd084090a204beab0da1c2deb5b5ae2a86281c8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="do-bindings"></a>Liaisons do

A `do` liaison est utilisée pour exécuter du code sans définir de fonction ou une valeur. En outre, les liaisons do peuvent être utilisées dans les classes, consultez [ `do` liaisons dans les Classes](../members/do-bindings-in-classes.md).


## <a name="syntax"></a>Syntaxe

```fsharp
[ attributes ]
[ do ]expression
```

## <a name="remarks"></a>Notes
Utilisez un `do` liaison lorsque vous souhaitez exécuter du code indépendamment d’une définition de fonction ou de valeur. L’expression dans une `do` liaison doit retourner `unit`. Le code dans un niveau supérieur `do` liaison est exécutée lorsque le module est initialisé. Le mot clé `do` est facultatif.

Attributs peuvent être appliqués à un niveau supérieur `do` liaison. Par exemple, si votre programme utilise COM interop, vous pouvez souhaiter appliquer le `STAThread` d’attribut à votre programme. Vous pouvez pour cela à l’aide d’un attribut sur un `do` de liaison, comme indiqué dans le code suivant.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet201.fs)]
    
## <a name="see-also"></a>Voir aussi
[Informations de référence du langage F#](../index.md)

[Fonctions](index.md)

