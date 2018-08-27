---
title: sealed (référence C#)
ms.date: 07/20/2015
f1_keywords:
- sealed
- sealed_CSharpKeyword
helpviewer_keywords:
- sealed keyword [C#]
ms.assetid: 8e4ed5d3-10be-47db-9488-0da2008e6f3f
ms.openlocfilehash: be13e04dce12dfb60a1179e05a0a47eca1df1af4
ms.sourcegitcommit: a1e35d4e94edab384a63406c0a5438306873031b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2018
ms.locfileid: "42752041"
---
# <a name="sealed-c-reference"></a>sealed (référence C#)
Lorsqu’il est appliqué à une classe, le modificateur `sealed` empêche les autres classes d’en hériter. Dans l’exemple suivant, la classe `B` hérite de la classe `A`, mais aucune classe ne peut hériter de la classe `B`.  
  
```csharp  
class A {}      
sealed class B : A {}  
```  
  
 Vous pouvez également utiliser le modificateur `sealed` sur une méthode ou une propriété qui substitue une méthode ou une propriété virtuelle dans une classe de base. Ainsi, vous pouvez autoriser les classes à dériver de votre classe et les empêcher de substituer des méthodes ou des propriétés virtuelles spécifiques.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, `Z` hérite de `Y` mais `Z` ne peut pas substituer la fonction virtuelle `F` qui est déclarée dans `X` et scellée (sealed) dans `Y`.  
  
 [!code-csharp[csrefKeywordsModifiers#16](../../../csharp/language-reference/keywords/codesnippet/CSharp/sealed_1.cs)]  
  
 Lorsque vous définissez de nouvelles méthodes ou propriétés dans une classe, vous pouvez empêcher les classes dérivées de les substituer en ne les déclarant pas comme [virtuelles](../../../csharp/language-reference/keywords/virtual.md).  
  
 Une erreur consiste à utiliser le modificateur [abstract](../../../csharp/language-reference/keywords/abstract.md) avec une classe sealed, car une classe abstraite doit être héritée par une classe qui fournit une implémentation des méthodes ou des propriétés abstraites.  
  
 Lorsqu’il est appliqué à une méthode ou une propriété, le modificateur `sealed` doit toujours être utilisé avec [override](../../../csharp/language-reference/keywords/override.md).  
  
 Comme les structs sont implicitement sealed, ils ne peuvent pas être hérités.  
  
 Pour plus d’informations, consultez [Héritage](../../../csharp/programming-guide/classes-and-structs/inheritance.md).  
  
 Pour plus d’exemples, consultez [Classes abstract et sealed et membres de classe](../../../csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csrefKeywordsModifiers#17](../../../csharp/language-reference/keywords/codesnippet/CSharp/sealed_2.cs)]  
  
 Dans l’exemple précédent, vous pouvez essayer d’hériter de la classe sealed à l’aide de l’instruction suivante :  
  
 `class MyDerivedC: SealedClass {}   // Error`  
  
 Le résultat est un message d’erreur :  
  
 `'MyDerivedC': cannot derive from sealed type 'SealedClass'`  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="remarks"></a>Notes  
 Pour déterminer s’il faut sceller une classe, une méthode ou une propriété, vous devez généralement prendre en compte les deux points suivants :  
  
-   Les avantages potentiels dont les classes dérivées peuvent bénéficier grâce à la possibilité de personnaliser votre classe.  
  
-   Le risque que les classes dérivées puissent modifier vos classes de telle manière qu’elles ne fonctionnent plus correctement ou comme prévu.  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
 [Classes statiques et membres de classe statique](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md)  
 [Classes abstract et sealed et membres de classe](../../../csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members.md)  
 [Modificateurs d’accès](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)  
 [Modificateurs](../../../csharp/language-reference/keywords/modifiers.md)  
 [override](../../../csharp/language-reference/keywords/override.md)  
 [virtual](../../../csharp/language-reference/keywords/virtual.md)
