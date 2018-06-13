---
title: Structures (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, structs
- structs [C#]
ms.assetid: b7cf4ff2-0eb7-4e5c-93d5-b2196b4f5d89
ms.openlocfilehash: ffb5b8da6c72056620cf890f38af4e7a8116ab3e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33322986"
---
# <a name="structs-c-programming-guide"></a>Structures (Guide de programmation C#)
Les structs sont définis à l’aide du mot clé [struct](../../../csharp/language-reference/keywords/struct.md), par exemple :  
  
 [!code-csharp[csProgGuideObjects#39](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/structs_1.cs)]  
  
 Les structs partagent presque tous la même syntaxe que les classes, bien qu'ils soient plus limités que ces dernières :  
  
-   Au sein d’une déclaration de struct, les champs ne peuvent pas être initialisés à moins d’être déclarés comme étant de type const ou static.  
  
-   Un struct ne peut pas déclarer de constructeur par défaut (un constructeur sans paramètre) ni de finaliseur.  
  
-   Les structs sont copiés lors de l'assignation. Lorsqu'un struct est assigné à une nouvelle variable, toutes les données sont copiées et les modifications apportées à la nouvelle copie ne changent pas les données de la copie d'origine. Il est important de s’en souvenir lors de l’utilisation de collections de types valeur comme Dictionary\<string, myStruct>.  
  
-   Les structs sont des types valeur et les classes des types référence.  
  
-   Contrairement aux classes, il est possible d’instancier les structs sans avoir recours à un opérateur `new`.  
  
-   Les structs peuvent déclarer des constructeurs qui ont des paramètres.  
  
-   Un struct ne peut pas hériter d'un autre struct ou d'une classe ; il ne peut pas non plus servir de base à une classe. Tous les structs héritent directement de `System.ValueType`, qui hérite de `System.Object`.  
  
-   Un struct peut implémenter des interfaces.  
  
-   Un struct peut être utilisé comme un type Nullable et peut avoir une valeur null.  
  
## <a name="related-sections"></a>Rubriques connexes  
 Pour plus d'informations :  
  
-   [Utilisation de structs](../../../csharp/programming-guide/classes-and-structs/using-structs.md)  
  
-   [Constructeurs](../../../csharp/programming-guide/classes-and-structs/constructors.md)  
  
-   [Types Nullable](../../../csharp/programming-guide/nullable-types/index.md)  
  
-   [Comment : différencier le passage d’un struct et le passage d’une référence de classe à une méthode](../../../csharp/programming-guide/classes-and-structs/how-to-know-the-difference-passing-a-struct-and-passing-a-class-to-a-method.md)  
  
-   [Guide pratique pour implémenter des conversions définies par l’utilisateur entre des structs](../../../csharp/programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)  
  
## <a name="see-also"></a>Voir aussi  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Classes et structs](../../../csharp/programming-guide/classes-and-structs/index.md)  
 [Classes](../../../csharp/programming-guide/classes-and-structs/classes.md)
