---
title: Impossible de convertir le type anonyme en arborescence de l'expression, car elle contient un champ qui sert à initialiser un autre champ
ms.date: 07/20/2015
f1_keywords:
- bc36548
- vbc36548
helpviewer_keywords:
- BC36548
ms.assetid: 27de068f-080e-4160-86bf-1ec23fd1925a
ms.openlocfilehash: 045061f403b301d460bc85d161c1d6dee9c7d9f1
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64602400"
---
# <a name="cannot-convert-anonymous-type-to-expression-tree-because-it-contains-a-field-that-is-used-in-the-initialization-of-another-field"></a>Impossible de convertir le type anonyme en arborescence de l'expression, car elle contient un champ qui sert à initialiser un autre champ
Le compilateur n’accepte pas de conversion d’un anonyme en une arborescence d’expression lorsqu’une propriété du type anonyme est utilisée pour initialiser une autre propriété du type anonyme. Par exemple, dans le code suivant, `Prop1` est déclarée dans la liste d’initialisation et ensuite utilisée comme valeur initiale pour `Prop2`.  
  
```vb  
Module M2  
  
    Sub ExpressionExample(Of T)(ByVal x As Expressions.Expression(Of Func(Of T)))  
    End Sub  
  
    Sub Main()  
        ' The following line causes the error.  
        ' ExpressionExample(Function() New With {.Prop1 = 2, .Prop2 = .Prop1})  
  
    End Sub  
End Module  
```  
  
 **ID d’erreur :** BC36548  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Affectez la valeur initiale pour `Prop1` à une variable locale. Assignez cette variable à la fois aux `Prop1` et `Prop2`, comme illustré dans le code suivant.  
  
    ```  
    Sub Main()  
  
        Dim temp = 2  
        ExpressionExample(Function() New With {.Prop1 = temp, .Prop2 = temp})  
  
    End Sub  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Types anonymes (Visual Basic)](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)
- [Arborescences d’expressions (Visual Basic)](../../programming-guide/concepts/expression-trees/index.md)
- [Guide pratique pour Utiliser des arborescences d’Expression pour générer des requêtes dynamiques (Visual Basic)](../../programming-guide/concepts/expression-trees/how-to-use-expression-trees-to-build-dynamic-queries.md)
