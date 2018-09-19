---
title: Conception de classes statiques
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines, static classes
- class library design guidelines [.NET Framework], classes
- classes [.NET Framework], static
- static classes [.NET Framework]
- classes [.NET Framework], design guidelines
- type design guidelines, classes
ms.assetid: d67c14d8-c4dd-443f-affb-4ccae677c9b6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c3a0a51fc6055190f9a0189de2e17d98f88036ea
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "45972044"
---
# <a name="static-class-design"></a>Conception de classes statiques
Une classe statique est définie comme une classe qui contient uniquement des membres statiques (bien entendu, outre les membres d’instance hérités de <xref:System.Object?displayProperty=nameWithType> et éventuellement un constructeur privé). Certains langages fournissent la prise en charge intégrée pour les classes static. Dans c# 2.0 et versions ultérieures, quand une classe est déclarée comme statique, il est scellé, abstract, et aucun membre d’instance peut être remplacée ou déclaré.  
  
 Les classes statiques sont un compromis entre la conception orientée objet et la simplicité. Ils sont couramment utilisés pour fournir des raccourcis vers les autres opérations (telles que <xref:System.IO.File?displayProperty=nameWithType>), les détenteurs de méthodes d’extension ou de fonctionnalités pour lequel un wrapper orienté objet est injustifié (tel que <xref:System.Environment?displayProperty=nameWithType>).  
  
 **✓ DO** utilisent des classes statiques avec parcimonie.  
  
 Classes static doivent être utilisées uniquement comme prenant en charge de classes pour la core orientée objet du framework.  
  
 **X DO NOT** traiter des classes statiques comme un compartiment divers.  
  
 **X DO NOT** déclarer ou substituer des membres d’instance dans les classes static.  
  
 **✓ DO** déclarer des classes statiques comme sealed, abstract, et ajoutez un constructeur d’instance privée si votre langage de programmation ne dispose pas de prise en charge intégrée pour les classes static.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions pour la conception des types](../../../docs/standard/design-guidelines/type.md)  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
