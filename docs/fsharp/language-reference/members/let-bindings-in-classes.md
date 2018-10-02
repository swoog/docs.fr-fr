---
title: Liaisons let dans les classes (F#)
description: "Découvrez comment définir des champs privés et des fonctions privées pour les classes F # à l’aide de liaisons 'let' dans la définition de classe."
ms.date: 05/16/2016
ms.openlocfilehash: 237eb98a57571a21c9187abf31f05160374cf4fc
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48033218"
---
# <a name="let-bindings-in-classes"></a>Liaisons let dans des classes

Vous pouvez définir des champs privés et des fonctions privées pour les classes F # à l’aide de `let` liaisons dans la définition de classe.

## <a name="syntax"></a>Syntaxe

```fsharp
// Field.
[static] let [ mutable ] binding1 [ and ... binding-n ]

// Function.
[static] let [ rec ] binding1 [ and ... binding-n ]
```

## <a name="remarks"></a>Notes

La syntaxe précédente apparaît après les déclarations de titre et l’héritage de classe, mais avant les définitions de membre. La syntaxe est similaire à celle de `let` liaisons en dehors des classes, mais les noms définis dans une classe ont une portée est limitée à la classe. Un `let` liaison crée un champ privé ou une fonction ; pour exposer des données ou les fonctions déclarer publiquement, une propriété ou une méthode membre.

Un `let` liaison qui n’est pas statique est appelée une instance `let` liaison. Instance `let` liaisons exécutent lorsque des objets sont créés. Statique `let` liaisons font partie de l’initialiseur statique pour la classe, qui est toujours exécuté avant que le type est utilisé tout d’abord.

Le code au sein de l’instance `let` liaisons peuvent utiliser les paramètres du constructeur principal.

Attributs et les modificateurs d’accessibilité ne sont pas autorisés sur `let` liaisons dans les classes.

Les exemples de code suivants illustrent plusieurs types de `let` liaisons dans les classes.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3001.fs)]

La sortie est la suivante.

```
10 52 1 204
```

## <a name="alternative-ways-to-create-fields"></a>Autres manières de créer des champs

Vous pouvez également utiliser le `val` mot clé pour créer un champ privé. Lorsque vous utilisez le `val` mot clé, le champ n'est pas une valeur donné lorsque l’objet est créé, mais est initialisé avec une valeur par défaut. Pour plus d’informations, consultez [champs explicites : val mot clé](explicit-fields-the-val-keyword.md).

Vous pouvez également définir des champs privés dans une classe en utilisant une définition de membre et en ajoutant le mot clé `private` à la définition. Cela peut être utile si vous envisagez de modifier l’accessibilité d’un membre sans réécrire votre code. Pour plus d’informations, consultez [Contrôle d’accès](../access-control.md).

## <a name="see-also"></a>Voir aussi

- [Membres](index.md)
- [Liaisons `do` dans des classes](do-bindings-in-classes.md)
- [`let` liaisons](../functions/let-bindings.md)
