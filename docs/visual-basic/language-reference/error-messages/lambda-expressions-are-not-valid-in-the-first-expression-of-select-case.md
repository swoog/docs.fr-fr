---
title: Expressions lambda ne sont pas valides dans la première expression d’une &#39;Select Case&#39; instruction
ms.date: 07/20/2015
f1_keywords:
- bc36635
- vbc36635
helpviewer_keywords:
- BC36635
ms.assetid: 74609979-9c03-4864-bbce-f588aa2e0917
ms.openlocfilehash: afefa821f9695dbbfe2a96aee5afd3171ae5b1db
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54700219"
---
# <a name="lambda-expressions-are-not-valid-in-the-first-expression-of-a-39select-case39-statement"></a>Expressions lambda ne sont pas valides dans la première expression d’une &#39;Select Case&#39; instruction
Vous ne pouvez pas utiliser une expression lambda pour l’expression de test dans un `Select Case` instruction. Définitions d’expression lambda retournent des fonctions et l’expression de test d’un `Select Case` instruction doit être un type de données élémentaire.  
  
 Le code suivant génère cette erreur :  
  
```vb  
' Select Case (Function(arg) arg Is Nothing)  
    ' List of the cases.  
' End Select  
```  
  
 **ID d’erreur :** BC36635  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Examinez votre code pour déterminer si une construction conditionnelle différente, comme une instruction `If...Then...Else` , répond à vos besoins.  
  
-   Vous aviez prévu appeler la fonction, comme indiqué dans le code suivant :  
  
```vb  
Dim num? As Integer  
Select Case ((Function(arg? As Integer) arg Is Nothing)(num))  
    ' List of the cases  
End Select  
```  
  
## <a name="see-also"></a>Voir aussi
- [Expressions lambda](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [If...Then...Else (instruction)](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [Select...Case (instruction)](../../../visual-basic/language-reference/statements/select-case-statement.md)
