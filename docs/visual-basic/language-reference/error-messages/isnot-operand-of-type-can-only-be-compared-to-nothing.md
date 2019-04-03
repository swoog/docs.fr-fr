---
title: L’opérande 'IsNot' du type 'NomType' ne peut être comparé qu’à 'Nothing', car 'NomType' est un type nullable
ms.date: 07/20/2015
f1_keywords:
- bc32128
- vbc32128
helpviewer_keywords:
- BC32128
ms.assetid: 1155b23a-ad75-4bab-b9da-73f35c767a36
ms.openlocfilehash: be2a3239b2ca520c4051a1504f91a766b4401a05
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58834021"
---
# <a name="isnot-operand-of-type-typename-can-only-be-compared-to-nothing-because-typename-is-a-nullable-type"></a>L’opérande 'IsNot' du type 'NomType' ne peut être comparé qu’à 'Nothing', car 'NomType' est un type nullable
Une variable déclarée comme nullable a été comparée à une expression autre que `Nothing` à l’aide de la `IsNot` opérateur.  
  
 **ID d’erreur :** BC32128  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Pour comparer un type nullable à une expression autre que `Nothing` à l’aide de l’opérateur `IsNot` , appelez la méthode `GetType` sur le type nullable et comparez le résultat à l’expression, comme illustré dans l’exemple suivant.  
  
```vb  
Dim number? As Integer = 5  
  
If number IsNot Nothing Then  
  If number.GetType() IsNot Type.GetType("System.Int32") Then   
  
  End If  
End If  
```  
  
## <a name="see-also"></a>Voir aussi

- [Types valeur Nullable](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [IsNot (opérateur)](../../../visual-basic/language-reference/operators/isnot-operator.md)
