---
title: Comparaison entre propriétés et indexeurs (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- properties [C#], vs. indexers
- indexers [C#], vs. properties
ms.assetid: 3358a89f-44a0-4a4d-bf8c-07237a90af39
ms.openlocfilehash: 3a78b97f2cac1f2c49be03bc351d9b6f4b6438e6
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43861440"
---
# <a name="comparison-between-properties-and-indexers-c-programming-guide"></a>Comparaison entre propriétés et indexeurs (Guide de programmation C#)
Les indexeurs sont semblables aux propriétés. À l’exception des différences répertoriées dans le tableau suivant, toutes les règles définies pour les accesseurs des propriétés s’appliquent également aux accesseurs des indexeurs.  
  
|Property|Indexeur|  
|--------------|-------------|  
|Permet aux méthodes d’être appelées comme si elles étaient des membres de données publics.|Permet aux éléments d’une collection interne d’un objet d’être accessibles à l’aide de la notation de tableau sur l’objet lui-même.|  
|Accessible par le biais d’un nom simple.|Accessible par le biais d’un index.|  
|Peut être un membre statique ou un membre d’instance.|Doit être un membre d’instance.|  
|Un accesseur [get](../../../csharp/language-reference/keywords/get.md) d’une propriété n’a aucun paramètre.|Un accesseur `get` d’un indexeur possède la même liste de paramètres formels que l’indexeur.|  
|Un accesseur [set](../../../csharp/language-reference/keywords/set.md) d’une propriété contient le paramètre `value` implicite.|Un accesseur `set` d’un indexeur possède la même liste de paramètres formels que l’indexeur, outre le paramètre [value](../../../csharp/language-reference/keywords/value.md).|  
|Prend en charge la syntaxe abrégée avec les [propriétés implémentées automatiquement](../../../csharp/programming-guide/classes-and-structs/auto-implemented-properties.md).|Ne prend pas en charge la syntaxe abrégée.|  
  
## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Indexeurs](../../../csharp/programming-guide/indexers/index.md)  
- [Propriétés](../../../csharp/programming-guide/classes-and-structs/properties.md)
