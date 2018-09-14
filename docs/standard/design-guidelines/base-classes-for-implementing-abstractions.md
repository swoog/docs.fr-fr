---
title: Classes de base pour l'implémentation d'abstractions
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- abstractions [.NET Framework]
- base classes, abstractions
ms.assetid: 37a2d9a4-9721-482a-a40f-eee2c1d97875
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9f326ee895251678c7a23ea84a11e83951edf2cc
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45519469"
---
# <a name="base-classes-for-implementing-abstractions"></a>Classes de base pour l'implémentation d'abstractions
À proprement parler, une classe devient une classe de base lorsqu’une autre classe est dérivée à partir de celui-ci. Pour les besoins de cette section, toutefois, une classe de base est une classe principalement conçue pour fournir une abstraction commune ou pour d’autres classes de réutiliser une partie implémentation cependant l’héritage par défaut. Classes de base se trouvent généralement au milieu des hiérarchies d’héritage entre une abstraction à la racine d’une hiérarchie et plusieurs implémentations personnalisées en bas.  
  
 Ils servent helpers d’implémentation pour l’implémentation d’abstractions. Par exemple, une des abstractions de l’infrastructure pour les collections ordonnées d’éléments est le <xref:System.Collections.Generic.IList%601> interface. Implémentation <xref:System.Collections.Generic.IList%601> n’est pas simple, et par conséquent le Framework fournit plusieurs classes de base, telles que <xref:System.Collections.ObjectModel.Collection%601> et <xref:System.Collections.ObjectModel.KeyedCollection%602>, faisant office de programmes d’assistance pour l’implémentation des regroupements personnalisés.  
  
 Classes de base ne sont généralement pas adaptées pour servir les abstractions par eux-mêmes, car ils ont tendance à contenir trop implémentation. Par exemple, le `Collection<T>` classe de base contient un grand nombre d’implémentation lié au fait qu’il implémente non générique `IList` interface (pour mieux s’intégrer avec les collections non génériques) et au fait qu’il est une collection d’éléments stockés dans mémoire dans un de ses champs.  
  
 Comme indiqué précédemment, les classes de base peuvent fournir une aide précieuse aux utilisateurs qui ont besoin pour implémenter des abstractions, mais en même temps, ils peuvent être une responsabilité importante. Ils ajouter la surface d’exposition et augmenter la profondeur des hiérarchies d’héritage et donc conceptuellement compliquent l’infrastructure. Par conséquent, les classes de base doivent être utilisés uniquement si ils fournissent une valeur ajoutée significative pour les utilisateurs de l’infrastructure. Ils doivent être évités s’ils fournissent la valeur uniquement pour les implémenteurs de l’infrastructure, dans lequel cas délégation vers une implémentation interne au lieu de l’héritage à partir d’une classe de base fortement prenez en compte.  
  
 **✓ CONSIDER** les classes de base en abstraite même s’ils ne contiennent aucun membre abstrait. Clairement aux utilisateurs que la classe doit uniquement être héritée.  
  
 **✓ CONSIDER** en plaçant des classes de base dans un espace de noms distinct à partir des types de scénario principal. Par définition, classes de base destinées aux scénarios d’extensibilité avancée et par conséquent, ne sont pas intéressants de la majorité des utilisateurs.  
  
 **X AVOID** d’affectation de noms des classes de base avec un suffixe « Base » si la classe est destinée à être utilisée dans les API publiques.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
- [Conception en vue de l’extensibilité](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
