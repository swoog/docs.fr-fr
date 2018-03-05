---
title: "Exemple d'expression régulière : recherche de valeurs HREF"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- searching with regular expressions, examples
- parsing text with regular expressions, examples
- regular expressions, examples
- .NET Framework regular expressions, examples
- regular expressions [.NET Framework], examples
- pattern-matching with regular expressions, examples
ms.assetid: fae2c15b-7adf-4b15-b118-58eb3906994f
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: c6da140ea82fc3c6d3f5f3001f37711ffe861370
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="regular-expression-example-scanning-for-hrefs"></a>Exemple d'expression régulière : recherche de valeurs HREF
L’exemple suivant recherche une chaîne d’entrée et affiche toutes les valeurs href="…" et leurs emplacements dans la chaîne.  
  
## <a name="the-regex-object"></a>Objet Regex  
 Étant donné que la méthode `DumpHRefs` peut être appelée plusieurs fois à partir du code utilisateur, la méthode <xref:System.Text.RegularExpressions.Regex.Match%28System.String%2CSystem.String%2CSystem.Text.RegularExpressions.RegexOptions%29?displayProperty=nameWithType> `static`(`Shared` dans Visual Basic) est utilisée. Ainsi, le moteur d’expression régulière peut mettre en cache l’expression régulière et éviter le traitement de l’instanciation d’un nouvel objet <xref:System.Text.RegularExpressions.Regex> chaque fois que la méthode est appelée. Un objet <xref:System.Text.RegularExpressions.Match> est alors utilisé pour effectuer une itération dans toutes les correspondances dans la chaîne.  
  
 [!code-csharp[RegularExpressions.Examples.HREF#1](../../../samples/snippets/csharp/VS_Snippets_CLR/RegularExpressions.Examples.HREF/cs/example.cs#1)]
 [!code-vb[RegularExpressions.Examples.HREF#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/RegularExpressions.Examples.HREF/vb/example.vb#1)]  
  
 L’exemple suivant illustre un appel à la méthode `DumpHRefs`.  
  
 [!code-csharp[RegularExpressions.Examples.HREF#2](../../../samples/snippets/csharp/VS_Snippets_CLR/RegularExpressions.Examples.HREF/cs/example.cs#2)]
 [!code-vb[RegularExpressions.Examples.HREF#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/RegularExpressions.Examples.HREF/vb/example.vb#2)]  
  
 Le modèle d'expression régulière `href\s*=\s*(?:["'](?<1>[^"']*)["']|(?<1>\S+))` est interprété comme indiqué dans le tableau suivant.  
  
|Motif|Description|  
|-------------|-----------------|  
|`href`|Correspond à la chaîne littérale « href ». La recherche de correspondance ne respecte pas la casse.|  
|`\s*`|Correspond à zéro, un ou plusieurs espaces blancs.|  
|`=`|Correspond au signe égal.|  
|`\s*`|Correspond à zéro, un ou plusieurs espaces blancs.|  
|`(?:["'](?<1>[^"']*)"&#124;(?<1>\S+))`|Correspond à l’un des éléments suivants sans assigner le résultat à un groupe capturé :<br /><br /> -   Un guillemet ou une apostrophe, suivi(e) de zéro, d’une ou de plusieurs occurrences de tout caractère autre qu’un guillemet ou une apostrophe, suivie(s) d’un guillemet ou d’une apostrophe. Le groupe nommé `1` est inclus dans ce modèle.<br />-   Un ou plusieurs caractères autres que des espaces blancs. Le groupe nommé `1` est inclus dans ce modèle.|  
|`(?<1>[^"']*)`|Affecte zéro, une ou plusieurs occurrences de tout caractère autre qu’un guillemet ou une apostrophe au groupe de capture nommé `1`.|  
|`"(?<1>\S+)`|Affecte un ou plusieurs caractères non espace blanc au groupe de capture nommé `1`.|  
  
## <a name="match-result-class"></a>Classe de résultats Match  
 Les résultats d’une recherche sont stockés dans la classe <xref:System.Text.RegularExpressions.Match>, qui donne accès à toutes les sous-chaînes extraites par la recherche. Cette classe mémorise également la chaîne recherchée et l’expression régulière utilisée, pour pouvoir appeler la méthode <xref:System.Text.RegularExpressions.Match.NextMatch%2A?displayProperty=nameWithType> afin d’effectuer une nouvelle recherche qui commence là où la dernière s’est terminée.  
  
## <a name="explicitly-named-captures"></a>Captures explicitement nommées  
 Dans les expressions régulières classiques, les parenthèses de capture sont automatiquement numérotées dans l’ordre. Cela génère deux problèmes. Tout d’abord, si une expression régulière est modifiée par l’insertion ou la suppression d’un jeu de parenthèses, tout code qui fait référence aux captures numérotées doit être réécrit pour refléter la nouvelle numérotation. Ensuite, étant donné que différents jeux de parenthèses sont souvent utilisés pour fournir deux expressions différentes pour une correspondance acceptable, il peut s’avérer difficile de déterminer laquelle des deux expressions en fait retourné un résultat.  
  
 Pour résoudre ces problèmes, la classe <xref:System.Text.RegularExpressions.Regex> prend en charge la syntaxe `(?<name>…)` pour capturer une correspondance dans un emplacement spécifié (l’emplacement peut être nommé à l’aide d’une chaîne ou d’un entier ; les entiers peuvent être rappelés plus rapidement). Ainsi, les autres correspondances de la même chaîne peuvent toutes être dirigées vers le même emplacement. En cas de conflit, la dernière correspondance placée dans un emplacement est la correspondance correcte. (Toutefois, la liste complète des différentes correspondances pour un seul emplacement est disponible. Consultez la collection <xref:System.Text.RegularExpressions.Group.Captures%2A?displayProperty=nameWithType> pour plus d’informations.)  
  
## <a name="see-also"></a>Voir aussi  
 [Expressions régulières .NET](../../../docs/standard/base-types/regular-expressions.md)
