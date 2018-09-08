---
title: Membres protégés
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- members [.NET Framework], protected
- protected members
- classes [.NET Framework], unsealed
- classes [.NET Framework], protected members
- unsealed classes
- customizing class behavior
ms.assetid: aa0b58ee-3956-494d-ab48-471ae5db8740
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4574dffc3f9dd1b60d655bfde33a4ddc1a81d350
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44140942"
---
# <a name="protected-members"></a>Membres protégés
Membres protégés par eux-mêmes ne fournissent pas de n’importe quel d’extensibilité, mais qu’ils puissent prendre extensibilité via sous-classement plus puissant. Ils peuvent être utilisés pour exposent des options de personnalisation avancée sans compliquer inutilement l’interface publique principale.  
  
 Concepteurs de Framework doivent être prudent avec les membres protégés, car le nom « protégé » peut donner un faux sentiment de sécurité. Toute personne est en mesure de sous-classe d’une classe unsealed et les membres de l’accès protégé, et par conséquent, les mêmes pratiques de codage défensifs utilisés pour les membres publics s’appliquent aux membres protégés.  
  
 **✓ CONSIDER** à l’aide de membres pour la personnalisation avancée protégés.  
  
 **✓ DO** considérer les membres protégés dans les classes unsealed comme public à des fins de sécurité, la documentation et compatibilité analysis.  
  
 Toute personne peut hériter d’une classe et accéder aux membres protégés.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
- [Conception en vue de l’extensibilité](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
