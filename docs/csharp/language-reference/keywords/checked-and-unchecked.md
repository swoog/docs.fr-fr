---
title: Checked et Unchecked (référence C#)
ms.date: 07/20/2015
helpviewer_keywords:
- operators [C#], checked and unchecked
- exceptions [C#], overflow checking
- checked statement [C#]
- overflow checking [C#]
- unchecked statement [C#]
- statements [C#], checked and unchecked
ms.assetid: a84bc877-2c7f-4396-8735-1ce97c42f35e
ms.openlocfilehash: 26ea8a7864d93b8d64661db2b0dc1df6634f989a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="checked-and-unchecked-c-reference"></a>Checked et Unchecked (référence C#)
Les instructions C# peuvent s'exécuter dans un contexte vérifié (checked) ou non vérifié (unchecked). Dans un contexte vérifié, un dépassement de capacité arithmétique lève une exception. Dans un contexte non vérifié, un dépassement de capacité arithmétique et le résultat sont tronqués.  
  
-   [checked](../../../csharp/language-reference/keywords/checked.md) Indique un contexte vérifié.  
  
-   [unchecked](../../../csharp/language-reference/keywords/unchecked.md) Indique un contexte non vérifié.  
  
 Si ni `checked`, ni `unchecked` n'est spécifié, le contexte par défaut dépend de facteurs externes, notamment les options du compilateur.  
  
 Les opérations suivantes sont concernées par la vérification du dépassement de capacité :  
  
-   Expressions utilisant les opérateurs prédéfinis suivants dans des types intégraux :  
  
     `++` `--` - (unaire)   `+` -   `*` `/`  
  
-   Conversions numériques explicites entre types intégraux.  
  
 L’option de compilateur[/checked](../../../csharp/language-reference/compiler-options/checked-compiler-option.md) vous permet d’indiquer le contexte vérifié ou non vérifié pour toutes les instructions arithmétiques entières qui ne figurent pas explicitement dans l’étendue d’un mot clé`checked` ou `unchecked`.  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
 [Mots clés d’instructions](../../../csharp/language-reference/keywords/statement-keywords.md)
