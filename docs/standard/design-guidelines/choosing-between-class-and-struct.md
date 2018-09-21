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
Une des décisions de conception de base auxquelles est confronté chaque concepteur de framework est de concevoir un type sous forme de classe (type référence) ou sous forme de struct (type valeur). Il est nécessaire de bien comprendre les différences de comportement entre les types référence et les types valeur pour faire ce choix.  
  
 La première différence entre les types référence et les types valeur que nous considérerons est que les types référence sont alloués sur la pile et récupérés par le récupérateur de mémoire, alors que les types valeur sont alloués sur la pile ou en ligne dans les types conteneurs, et désalloués quand la pile se déroule ou quand leur type conteneur est désalloué. Par conséquent, les allocations et les désallocations des types valeur sont en général moins coûteuses en ressources que les allocations et désallocations des types référence.  
  
 Ensuite, les tableaux de types référence sont alloués hors ligne, ce qui signifie que les éléments du tableau sont simplement des références à des instances de type référence présentes dans la pile. Les tableaux de types valeur sont alloués en ligne, ce qui signifie que les éléments du tableau sont les instances réelles du type valeur. Par conséquent, les allocations et les désallocations de tableaux de types valeur sont beaucoup moins coûteuses en ressources que les allocations et les désallocations de tableaux de types référence. En outre, dans la plupart des cas, les tableaux de types valeur présentent une bien meilleure localité des références.  
  
 La différence suivante est liée à l’utilisation de la mémoire. Les types valeur subissent un boxing lors du cast en un type référence ou en une des interfaces qu’ils implémentent. Ils subissent un unboxing quand ils sont recastés en type valeur. Comme les box sont des objets qui sont alloués à la pile et récupérés par le récupérateur de mémoire, trop de boxing et d’unboxing peut avoir un impact négatif sur la pile, sur le récupérateur de mémoire et au final sur les performances de l’application.  En revanche, aucun boxing de ce type ne se produit quand des types référence sont castés.  
  
 Ensuite, les affectations de type référence copient la référence, tandis que les affectations de type valeur copient la valeur entière. Par conséquent, les affectations de types référence de grande taille sont moins coûteuses en ressources que les affectations de types valeur de grande taille.  
  
 Enfin, les types référence sont passés par référence, tandis que les types valeur sont passés par valeur. Les modifications apportées à une instance d’un type référence affectent toutes les références pointant vers l’instance. Les instances de types valeur sont copiées quand elles sont passées par valeur. Quand une instance d’un type valeur est modifiée, cela n’affecte bien sûr pas ses copies. Comme les copies ne sont pas créées explicitement par l’utilisateur, mais sont créées implicitement quand des arguments sont passés ou que des valeurs sont retournées, les types valeur qui peuvent être modifiés peuvent créer de la confusion pour de nombreux utilisateurs. Par conséquent, les types valeur devraient être immuables.  
  
 D’une façon générale, la majorité des types d’un framework devraient être des classes. Cependant, il existe certaines situations dans lesquelles les caractéristiques d’un type valeur font qu’il est plus approprié d’utiliser des structs.  
  
 **✓ CONSIDER** de définir un struct au lieu d’une classe si les instances du type sont de petite taille et d’une durée de vie assez courte, ou si elles sont souvent incorporées dans d’autres objets.  
  
 **X AVOID** définition d’un struct, sauf si le type possède toutes les caractéristiques suivantes :  
  
-   Il représente logiquement une seule valeur, similaire aux types primitifs (`int`, `double`, etc..).  
  
-   Il a une taille d’instance inférieure à 16 octets.  
  
-   Il est immuable.  
  
-   Il n’aura pas à subir fréquemment des opérations de boxing.  
  
 Dans tous les autres cas, vous devez définir vos types comme classes.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions pour la conception des types](../../../docs/standard/design-guidelines/type.md)  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
