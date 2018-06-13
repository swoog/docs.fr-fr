---
title: Espaces de noms (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, namespaces
- namespaces [C#]
ms.assetid: b1c4ab46-3fad-4ffa-9deb-dd50a2d8c65a
ms.openlocfilehash: 60e4c6e98ca9e71d1a095a0c7ee1df6be6d13f4b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33334348"
---
# <a name="namespaces-c-programming-guide"></a>Espaces de noms (Guide de programmation C#)
Les espaces de noms sont largement utilisés de deux façons dans la programmation avec C#. Premièrement, le .NET Framework utilise des espaces de noms pour organiser ses nombreuses classes, comme suit :  
  
 [!code-csharp[csProgGuide#22](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/index_1.cs)]  
  
 `System` est un espace de noms et `Console` est une classe de cet espace de noms. Vous pouvez utiliser le mot clé `using`. Ainsi, le nom complet n’est pas obligatoire, comme dans l’exemple suivant :  
  
 [!code-csharp[csProgGuide#1](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/index_2.cs)]  
  
 [!code-csharp[csProgGuide#25](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/index_3.cs)]  
  
 Pour plus d’informations, consultez [using, directive](../../../csharp/language-reference/keywords/using-directive.md).  
  
 Deuxièmement, la déclaration de vos propres espaces de noms peut vous aider à contrôler l’étendue des noms de classes et de méthodes dans les projets de programmation plus vastes. Utilisez le mot clé [namespace](../../../csharp/language-reference/keywords/namespace.md) pour déclarer un espace de noms, comme dans l’exemple suivant :  
  
 [!code-csharp[csProgGuideNamespaces#6](../../../csharp/programming-guide/namespaces/codesnippet/CSharp/index_4.cs)]  
  
## <a name="namespaces-overview"></a>Vue d'ensemble des espaces de noms  
 Les espaces de noms ont les propriétés suivantes :  
  
-   Ils organisent les projets de code de taille importante.  
  
-   Ils sont délimités à l’aide de l’opérateur `.`.  
  
-   La `using directive` évite de devoir spécifier le nom de l’espace de noms pour chaque classe.  
  
-   L’espace de noms `global` est l’espace de noms « racine » : `global::System` fait toujours référence à l’espace de noms `System` du .NET Framework.  
  
## <a name="related-sections"></a>Rubriques connexes  
 Pour plus d’informations sur les espaces de noms, consultez les rubriques suivantes :  
  
-   [Utilisation d’espaces de noms](../../../csharp/programming-guide/namespaces/using-namespaces.md)  
  
-   [Comment : utiliser l’alias d’espace de noms global](../../../csharp/programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)  
  
-   [Comment : utiliser l’espace de noms My](../../../csharp/programming-guide/namespaces/how-to-use-the-my-namespace.md)  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Mots clés d’espaces de noms](../../../csharp/language-reference/keywords/namespace-keywords.md)  
 [using, directive](../../../csharp/language-reference/keywords/using-directive.md)  
 [:: (opérateur)](../../../csharp/language-reference/operators/namespace-alias-qualifer.md)  
 [. Opérateur](../../../csharp/language-reference/operators/member-access-operator.md)
