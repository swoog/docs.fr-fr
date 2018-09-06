---
title: Événements et rappels
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- events [.NET Framework], extensibility
- methods [.NET Framework], callback
- callback methods
- callbacks
ms.assetid: 48b55c60-495f-4089-9396-97f9122bba7c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 390c12af7107bb78fc261c55ea15390cf9eaa5b7
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43862947"
---
# <a name="events-and-callbacks"></a>Événements et rappels
Les rappels sont des points d’extensibilité qui permettent une infrastructure effectuer un rappel dans le code de l’utilisateur via un délégué. Ces délégués sont généralement transmises à l’infrastructure à un paramètre d’une méthode.  
  
 Les événements sont un cas spécial de rappels qui prend en charge la syntaxe pratique et cohérente pour fournir le délégué (un gestionnaire d’événements). En outre, saisie semi-automatique des instructions et les concepteurs de Visual Studio fournissent de l’aide à l’aide des API basées sur des événements. (Consultez [conception d’événements](../../../docs/standard/design-guidelines/event.md).)  
  
 **✓ CONSIDER** à l’aide des rappels pour permettre aux utilisateurs de fournir un code personnalisé doit être exécuté par l’infrastructure.  
  
 **✓ CONSIDER** à l’aide d’événements pour permettre aux utilisateurs de personnaliser le comportement d’une infrastructure sans avoir besoin pour comprendre la conception orientée objet.  
  
 **✓ DO** de préférence des événements via des rappels ordinaires, car ils sont plus facile pour un grand nombre de développeurs et sont intégrés à la fin de l’instruction Visual Studio.  
  
 **X AVOID** à l’aide de rappels dans les API sensibles aux performances.  
  
 **✓ DO** utiliser la nouvelle `Func<...>`, `Action<...>`, ou `Expression<...>` types à la place des délégués personnalisés lors de la définition d’API avec des rappels.  
  
 `Func<...>` et `Action<...>` représentent les délégués génériques. `Expression<...>` représente les définitions de fonction qui peuvent être compilées et appelées par la suite lors de l’exécution, mais peut également être sérialisées et transmies aux processus à distance.  
  
 **✓ DO** mesurer et comprendre les implications en matière de performances de l’utilisation de `Expression<...>`, au lieu d’utiliser `Func<...>` et `Action<...>` délégués.  
  
 `Expression<...>` les types sont dans la plupart des cas logiquement équivalente à `Func<...>` et `Action<...>` délégués. La principale différence est que les délégués sont destinées à être utilisées dans des scénarios de processus local. les expressions sont conçues pour les cas où il est possible d’évaluer l’expression dans un processus à distance ou de la machine et profitable.  
  
 **✓ DO** comprendre que par l’appel d’un délégué, vous exécutez du code arbitraire et qui pourraient avoir des répercussions de sécurité, d’exactitude et de compatibilité.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Conception en vue de l’extensibilité](../../../docs/standard/design-guidelines/designing-for-extensibility.md)  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
