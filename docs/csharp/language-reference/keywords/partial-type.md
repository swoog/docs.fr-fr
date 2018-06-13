---
title: partial, type (référence C#)
ms.date: 07/20/2015
f1_keywords:
- partialtype
- partialtype_CSharpKeyword
helpviewer_keywords:
- partial types [C#]
ms.assetid: 27320743-a22e-4c7b-b0b3-53afe3607334
ms.openlocfilehash: 4f57149dd18deb08aa11b72d0a6d5f71b3838bd1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33266687"
---
# <a name="partial-type-c-reference"></a>partial, type (référence C#)
Les définitions de type partiel permettent le fractionnement de la définition d’une classe, d’un struct ou d’une interface entre plusieurs fichiers.  
  
 Dans File1.cs :  
  
 [!code-csharp[csrefKeywordsContextual#3](../../../csharp/language-reference/keywords/codesnippet/CSharp/partial-type_1.cs)]  
  
 Déclaration dans File2.cs :  
  
 [!code-csharp[csrefKeywordsContextual#4](../../../csharp/language-reference/keywords/codesnippet/CSharp/partial-type_2.cs)]  
  
## <a name="remarks"></a>Notes  
 Fractionner un type de classe, de struct ou d’interface entre plusieurs fichiers peut être utile si vous travaillez sur des projets volumineux ou des projets contenant du code généré automatiquement, comme celui fourni par le [Concepteur Windows Forms](../../../framework/winforms/controls/developing-windows-forms-controls-at-design-time.md). Un type partiel peut contenir une [méthode partielle](../../../csharp/language-reference/keywords/partial-method.md). Pour plus d’informations, consultez [Classes et méthodes partielles](../../../csharp/programming-guide/classes-and-structs/partial-classes-and-methods.md).  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Modificateurs](../../../csharp/language-reference/keywords/modifiers.md)  
 [Introduction aux génériques](../../../csharp/programming-guide/generics/introduction-to-generics.md)
