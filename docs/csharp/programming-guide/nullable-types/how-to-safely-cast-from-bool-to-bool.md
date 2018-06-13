---
title: 'Comment : effectuer sans risque un cast du type bool? en bool (Guide de programmation C#)'
ms.date: 07/20/2015
helpviewer_keywords:
- casting [C#], nullable types
- nullable types [C#], casting bool? to bool
ms.assetid: e06e4274-a443-422d-8ef1-9dbf9df55237
ms.openlocfilehash: e04e34abd477730f9dd01486ec6bddcde4943edc
ms.sourcegitcommit: 43924acbdbb3981d103e11049bbe460457d42073
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
ms.locfileid: "34457481"
---
# <a name="how-to-safely-cast-from-bool-to-bool-c-programming-guide"></a>Comment : effectuer sans risque un cast du type bool? en bool (Guide de programmation C#)
Le type Nullable `bool?` peut contenir trois valeurs différentes : `true`, `false` et `null`. Par conséquent, le type `bool?` ne peut pas être utilisé dans des instructions conditionnelles comme `if`, `for` ou `while`. Par exemple, le code suivant génère une erreur du compilateur.  
  
```csharp  
bool? b = null;  
if (b) // Error CS0266.  
{  
}  
```  
  
 Cela n’est pas autorisé, car il est difficile de savoir ce que `null` signifie dans le contexte d’une instruction conditionnelle. Pour utiliser un `bool?` dans une instruction conditionnelle, examinez d’abord sa propriété <xref:System.Nullable%601.HasValue%2A> pour vérifier que sa valeur n’est pas `null`, puis castez-le en `bool`. Pour plus d'informations, consultez [bool](../../../csharp/language-reference/keywords/bool.md). Si vous effectuez le cast sur un `bool?` avec la valeur `null`, une exception <xref:System.InvalidOperationException> est levée dans le test conditionnel. L’exemple suivant illustre une façon d’effectuer sans risque un cast de `bool?` en `bool` :  
  
## <a name="example"></a>Exemple  
  
```csharp  
bool? test = null;  
// Other code that may or may not  
// give a value to test.  
if(!test.HasValue) //check for a value  
{  
    // Assume that IsInitialized  
    // returns either true or false.  
    test = IsInitialized();  
}  
if((bool)test) //now this cast is safe  
{  
   // Do something.  
}  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Mots clés littéraux](../../../csharp/language-reference/keywords/literal-keywords.md)  
 [Types Nullable](../../../csharp/programming-guide/nullable-types/index.md)  
 [?? Opérateur](../../../csharp/language-reference/operators/null-coalescing-operator.md)
