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
ms.openlocfilehash: 92152600d317c04e3fef26400b11e94a549fde4c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33571057"
---
# <a name="static-class-design"></a>Conception de classes statiques
Une classe statique est définie comme une classe qui contient uniquement des membres statiques (bien entendu, outre les membres d’instance héritées <xref:System.Object?displayProperty=nameWithType> et éventuellement un constructeur privé). Certains langages fournissent une prise en charge intégrée pour les classes static. En c# 2.0 et versions ultérieures, lorsqu’une classe est déclarée comme étant statique, il est sealed, abstract, et aucun membre d’instance peut être substituée ou déclaré.  
  
 Les classes statiques sont un compromis entre pure conception orientée objet et la simplicité. Ils sont couramment utilisés pour fournir des raccourcis à d’autres opérations (telles que <xref:System.IO.File?displayProperty=nameWithType>), titulaires de méthodes d’extension ou de fonctionnalités pour lequel un wrapper orienté objet est injustifié (tel que <xref:System.Environment?displayProperty=nameWithType>).  
  
 **✓ FAIRE** utilisent des classes statiques avec parcimonie.  
  
 Les classes static doivent être utilisés uniquement comme classes de prise en charge pour le noyau orientée objet de l’infrastructure.  
  
 **X ne sont pas** traiter des classes statiques comme un compartiment divers.  
  
 **X ne sont pas** déclarer ou substituer des membres d’instance dans les classes static.  
  
 **✓ FAIRE** déclarer des classes statiques comme sealed, abstract, et ajoutez un constructeur d’instance privée si votre langage de programmation ne dispose pas de prise en charge intégrée pour les classes static.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimées avec l’autorisation de Pearson éducation, Inc. à partir de [règles de conception d’infrastructure : Conventions, idiomes et des modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi  
 [Instructions pour la conception des types](../../../docs/standard/design-guidelines/type.md)  
 [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
