---
title: Conception de classes abstraites
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines, abstract classes
- abstract classes, design guidelines
- class library design guidelines [.NET Framework], classes
- classes [.NET Framework], abstract
- classes [.NET Framework], design guidelines
- type design guidelines, classes
ms.assetid: d3646e6d-5c1f-4922-8fb0-ec5effb30d60
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c5b9dacc4995a126e1ee3f6062dca796194d4882
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45519180"
---
# <a name="abstract-class-design"></a>Conception de classes abstraites
**X DO NOT** définir des constructeurs internes publiques ou protégées dans les types abstraits.  
  
 Les constructeurs doivent être publics uniquement si les utilisateurs devront créer des instances du type. Étant donné que vous ne pouvez pas créer des instances d’un type abstrait, un type abstrait avec un constructeur public est correctement conçu et trompeur aux utilisateurs.  
  
 **✓ DO** définir un document protégé ou un constructeur interne dans les classes abstraites.  
  
 Un constructeur protégé est plus courant et il permet simplement de la classe de base pour son propre initialisation lorsque des sous-types sont créés.  
  
 Un constructeur interne peut être utilisé pour limiter les implémentations concrètes de la classe abstraite pour l’assembly qui définit la classe.  
  
 **✓ DO** fournir au moins un type concret qui hérite de chaque classe abstraite qui vous sont fournis.  
  
 Ceci permet de valider la conception de la classe abstraite. Par exemple, <xref:System.IO.FileStream?displayProperty=nameWithType> est une implémentation de la <xref:System.IO.Stream?displayProperty=nameWithType> classe abstraite.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions pour la conception des types](../../../docs/standard/design-guidelines/type.md)  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
