---
title: Membres virtuels
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- overridable members
- virtual members
- members [.NET Framework], virtual
ms.assetid: 8ff4eb97-0364-43ec-8a02-934b5cd94d19
author: KrzysztofCwalina
ms.openlocfilehash: 4943ddcdf1bc4e3e32c8d664cbcc5c50ae3959bd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778701"
---
# <a name="virtual-members"></a>Membres virtuels
Membres virtuels peuvent être remplacées, ce qui modifie le comportement de la sous-classe. Ils sont assez semblables aux rappels en termes de l’extensibilité qu’ils fournissent, mais qu’ils sont mieux en termes de performances de l’exécution et la consommation de mémoire. En outre, les membres virtuels sembler plus naturelles dans les scénarios qui nécessitent la création de type d’un type existant (spécialisation) spécial.  
  
 Membres virtuels plus performant que les rappels et les événements, mais n’effectuent pas de meilleures performances que les méthodes non virtuelles.  
  
 Le principal inconvénient de membres virtuels est que le comportement d’un membre virtuel peut uniquement être modifié au moment de la compilation. Le comportement d’un rappel peut être modifié lors de l’exécution.  
  
 Les membres virtuels, telles que des rappels (et peut-être plusieurs rappels) sont coûteuses à concevoir, tester et mettre en place car un appel à un membre virtuel peut être substitué de manière imprévisible et peut exécuter du code arbitraire. En outre, plus beaucoup d’efforts est généralement requis pour définir clairement le contrat de membres virtuels, ce qui augmente le coût de conception et de les documenter.  
  
 **X DO NOT** rendre les membres virtuels sauf si vous avez une bonne raison à cela et que vous connaissez tous les coûts liés à la conception, de test et de maintenance des membres virtuels.  
  
 Membres virtuels sont moins indulgent en termes de modifications qui peuvent être apportées à leur sans perdre la compatibilité. En outre, ils sont plus lents que les membres non virtuelle, principalement parce que les appels aux membres virtuels ne sont pas inline.  
  
 **✓ CONSIDER** limiter l’extensibilité à celles qui sont absolument nécessaires.  
  
 **✓ DO** accessibilité protégée préférer une accessibilité publique pour les membres virtuels. Les membres publics doivent fournir l’extensibilité (si nécessaire) en appelant un membre virtuel protégé.  
  
 Les membres publics d’une classe doivent fournir l’ensemble approprié de fonctionnalités pour les consommateurs directs de cette classe. Membres virtuels sont conçus pour être substitué dans les sous-classes et accessibilité protégée est un excellent moyen pour définir l’étendue tous les points d’extension virtuel où ils peuvent être utilisés.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
- [Conception en vue de l’extensibilité](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
