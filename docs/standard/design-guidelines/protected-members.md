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
ms.openlocfilehash: 5d4d334d9809f374442e19807d3b249a17a1d9df
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33571083"
---
# <a name="protected-members"></a>Membres protégés
Les membres protégés par eux-mêmes ne fournissent pas de n’importe quel d’extensibilité, mais elles peuvent rendre les extensibilité via le sous-classement plus puissant. Ils peuvent être utilisés pour exposer les options de personnalisation avancée sans compliquer inutilement de l’interface publique principale.  
  
 Concepteurs de Framework doivent être prudent avec les membres protégés, car le nom « protégé » peut donner un sentiment de sécurité. Toute personne est en mesure de sous-classe d’une classe unsealed et les membres de l’accès protégé, et par conséquent, les mêmes défensives pratiques de codage utilisés pour les membres publics s’appliquent à des membres protégés.  
  
 **✓ Envisagez** à l’aide de membres pour la personnalisation avancée protégés.  
  
 **✓ FAIRE** considérer les membres protégés dans les classes unsealed comme public à des fins de sécurité, la documentation et compatibilité analysis.  
  
 Toute personne peut hériter d’une classe et accéder aux membres protégés.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimées avec l’autorisation de Pearson éducation, Inc. à partir de [règles de conception d’infrastructure : Conventions, idiomes et des modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi  
 [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
 [Conception en vue de l’extensibilité](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
