---
title: Classes (Guide de programmation C#)
description: En savoir plus sur les types de classe et découvrir comment les créer
ms.date: 04/05/2018
helpviewer_keywords:
- classes [C#]
- C# language, classes
ms.assetid: e8848524-7273-429f-8aba-c658d5eff5ad
ms.openlocfilehash: 688736aa8556719789b02d7db25858f442b4309e
ms.sourcegitcommit: 895c7602386a6dfe7ca4facce3d965b27e5c6e87
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2018
ms.locfileid: "34312090"
---
# <a name="classes-c-programming-guide"></a>Classes (Guide de programmation C#)
Une *classe* est une construction qui vous permet de créer vos propres types personnalisés en regroupant des variables d’autres types, méthodes et événements. Une classe s’apparente à un plan. Elle définit les données et le comportement d’un type. Si la classe n’est pas déclarée comme statique, le code client peut créer des *instances* de cette classe. Ces instances sont des *objets* qui sont assignés à une variable. L’instance d’une classe reste en mémoire jusqu’à ce que toutes les références à celle-ci soient hors de portée. À ce stade, le CLR la marque comme admissible pour le garbage collection. Si la classe est déclarée comme [static](../../../csharp/language-reference/keywords/static.md), vous ne pouvez pas créer d’instances, et le code client peut y accéder uniquement par le biais de la classe elle-même. Pour plus d’informations, consultez [Classes statiques et membres de classe statique](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).  

## <a name="reference-types"></a>Types référence  
Un type défini comme [class](../../../csharp/language-reference/keywords/class.md) est un *type référence*. Au moment de l’exécution, quand vous déclarez une variable de type référence, celle-ci contient la valeur [Null](../../../csharp/language-reference/keywords/null.md) tant que vous n’avez pas explicitement créé une instance de la classe à l’aide de l’opérateur [new](../../../csharp/language-reference/keywords/new.md) ou que vous ne lui avez pas assigné un objet créé ailleurs, comme indiqué dans l’exemple suivant :

```csharp
MyClass mc = new MyClass();
MyClass mc2 = mc;
```

Quand l’objet est créé, la mémoire est allouée sur le tas managé et la variable contient uniquement une référence à l’emplacement de l’objet. Les types sur le tas managé entraînent une surcharge quand ils sont alloués et récupérés par la fonctionnalité de gestion automatique de la mémoire du CLR (appelée *garbage collection*). Toutefois, le garbage collection est également optimisé, et dans la plupart des cas, ne nuit pas aux performances. Pour plus d’informations sur le garbage collection, consultez [Gestion automatique de la mémoire et garbage collection](../../../standard/garbage-collection/gc.md).  
  
## <a name="declaring-classes"></a>Déclaration de classes  
 Les classes sont déclarées à l’aide du mot clé [class](../../../csharp/language-reference/keywords/class.md), comme l’illustre l’exemple suivant :

 ```csharp
 public class Customer
 {
    // Fields, properties, methods and events go here...
 }
```

 Le mot clé `class` est précédé du niveau d’accès. Comme [public](../../../csharp/language-reference/keywords/public.md) est utilisé dans ce cas, n’importe qui peut créer des instances de cette classe. Le nom de la classe suit le mot clé `class`. Le reste de la définition est le corps de la classe, où le comportement et les données sont définis. Les champs, propriétés, méthodes et événements d’une classe sont désignés collectivement par le terme « *membres de classe* ».  
  
## <a name="creating-objects"></a>Création d'objets  
 Bien qu’ils soient parfois employés indifféremment, une classe et un objet sont deux choses différentes. Une classe définit un type d’objet, mais il ne s’agit pas d’un objet en soi. Un objet, qui est une entité concrète basée sur une classe, est parfois désigné par le terme « instance de classe ».  
  
 Vous pouvez créer des objets en utilisant le mot clé [new](../../../csharp/language-reference/keywords/new.md) suivi du nom de la classe sur laquelle l’objet est basé, comme suit :  

 ```csharp
 Customer object1 = new Customer();
 ```
  
 Quand une instance d’une classe est créée, une référence à l’objet est repassée au programmeur. Dans l’exemple précédent, `object1` est une référence à un objet basé sur `Customer`. Cette référence fait référence au nouvel objet, mais elle ne contient pas ses données. En fait, vous pouvez créer une référence d’objet sans créer d’objet :  
  
  ```csharp
  Customer object2;
  ```
  
 Nous vous déconseillons de créer des références d’objet comme celle-ci, sans référence à un objet, car toute tentative d’accès à un objet à l’aide d’une telle référence échoue au moment de l’exécution. Vous pouvez toutefois créer une telle référence pour faire référence à un objet : soit en créant un objet, soit en l’assignant à un objet existant, comme suit :  

 ```csharp
 Customer object3 = new Customer();
 Customer object4 = object3;
 ```
  
 Ce code crée deux références d’objet qui font toutes deux référence au même objet. Toute modification apportée à l’objet par le biais de `object3` est donc reflétée dans les utilisations suivantes de `object4`. Les objets qui sont basés sur des classes étant désignés par référence, les classes sont appelées des « types référence ».  
  
## <a name="class-inheritance"></a>Héritage de classe  

 Les classes prennent entièrement en charge l’*héritage*, caractéristique fondamentale de la programmation orientée objet. Quand vous créez une classe, vous pouvez hériter de toute autre interface ou classe qui n’est pas définie comme [sealed](../../../csharp/language-reference/keywords/sealed.md), et d’autres classes peuvent hériter de votre classe et substituer des méthodes virtuelles de la classe.

 L’héritage se fait par le biais d’une *dérivation*, ce qui signifie qu’une classe est déclarée à l’aide d’une *classe de base* dont elle hérite les données et le comportement. Pour spécifier une classe de base, ajoutez deux-points et le nom de la classe de base après le nom de la classe dérivée, comme suit :  

 ```csharp
 public class Manager : Employee
 {
     // Employee fields, properties, methods and events are inherited
     // New Manager fields, properties, methods and events go here...
 }
 ```
  
 Quand une classe déclare une classe de base, elle hérite de tous les membres de la classe de base à l’exception des constructeurs. Pour plus d’informations, consultez [Héritage](../../../csharp/programming-guide/classes-and-structs/inheritance.md).
  
 Contrairement à C++, une classe en C# ne peut hériter directement que d’une classe de base. Toutefois, une classe de base pouvant elle-même hériter d’une autre classe, une classe peut hériter indirectement de plusieurs classes de base. En outre, une classe peut implémenter directement plusieurs interfaces. Pour plus d’informations, consultez [Interfaces](../../../csharp/programming-guide/interfaces/index.md).  
  
 Une classe peut être déclarée [abstract](../../../csharp/language-reference/keywords/abstract.md). Une classe abstraite contient des méthodes abstraites qui ont une définition de signature, mais aucune implémentation. Les classes abstraites ne peuvent pas être instanciées. Elles peuvent être utilisées uniquement à travers des classes dérivées qui implémentent les méthodes abstraites. En revanche, une classe [sealed](../../../csharp/language-reference/keywords/sealed.md) ne permet pas à d’autres classes de dériver d’elle. Pour plus d’informations, consultez la page [Classes abstraites et scellées et membres de classe](../../../csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members.md).  
  
 Les définitions de classe peuvent être fractionnées entre différents fichiers sources. Pour plus d’informations, consultez [Classes et méthodes partielles](../../../csharp/programming-guide/classes-and-structs/partial-classes-and-methods.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit une classe publique qui contient une [propriété implémentée automatiquement](auto-implemented-properties.md), une méthode et une méthode spéciale appelée un constructeur. Pour plus d’informations, consultez les rubriques [Propriétés](properties.md), [Méthodes](methods.md) et [Constructeurs](constructors.md). Les instances de la classe sont ensuite instanciées à l’aide du mot clé `new`.  
  
 [!code-csharp[Class Example](~/samples/snippets/csharp/programming-guide/classes-and-structs/class-example.cs)] 
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Programmation orientée objet](../concepts/object-oriented-programming.md)  
 [Polymorphisme](../../../csharp/programming-guide/classes-and-structs/polymorphism.md)  
 [Membres](../../../csharp/programming-guide/classes-and-structs/members.md)  
 [Méthodes](../../../csharp/programming-guide/classes-and-structs/methods.md)  
 [Constructeurs](../../../csharp/programming-guide/classes-and-structs/constructors.md)  
 [Finaliseurs](../../../csharp/programming-guide/classes-and-structs/destructors.md)  
 [Objects](../../../csharp/programming-guide/classes-and-structs/objects.md)
