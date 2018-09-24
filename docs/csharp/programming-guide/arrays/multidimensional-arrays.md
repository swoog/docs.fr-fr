---
title: Tableaux multidimensionnels (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- arrays [C#], multidimensional
- multidimensional arrays [C#]
ms.assetid: 020ce02e-7dff-4273-8e53-bf0b33747232
ms.openlocfilehash: a1d7a0a014c330682316e869f6727082fa3b31ef
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "47027079"
---
# <a name="multidimensional-arrays-c-programming-guide"></a>Tableaux multidimensionnels (Guide de programmation C#)

Les tableaux peuvent avoir plusieurs dimensions. Par exemple, la déclaration suivante crée un tableau à deux dimensions composé de quatre lignes et deux colonnes.  
  
 [!code-csharp[csProgGuideArrays#11](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_1.cs)]  
  
 La déclaration suivante crée un tableau de trois dimensions, 4, 2 et 3.  
  
 [!code-csharp[csProgGuideArrays#12](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_2.cs)]  
  
## <a name="array-initialization"></a>Initialisation du tableau

 Vous pouvez initialiser le tableau au moment de la déclaration, comme le montre l’exemple suivant.  
  
 [!code-csharp[csProgGuideArrays#13](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_3.cs)]  
  
 Vous pouvez aussi initialiser le tableau sans spécifier de rang.  
  
 [!code-csharp[csProgGuideArrays#14](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_4.cs)]  
  
 Si vous choisissez de déclarer une variable de tableau sans initialisation, vous devez utiliser l’opérateur `new` pour assigner un tableau à la variable. L’utilisation de `new` est illustrée dans l’exemple suivant.  
  
 [!code-csharp[csProgGuideArrays#15](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_5.cs)]  
  
 L’exemple suivant assigne une valeur à un élément de tableau particulier.  
  
 [!code-csharp[csProgGuideArrays#16](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_6.cs)]  
  
 De la même manière, l’exemple suivant obtient la valeur d’un élément de tableau particulier et l’affecte à la variable `elementValue`.  
  
 [!code-csharp[csProgGuideArrays#42](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_7.cs)]  
  
 L’exemple de code suivant initialise les éléments de tableau avec les valeurs par défaut (sauf pour les tableaux en escalier).  
  
 [!code-csharp[csProgGuideArrays#17](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_8.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Tableaux](../../../csharp/programming-guide/arrays/index.md)  
- [Tableaux unidimensionnels](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)  
- [Tableaux en escalier](../../../csharp/programming-guide/arrays/jagged-arrays.md)
