---
title: return (référence C#)
ms.date: 07/20/2015
f1_keywords:
- return_CSharpKeyword
- return
helpviewer_keywords:
- return statement [C#]
- return keyword [C#]
ms.assetid: 6da6e152-5b58-4448-8f3f-470dd0617ecd
ms.openlocfilehash: 1b6a1ce2a8587c8630fece3d5c9a2186fbbc9c22
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "43001474"
---
# <a name="return-c-reference"></a>return (référence C#)
L’instruction `return` met un terme à l’exécution de la méthode dans laquelle elle apparaît et retourne le contrôle à la méthode d’appel. Elle peut également retourner une valeur facultative. Si la méthode est un type `void`, l’instruction `return` peut être omise.  
  
 Si l’instruction return est à l’intérieur d’un bloc `try`, le bloc `finally`, le cas échéant, est exécuté avant que le contrôle retourne à la méthode d’appel.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, la méthode `CalculateArea()` retourne la variable locale `area` en tant que valeur [double](../../../csharp/language-reference/keywords/double.md).  
  
 [!code-csharp[csrefKeywordsJump#6](../../../csharp/language-reference/keywords/codesnippet/CSharp/return_1.cs)]  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
- [Instruction return](/cpp/cpp/return-statement-cpp)  
- [Instructions de saut](../../../csharp/language-reference/keywords/jump-statements.md)
