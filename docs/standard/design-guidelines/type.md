---
title: Instructions de conception de types
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines
- type design guidelines, about type design guidelines
- class library design guidelines [.NET Framework], type design guidelines
- types [.NET Framework], design guidelines
ms.assetid: 6b49314e-8bba-43ea-97ca-4e0255812f95
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a7fb9964d0e542c0937c55ae65bd88b3f7149fa8
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44187937"
---
# <a name="type-design-guidelines"></a>Instructions de conception de types
À partir de la perspective du CLR, il existe uniquement deux catégories de types : types référence et les types valeur, mais à des fins une discussion sur la conception d’infrastructure, nous divisons types en groupes logiques de plus, chacun avec ses propres règles de conception spécifiques.  
  
 Les classes sont des types référence générale. Ils constituent la majeure partie des types dans la plupart des infrastructures. Classes à régler leur popularité pour la riche ensemble de fonctionnalités orientées objet, qu'ils prennent en charge et leur applicabilité générale. Classes de base et des classes abstraites sont des groupes logiques spéciales relatives à l’extensibilité.  
  
 Les interfaces sont des types qui peuvent être implémentées par les types référence et les types valeur. Elles peuvent donc servir racines des hiérarchies polymorphes des types référence et les types valeur. En outre, les interfaces peuvent être utilisées pour simuler l’héritage multiple, ce qui n’est pas pris en charge en mode natif par le CLR.  
  
 Les structs sont générale des types valeur et doit être réservés pour les types simples, similaires aux primitives de langage.  
  
 Les enums sont un cas spécial de types valeur utilisés pour définir des ensembles courts de valeurs, telles que les jours de la semaine, les couleurs de console et ainsi de suite.  
  
 Les classes statiques sont destinées à être des conteneurs pour les membres statiques de types. Ils sont souvent utilisés pour fournir des raccourcis vers les autres opérations.  
  
 Délégués, les exceptions, les attributs, les tableaux et les collections sont tous les cas spéciaux de types de référence destinées à des utilisations spécifiques, et les instructions pour leur conception et leur utilisation sont étudiées ailleurs dans ce livre.  
  
 **✓ DO** Vérifiez que chaque type est un ensemble bien défini de membres associés, pas seulement une collection aléatoire des fonctionnalités non liées.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Choix entre classe et structure](../../../docs/standard/design-guidelines/choosing-between-class-and-struct.md)  
 [Conception de classes abstraites](../../../docs/standard/design-guidelines/abstract-class.md)  
 [Conception de classes statiques](../../../docs/standard/design-guidelines/static-class.md)  
 [Conception d’interfaces](../../../docs/standard/design-guidelines/interface.md)  
 [Conception de structures](../../../docs/standard/design-guidelines/struct.md)  
 [Conception d’énumérations](../../../docs/standard/design-guidelines/enum.md)  
 [Types imbriqués](../../../docs/standard/design-guidelines/nested-types.md)  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
