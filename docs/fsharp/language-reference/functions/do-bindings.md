---
title: Liaisons do (F#)
description: "Découvrez comment une liaison ' do' F # est utilisé pour exécuter du code sans définir une fonction ou une valeur."
ms.date: 05/16/2016
ms.openlocfilehash: 78dbf8da0fe40b5af566ad98693df1109eede7e4
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44192149"
---
# <a name="do-bindings"></a>Liaisons do

Un `do` liaison est utilisée pour exécuter du code sans définir une fonction ou une valeur. En outre, les liaisons do peuvent être utilisées dans les classes, consultez [ `do` liaisons dans les Classes](../members/do-bindings-in-classes.md).

## <a name="syntax"></a>Syntaxe

```fsharp
[ attributes ]
[ do ]expression
```

## <a name="remarks"></a>Notes

Utilisez un `do` liaison lorsque vous souhaitez exécuter du code indépendamment d’une définition de fonction ou de valeur. L’expression dans une `do` liaison doit retourner `unit`. Le code dans un niveau supérieur `do` liaison est exécutée lorsque le module est initialisé. Le mot clé `do` est facultatif.

Attributs peuvent être appliqués à un niveau supérieur `do` liaison. Par exemple, si votre programme utilise COM interop, vous souhaiterez appliquer la `STAThread` attribut à votre programme. Vous pouvez le faire à l’aide d’un attribut sur un `do` de liaison, comme indiqué dans le code suivant.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet201.fs)]

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](../index.md)
- [Fonctions](index.md)
