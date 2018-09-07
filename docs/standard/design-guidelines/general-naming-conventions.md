---
title: Conventions générales d'affectation de noms
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], conflicts
- type names, conflicts
- language-specific type names
- names [.NET Framework], about naming guidelines
- names [.NET Framework], abbreviations
- abbreviation naming guidelines
- acronym naming guidelines
- Hungarian notation
- names [.NET Framework], type names
- names [.NET Framework], acronyms
ms.assetid: d3a77ea1-75d2-4969-a8c3-3e1e3e1aaedc
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cd3defd969b5f26fb95e7feca9c3d533e67272b1
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44071094"
---
# <a name="general-naming-conventions"></a>Conventions générales d'affectation de noms
Cette section décrit les conventions générales de nommage qui se rapportent au choix de word, les instructions sur l’utilisation d’abréviations et acronymes et des recommandations sur la façon d’éviter d’utiliser des noms spécifiques au langage.  
  
## <a name="word-choice"></a>Choix des mots  
 **✓ DO** choisir des noms d’identificateurs lisibles.  
  
 Par exemple, une propriété nommée `HorizontalAlignment` est plus anglais-lisible que `AlignmentHorizontal`.  
  
 **✓ DO** privilégier la lisibilité des raisons de concision.  
  
 Le nom de propriété `CanScrollHorizontally` est meilleure que `ScrollableX` (une référence à l’axe des x).  
  
 **X DO NOT** utiliser d’autres caractères non alphanumériques, des traits d’union ou des traits de soulignement.  
  
 **X DO NOT** utilisent une notation hongroise.  
  
 **X AVOID** à l’aide d’identificateurs qui entrent en conflit avec les mots clés de largement utilisé des langages de programmation.  
  
 En fonction de la règle 4 de la Common Language Specification (CLS), tous les langages conformes à doivent fournir un mécanisme qui permet d’accéder à des éléments nommés qui utilisent un mot clé de cette langue en tant qu’identificateur. C#, par exemple, utilise le signe comme un mécanisme d’échappement dans ce cas @. Toutefois, il est toujours une bonne idée pour éviter les mots clés courants, car il est beaucoup plus difficile d’utiliser une méthode avec la séquence d’échappement à l’autre sans.  
  
## <a name="using-abbreviations-and-acronyms"></a>À l’aide des abréviations et acronymes  
 **X DO NOT** utiliser des abréviations ou contractions comme faisant partie des noms d’identificateur.  
  
 Par exemple, utilisez `GetWindow` plutôt que `GetWin`.  
  
 **X DO NOT** utiliser des acronymes ne sont pas largement reconnue et même si elles sont uniquement lorsque cela est nécessaire.  
  
## <a name="avoiding-language-specific-names"></a>Éviter les noms spécifiques au langage  
 **✓ DO** utiliser des noms sémantiquement intéressants plutôt que des mots clés spécifiques à la langue pour les noms de type.  
  
 Par exemple, `GetLength` est un meilleur nom que `GetInt`.  
  
 **✓ DO** utiliser un nom de type CLR générique, plutôt que d’un nom spécifique au langage, dans les rares cas où un identificateur n’a aucune signification sémantique au-delà de son type.  
  
 Par exemple, une méthode de conversion en <xref:System.Int64> doit être nommé `ToInt64`, et non `ToLong` (étant donné que <xref:System.Int64> est un nom CLR pour c#-alias spécifique `long`). Le tableau suivant présente plusieurs types de base de données à l’aide des noms de types CLR (comme les noms de type correspondant pour c#, Visual Basic et C++).  
  
|C#|Visual Basic|C++|CLR|  
|---------|------------------|-----------|---------|  
|**sbyte**|**SByte**|**char**|**SByte**|  
|**byte**|**Byte**|**unsigned char**|**Byte**|  
|**short**|**short**|**short**|**Int16**|  
|**ushort**|**UInt16**|**unsigned short**|**UInt16**|  
|**int**|**Integer**|**int**|**Int32**|  
|**uint**|**UInt32**|**unsigned int**|**UInt32**|  
|**long**|**Long**|**__int64**|**Int64**|  
|**ulong**|**UInt64**|**unsigned __int64**|**UInt64**|  
|**float**|**Single**|**float**|**Single**|  
|**double**|**Double**|**double**|**Double**|  
|**bool**|**Boolean**|**bool**|**Boolean**|  
|**char**|**Char**|**wchar_t**|**Char**|  
|**string**|**String**|**String**|**String**|  
|**object**|**Objet**|**Objet**|**Objet**|  
  
 **✓ DO** utiliser un nom commun, tel que `value` ou `item`, plutôt que de répéter le nom de type dans les rares cas où un identificateur n’a aucune signification sémantique et le type du paramètre n’est pas important.  
  
## <a name="naming-new-versions-of-existing-apis"></a>D’affectation de noms de nouvelles Versions d’API existantes  
 **✓ DO** utiliser un nom semblable à l’ancien API lors de la création de nouvelles versions d’une API existante.  
  
 Cela permet de mettre en évidence la relation entre les API.  
  
 **✓ DO** préférez l’ajout d’un suffixe au lieu d’un préfixe pour indiquer une nouvelle version d’une API existante.  
  
 Cela permet d’aider découverte lorsque vous parcourez la documentation, ou à l’aide d’IntelliSense. L’ancienne version de l’API est organisée près les nouvelles API, car la plupart des navigateurs et IntelliSense affichent les identificateurs dans l’ordre alphabétique.  
  
 **✓ CONSIDER** à l’aide d’un identificateur de tout nouveau, mais significatif, au lieu d’ajouter un préfixe ou un suffixe.  
  
 **✓ DO** un suffixe numérique permet d’indiquer une nouvelle version d’une API existante, en particulier si le nom existant de l’API est le seul nom logique (par exemple, si elle est une norme sectorielle) et si l’ajout explicite tout suffixe (ou la modification du nom) n’est pas une application option de ropriate.  
  
 **X DO NOT** utiliser le « Ex » (ou un texte similaire) suffixe pour un identificateur pour le distinguer d’une version antérieure de la même API.  
  
 **✓ DO** utiliser le suffixe « 64 » lorsque vous introduisez des versions d’API qui fonctionnent sur un entier 64 bits (un entier long) au lieu d’un entier 32 bits. Il vous suffit de suivre cette approche lors de l’API de 32 bits existante existe ; ne le faites pour toute nouvel API avec uniquement une version 64 bits.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
- [Directives de nommage](../../../docs/standard/design-guidelines/naming-guidelines.md)
