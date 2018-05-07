---
title: Classe déléguée &#39; &lt;classname&gt; &#39; n’a aucun méthode Invoke, afin de l’expression de ce type ne peut pas être la cible d’un appel de méthode
ms.date: 07/20/2015
f1_keywords:
- vbc30220
- bc30220
helpviewer_keywords:
- BC30220
ms.assetid: 6be0d61c-f2f9-4f9b-ab90-8871a0d7206d
ms.openlocfilehash: cc1abba46224772e733780800dd104dfc7ebe9ad
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="delegate-class-39ltclassnamegt39-has-no-invoke-method-so-an-expression-of-this-type-cannot-be-the-target-of-a-method-call"></a>Classe déléguée &#39; &lt;classname&gt; &#39; n’a aucun méthode Invoke, afin de l’expression de ce type ne peut pas être la cible d’un appel de méthode
Un appel à `Invoke` via un délégué a échoué, car `Invoke` n’est pas implémentée sur la classe déléguée.  
  
 **ID d’erreur :** BC30220  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Assurez-vous qu’une instance de la classe déléguée a été créée avec un `Dim` instruction et qu’une procédure a été assignée à l’instance de délégué avec le `AddressOf` opérateur.  
  
2.  Recherchez le code qui implémente la classe déléguée et vérifiez qu’il implémente la `Invoke` procédure.  
  
## <a name="see-also"></a>Voir aussi  
 [Délégués](../../../visual-basic/programming-guide/language-features/delegates/index.md)  
 [Delegate (instruction)](../../../visual-basic/language-reference/statements/delegate-statement.md)  
 [AddressOf (opérateur)](../../../visual-basic/language-reference/operators/addressof-operator.md)  
 [Dim (instruction)](../../../visual-basic/language-reference/statements/dim-statement.md)
