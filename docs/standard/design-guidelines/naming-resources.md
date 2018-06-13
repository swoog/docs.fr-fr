---
title: Attribution d'un nom à des ressources
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], localized resources
- localization, naming guidelines
- resource names
- global applications, naming guidelines
- international applications, naming guidelines
ms.assetid: 8b0e97f3-7877-44fd-bc76-e05d36d5d79c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b7cfda4e6a340d040de02903b9b64f0339751c5c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33571184"
---
# <a name="naming-resources"></a>Attribution d'un nom à des ressources
Étant donné que les ressources localisables peuvent être référencés via certains objets comme s’ils étaient des propriétés, les instructions d’affectation de noms pour les ressources sont semblables aux instructions de la propriété.  
  
 **✓ FAIRE** utilisent la casse Pascal dans les clés de ressources.  
  
 **✓ FAIRE** fournir descriptif au lieu d’identificateurs courts.  
  
 **X ne sont pas** utiliser des mots clés de langage spécifique langage CLR principal.  
  
 **✓ FAIRE** utiliser uniquement des caractères alphanumériques et des traits de soulignement dans les noms des ressources.  
  
 **✓ FAIRE** utilisent la convention d’affectation de noms suivante pour les ressources de message d’exception.  
  
 L’identificateur de ressource doit être le nom de type d’exception plus un identificateur court de l’exception :  
  
 `ArgumentExceptionIllegalCharacters`  
 `ArgumentExceptionInvalidName`  
 `ArgumentExceptionFileNameIsMalformed`  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimées avec l’autorisation de Pearson éducation, Inc. à partir de [règles de conception d’infrastructure : Conventions, idiomes et des modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi  
 [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
 [Directives de nommage](../../../docs/standard/design-guidelines/naming-guidelines.md)
