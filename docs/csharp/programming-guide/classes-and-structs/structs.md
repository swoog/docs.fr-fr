---
title: Structures (Guide de programmation C#)
ms.date: 08/21/2018
helpviewer_keywords:
- C# language, structs
- structs [C#]
ms.assetid: b7cf4ff2-0eb7-4e5c-93d5-b2196b4f5d89
ms.openlocfilehash: 27d4b0d7edf1b5e89e84ac1df5783d68ebb4efe0
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44259483"
---
# <a name="structs-c-programming-guide"></a>Structures (Guide de programmation C#)

Les structs sont définis à l’aide du mot clé [struct](../../language-reference/keywords/struct.md), par exemple :  
  
[!code-csharp[csProgGuideObjects#39](./codesnippet/CSharp/structs_1.cs)]  
  
Les structs partagent quasiment la même syntaxe que les classes. Le nom du struct doit être un [nom d’identificateur](../inside-a-program/identifier-names.md) C# valide. Les structs sont plus limités que les classes des manières suivantes :  
  
- Au sein d’une déclaration de struct, les champs ne peuvent pas être initialisés à moins d’être déclarés comme étant de type const ou static.  
- Un struct ne peut pas déclarer de constructeur par défaut (un constructeur sans paramètre) ni de finaliseur.  
- Les structs sont copiés lors de l'assignation. Lorsqu'un struct est assigné à une nouvelle variable, toutes les données sont copiées et les modifications apportées à la nouvelle copie ne changent pas les données de la copie d'origine. Il est important de vous en souvenir quand vous utilisez des collections de types valeur telles que `Dictionary<string, myStruct>`.  
- Les structs sont des types valeur, contrairement aux classes, qui sont des types référence.  
- Contrairement aux classes, il est possible d’instancier les structs sans avoir recours à un opérateur `new`.  
- Les structs peuvent déclarer des constructeurs qui ont des paramètres. 
- Un struct ne peut pas hériter d'un autre struct ou d'une classe ; il ne peut pas non plus servir de base à une classe. Tous les structs héritent directement de <xref:System.ValueType>, qui hérite de <xref:System.Object>.  
- Un struct peut implémenter des interfaces.  
- Un struct peut être utilisé comme un type Nullable et peut avoir une valeur null.  
  
## <a name="related-sections"></a>Rubriques connexes  

Pour plus d'informations :  
  
- [Utilisation de structs](using-structs.md)
- [Constructeurs](constructors.md)
- [Types Nullable](../nullable-types/index.md)
- [Comment : différencier le passage d’un struct et le passage d’une référence de classe à une méthode](how-to-know-the-difference-passing-a-struct-and-passing-a-class-to-a-method.md)
- [Guide pratique pour implémenter des conversions définies par l’utilisateur entre des structs](../statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)

## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../index.md)
- [Classes et structs](index.md)
- [Classes](classes.md)
- [Noms d’identificateur](../inside-a-program/identifier-names.md)
