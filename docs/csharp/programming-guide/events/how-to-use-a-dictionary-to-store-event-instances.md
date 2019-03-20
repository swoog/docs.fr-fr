---
title: 'Guide pratique : Utiliser un dictionnaire pour stocker des instances d’événements – Guide de programmation C#'
ms.custom: seodec18
ms.date: 03/11/2019
helpviewer_keywords:
- events [C#], storing instances in a Dictionary
ms.assetid: 9512c64d-5aaf-40cd-b941-ca2a592f0064
ms.openlocfilehash: f8522e499887398402f63c7788bbc6c6c4f57782
ms.sourcegitcommit: 16aefeb2d265e69c0d80967580365fabf0c5d39a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2019
ms.locfileid: "57845270"
---
# <a name="how-to-use-a-dictionary-to-store-event-instances-c-programming-guide"></a>Guide pratique : Utiliser un dictionnaire pour stocker des instances d’événements (Guide de programmation C#)

Les accesseurs d’événements personnalisés `add` et `remove` peuvent notamment servir à exposer un grand nombre d’événements sans allouer de champ à chacun, mais en utilisant une instance <xref:System.Collections.Generic.Dictionary%602> pour stocker les instances d’événements, comme le montre l’exemple ci-dessous. Cette méthode n’est utile que si le site comporte de nombreux événements, dont la plupart ne seront probablement pas souscrits.

[!code-csharp[csProgGuideEvents#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideEvents/CS/Events.cs#9)]

Cette implémentation est conforme au comportement [d’ajout et de suppression de délégués](~/_csharplang/spec/delegates.md#delegate-invocation) de la spécification du langage C#.

Vous remarquerez que l’instruction [lock](../../language-reference/keywords/lock-statement.md) ne sert qu’à *accéder* au dictionnaire comportant les gestionnaires d’événements. N’appelez pas un gestionnaire d’événements se trouvant dans le corps de l’instruction `lock`, car cela pourrait entraîner des blocages ou une contention de verrouillage.

## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../../../csharp/programming-guide/index.md)
- [Événements](../../../csharp/programming-guide/events/index.md)
- [Délégués](../../../csharp/programming-guide/delegates/index.md)
