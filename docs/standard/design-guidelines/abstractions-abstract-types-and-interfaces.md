---
title: Abstractions (Types et interfaces abstraits)
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- interfaces [.NET Framework], abstract
- abstract interfaces [.NET Framework]
- abstract types [.NET Framework]
- types [.NET Framework], abstract
ms.assetid: 0a632bc7-9b03-44ee-8842-c82f88672a45
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0ad8b2dd3dbf2a7a75c98a3115d4351dfea4e1a0
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44698358"
---
# <a name="abstractions-abstract-types-and-interfaces"></a>Abstractions (Types et interfaces abstraits)
Une abstraction est un type qui décrit un contrat, mais ne fournit pas une implémentation complète du contrat. Abstractions sont généralement implémentées comme des classes abstraites ou des interfaces, et ils sont livrés avec un ensemble bien défini de documentation de référence décrivant la sémantique requise des types qui implémente le contrat. Voici quelques-uns des abstractions plus importantes dans le .NET Framework <xref:System.IO.Stream>, <xref:System.Collections.Generic.IEnumerable%601>, et <xref:System.Object>.  
  
 Vous pouvez étendre des infrastructures en implémentant un type concret qui prend en charge le contrat d’une abstraction et de l’utilisation de ce type concret avec framework API consommateur (d’exploitation sur) l’abstraction.  
  
 Une abstraction significative et utile qui est en mesure de résister à l’épreuve du temps est très difficile de concevoir. La principale difficulté consiste à obtenir l’ensemble approprié de membres, pas plus et moins ne. Si une abstraction comporte trop de membres, il devient difficile, voire même d’implémenter. S’il a trop peu de membres pour la fonctionnalité Promise, il devient inutile dans de nombreux scénarios intéressants.  
  
 Trop d’abstractions dans une infrastructure également nuire facilité d’utilisation de l’infrastructure. Il est souvent très difficile de comprendre une abstraction sans avoir à comprendre comment elle s’adapte à l’image la plus grande des implémentations concrètes et les API d’exploitation sur l’abstraction. En outre, les noms des abstractions et leurs membres sont nécessairement abstraites, qui les rend difficiles à déchiffrer et difficiles à réaliser sans premier comprendre le contexte plus large de leur utilisation.  
  
 Toutefois, les abstractions fournissent extrêmement puissante d’extensibilité que les autres mécanismes d’extensibilité ne peut pas correspondre souvent. Ils sont au cœur de nombreux modèles architectures, tels que des plug-ins, inversion de contrôle (IoC), pipelines et ainsi de suite. Elles sont également extrêmement importants pour la testabilité de frameworks. Bonne abstractions permettent d’épargner des dépendances lourdes à des fins de tests unitaires. En résumé, les abstractions sont responsables de la richesse histoire des infrastructures et orienté objet modernes.  
  
 **X DO NOT** fournissent des abstractions, sauf si elles sont testées par le développement de plusieurs implémentations concrètes et consomme les abstractions des API.  
  
 **✓ DO** choisir entre une classe abstraite et une interface avec soin lors de la conception d’une abstraction.  
  
 **✓ CONSIDER** fournissant des tests de référence pour les implémentations concrètes d’abstractions. Ces tests doivent autoriser les utilisateurs à déterminer si leurs implémentations implémentent correctement le contrat.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
- [Conception en vue de l’extensibilité](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
