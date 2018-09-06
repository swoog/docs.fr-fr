---
title: Choix entre classe et structure
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], structures
- class library design guidelines [.NET Framework], classes
- structures [.NET Framework], vs. classes
- classes [.NET Framework], design guidelines
- type design guidelines, structures
- structures [.NET Framework], design guidelines
- classes [.NET Framework], vs. structures
- type design guidelines, classes
ms.assetid: f8b8ec9b-0ba7-4dea-aadf-a93395cd804f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 06661cb2c34d1da9085fa2129cb0c3307b99097e
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43865551"
---
# <a name="choosing-between-class-and-struct"></a>Choix entre classe et structure
Une des décisions de conception de base qu'est confrontée chaque concepteur framework est s’il faut un type de conception sous la forme d’une classe (type référence) ou un struct (type valeur). Est de bien comprendre les différences dans le comportement des types référence et les types valeur essentiel pour faire ce choix.  
  
 La première différence entre les types référence et les types de valeur nous considérera est que les types référence sont alloués sur le tas et le garbage collector, alors que les types valeur sont alloués sur la pile ou inline dans contenant les types et libérée lorsque la pile se déroule ou quand leur type conteneur est désallouée. Par conséquent, les allocations et désallocations de types valeur sont en général moins cher que les allocations et désallocations de types référence.  
  
 Ensuite, les tableaux de référence sont des types alloués hors ligne, ce qui signifie que le tableau d’éléments sont simplement les références aux instances du type référence résidant sur le tas. Les tableaux de types valeur sont alloués inline, ce qui signifie que les éléments du tableau sont les instances réelles du type valeur. Par conséquent, les allocations et désallocations de tableaux de types valeur sont beaucoup moins chers que les allocations et désallocations de tableaux de types référence. En outre, les tableaux de types valeur présentent une bien meilleure localité de référence dans la majorité des cas.  
  
 La différence suivante est liée à l’utilisation de la mémoire. Types valeur inclus lors de la conversion en un type de référence ou une des interfaces qu’ils implémentent. Ils obtiennent unboxed lors de la conversion vers le type de valeur. Étant donné que les zones sont des objets qui sont alloués sur le tas et sont garbage collector, trop boxing et unboxing peut avoir un impact négatif sur le tas, le garbage collector et, finalement, les performances de l’application.  En revanche, pas de boxing se produit comme types référence sont convertis.  
  
 Ensuite, les affectations de type référence copier la référence, tandis que les affectations de type valeur copiez la valeur entière. Par conséquent, des types référence volumineux sont moins cher que les affectations de types de valeur élevée.  
  
 Enfin, les types référence sont passés par référence, tandis que les types valeur sont passés par valeur. Modifications apportées à une instance d’un type référence affectent toutes les références pointant vers l’instance. Les instances de types valeur sont copiés quand ils sont passés par valeur. Lorsqu’une instance d’un type valeur est modifiée, elle évidemment n’affecte pas un de ses copies. Étant donné que les copies ne sont pas créées explicitement par l’utilisateur, mais sont créées implicitement lorsque les arguments sont passés ou retournent les valeurs sont retournées, les types de valeur qui peuvent être modifiées peuvent prêter à confus à de nombreux utilisateurs. Par conséquent, les types valeur doivent être immuables.  
  
 En règle générale, la majorité des types dans une infrastructure doit-elle être des classes. Toutefois, il existe certaines situations dans lesquelles les caractéristiques d’un type valeur rendent plus appropriées à utiliser les structures.  
  
 **✓ CONSIDER** définition d’un struct au lieu d’une classe si les instances du type sont généralement de courte durée et de petite taille ou sont généralement incorporés dans d’autres objets.  
  
 **X AVOID** définition d’un struct, sauf si le type possède toutes les caractéristiques suivantes :  
  
-   Il représente logiquement une seule valeur, similaire aux types primitifs (`int`, `double`, etc..).  
  
-   Il a une taille d’instance inférieure à 16 octets.  
  
-   Il est immuable.  
  
-   Il n’aura pas à être converti (boxed) fréquemment.  
  
 Dans tous les autres cas, vous devez définir vos types comme classes.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions pour la conception des types](../../../docs/standard/design-guidelines/type.md)  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
