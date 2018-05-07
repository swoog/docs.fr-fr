---
title: '&#39;IsNot&#39; opérande de type &#39;typename&#39; ne peut être comparé qu’à &#39;rien&#39;, car &#39;typename&#39; est un type nullable'
ms.date: 07/20/2015
f1_keywords:
- bc32128
- vbc32128
helpviewer_keywords:
- BC32128
ms.assetid: 1155b23a-ad75-4bab-b9da-73f35c767a36
ms.openlocfilehash: 44cc17c73b476e5e322b9b58b021bc7bcd63167f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="39isnot39-operand-of-type-39typename39-can-only-be-compared-to-39nothing39-because-39typename39-is-a-nullable-type"></a>&#39;IsNot&#39; opérande de type &#39;typename&#39; ne peut être comparé qu’à &#39;rien&#39;, car &#39;typename&#39; est un type nullable
Une variable déclarée comme nullable a été comparée à une expression autre que `Nothing` à l’aide de la `IsNot` opérateur.  
  
 **ID d’erreur :** BC32128  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Pour comparer un type nullable à une expression autre que `Nothing` à l’aide de la `IsNot` (opérateur), appelez le `GetType` méthode sur le type nullable et comparez le résultat à l’expression, comme illustré dans l’exemple suivant.  
  
```vb  
Dim number? As Integer = 5  
  
If number IsNot Nothing Then  
  If number.GetType() IsNot Type.GetType("System.Int32") Then   
  
  End If  
End If  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Types valeur Nullable](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)  
 [IsNot (opérateur)](../../../visual-basic/language-reference/operators/isnot-operator.md)
