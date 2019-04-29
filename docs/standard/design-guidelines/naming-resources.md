---
title: Attribution d'un nom à des ressources
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], localized resources
- localization, naming guidelines
- resource names
- global applications, naming guidelines
- international applications, naming guidelines
ms.assetid: 8b0e97f3-7877-44fd-bc76-e05d36d5d79c
author: KrzysztofCwalina
ms.openlocfilehash: 44627aafd9ec779625413a0862412a8f6c408109
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61756882"
---
# <a name="naming-resources"></a>Attribution d'un nom à des ressources
Étant donné que les ressources localisables peuvent être référencés par le biais de certains objets comme s’ils étaient des propriétés, les instructions d’affectation de noms pour les ressources sont similaires aux instructions de la propriété.  
  
 **✓ DO** utilisent la casse Pascal dans les clés de ressources.  
  
 **✓ DO** fournir descriptif au lieu d’identificateurs courts.  
  
 **X DO NOT** utiliser des mots clés de langage spécifique langage CLR principal.  
  
 **✓ DO** utiliser uniquement des caractères alphanumériques et des traits de soulignement dans les noms des ressources.  
  
 **✓ DO** utilisent la convention d’affectation de noms suivante pour les ressources de message d’exception.  
  
 L’identificateur de ressource doit être le nom du type exception ainsi qu’un identificateur court de l’exception :  
  
 `ArgumentExceptionIllegalCharacters`  
 `ArgumentExceptionInvalidName`  
 `ArgumentExceptionFileNameIsMalformed`  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
- [Directives de nommage](../../../docs/standard/design-guidelines/naming-guidelines.md)
