---
title: méthodes d’extension.
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 5de945cb-88f4-49d7-b0e6-f098300cf357
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6bfc2e6def94d0830df4a4cdf738cdeef106de9f
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44265245"
---
# <a name="extension-methods"></a>méthodes d’extension.
Méthodes d’extension sont une fonctionnalité de langage qui permet des méthodes statiques pour être appelée à l’aide de la syntaxe de méthode d’appel d’instance. Ces méthodes doivent disposer d’au moins un paramètre, qui représente l’instance de que la méthode consiste à utiliser.  
  
 La classe qui définit des méthodes d’extension correspond à la classe « parrain », et elle doit être déclarée comme statique. Pour utiliser les méthodes d’extension, un doit importer l’espace de noms définition de la classe de sponsor.  
  
 **X AVOID** leurs intentions soient amicales définissant les méthodes d’extension, en particulier sur les types que vous ne possédez pas.  
  
 Si vous possédez le code source d’un type, envisagez d’utiliser les méthodes d’instance normale à la place. Si vous n’êtes pas propriétaire, et que vous souhaitez ajouter une méthode, soyez très prudent. L’utilisation répandue des méthodes d’extension a le potentiel d’encombrer les API de types qui n’ont pas été conçues pour que ces méthodes.  
  
 **✓ CONSIDER** à l’aide des méthodes d’extension dans un des scénarios suivants :  
  
-   Pour fournir d’assistance fonctionnalités pertinentes pour chaque implémentation d’une interface, si vous dit de fonctionnalités peuvent être écrits en termes de l’interface principale. Il s’agit, car les implémentations concrètes sinon ne peut pas être attribuées aux interfaces. Par exemple, le `LINQ to Objects` opérateurs sont implémentées en tant que méthodes d’extension pour tous les <xref:System.Collections.Generic.IEnumerable%601> types. Par conséquent, les `IEnumerable<>` implémentation est automatiquement prenant en charge LINQ.  
  
-   Quand une méthode d’instance créerait une dépendance sur un type, mais une telle dépendance ne fonctionneraient pas les règles de gestion de dépendance. Par exemple, une dépendance à partir de <xref:System.String> à <xref:System.Uri?displayProperty=nameWithType> n’est pas souhaitable et donc `String.ToUri()` retour de méthode d’instance `System.Uri` serait la conception incorrecte à partir d’un point de vue de gestion de dépendance. Une méthode d’extension statique `Uri.ToUri(this string str)` retournant `System.Uri` serait une bien meilleure conception.  
  
 **X AVOID** définition des méthodes d’extension sur <xref:System.Object?displayProperty=nameWithType>.  
  
 Les utilisateurs de Visual Basic ne sera pas en mesure d’appeler des méthodes sur les références d’objet à l’aide de la syntaxe de méthode d’extension. VB ne prend pas en charge l’appel de ces méthodes, car, en VB, déclaration comme objet force tous les appels de méthode dessus en retard d’une référence liée (appelé de membre réel est déterminé lors de l’exécution), tandis que les liaisons aux méthodes d’extension sont déterminés au moment de la compilation (anticipée lié).  
  
 Notez que la règle s’applique à d’autres langages où se trouve le même comportement de liaison, ou dans lequel les méthodes d’extension ne sont pas pris en charge.  
  
 **X DO NOT** méthodes d’extension dans le même espace de noms en tant que le type étendu est utilisée pour ajouter des méthodes aux interfaces ou pour la gestion des dépendances.  
  
 **X AVOID** définissant deux ou plusieurs méthodes d’extension avec la même signature, même s’ils résident dans différents espaces de noms.  
  
 **✓ CONSIDER** définition des méthodes d’extension dans le même espace de noms en tant que le type étendu si le type est une interface et si les méthodes d’extension sont destinés à être utilisés dans la plupart des cas.  
  
 **X DO NOT** définir des méthodes d’extension mise en œuvre d’une fonctionnalité dans les espaces de noms normalement avec d’autres fonctionnalités. Au lieu de cela, les définir dans l’espace de noms associé à la fonctionnalité qu'auquel ils appartiennent.  
  
 **X AVOID** générique d’affectation de noms d’espaces de noms dédié aux méthodes d’extension (par exemple, « Extensions »). Utilisez un nom descriptif (par exemple, « routage ») à la place.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions de conception des membres](../../../docs/standard/design-guidelines/member.md)  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
