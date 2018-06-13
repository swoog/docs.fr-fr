---
title: partielle, méthode (Référence C#)
ms.date: 07/20/2015
f1_keywords:
- partialmethod_CSharpKeyword
helpviewer_keywords:
- partial methods [C#]
ms.assetid: 43f40242-17e0-4452-8573-090503ad3137
ms.openlocfilehash: 29b5d442a1aa33babc24aee987e749c93a5ec727
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33269039"
---
# <a name="partial-method-c-reference"></a>partielle, méthode (Référence C#)
La signature d’une méthode partielle est définie dans une partie d’un type partiel, tandis que son implémentation est définie dans une autre partie du type. Les méthodes partielles permettent aux concepteurs de classes de fournir des hooks de méthode, semblables aux gestionnaires d’événements, que les développeurs peuvent décider ou non d’implémenter. Si le développeur ne fournit pas d’implémentation, le compilateur supprime la signature au moment de la compilation. Les méthodes partielles obéissent aux conditions suivantes :  
  
-   Les signatures des deux parties du type partiel doivent correspondre.  
  
-   La méthode doit retourner void.  
  
-   Aucun modificateur d’accès n’est autorisé. Les méthodes partielles sont implicitement privées.  
  
 L’exemple suivant illustre une méthode partielle définie dans deux parties d’une classe partielle :  
  
 [!code-csharp[csrefKeywordsContextual#9](../../../csharp/language-reference/keywords/codesnippet/CSharp/partial-method_1.cs)]  
  
 Pour plus d’informations, consultez [Classes et méthodes partielles](../../../csharp/programming-guide/classes-and-structs/partial-classes-and-methods.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [partial (type)](../../../csharp/language-reference/keywords/partial-type.md)
