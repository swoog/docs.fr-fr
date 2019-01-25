---
title: '&#39;#ElseIf&#39; doit être précédé d’une mise en correspondance &#39;#If&#39; ou &#39;#ElseIf&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30014
- bc30014
helpviewer_keywords:
- BC30014
ms.assetid: 5215585e-2efa-485a-9efe-9833a1cc83a0
ms.openlocfilehash: 1e63595ee573e9356f6870a02b2131897c725baf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505781"
---
# <a name="39elseif39-must-be-preceded-by-a-matching-39if39-or-39elseif39"></a>&#39;#ElseIf&#39; doit être précédé d’une mise en correspondance &#39;#If&#39; ou &#39;#ElseIf&#39;
`#ElseIf` est une directive de compilation conditionnelle. Un `#ElseIf` clause doit être précédée d’une mise en correspondance `#If` ou `#ElseIf` clause.  
  
 **ID d’erreur :** BC30014  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Vérifiez que précédente `#If` ou `#ElseIf` n’a pas été séparés à partir de ce `#ElseIf` par un bloc de compilation conditionnelle intermédiaire ou mal placé `#End If`.  
  
2.  Si le `#ElseIf` est précédé par un `#Else` directive, supprimez le `#Else` ou remplacez-le par un `#ElseIf`.  
  
3.  Si tout le reste est en ordre, ajoutez une directive `#If` au début du bloc de compilation conditionnelle.  
  
## <a name="see-also"></a>Voir aussi
- [#If...Then...#Else, directives](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
