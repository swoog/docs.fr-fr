---
title: '&#39;#ElseIf&#39; doit être précédé d’une mise en correspondance &#39;#If&#39; ou &#39;#ElseIf&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30014
- bc30014
helpviewer_keywords:
- BC30014
ms.assetid: 5215585e-2efa-485a-9efe-9833a1cc83a0
ms.openlocfilehash: ef904173b1791309f6c2722bd959cabdad1d71da
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33588146"
---
# <a name="39elseif39-must-be-preceded-by-a-matching-39if39-or-39elseif39"></a>&#39;#ElseIf&#39; doit être précédé d’une mise en correspondance &#39;#If&#39; ou &#39;#ElseIf&#39;
`#ElseIf` est une directive de compilation conditionnelle. Un `#ElseIf` clause doit être précédée d’une mise en correspondance `#If` ou `#ElseIf` clause.  
  
 **ID d’erreur :** BC30014  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Vérifiez que précédente `#If` ou `#ElseIf` n’a pas été séparé à partir de ce `#ElseIf` par un bloc de compilation conditionnelle intermédiaire ou mal placé `#End If`.  
  
2.  Si le `#ElseIf` est précédé par un `#Else` directive, supprimez le `#Else` ou modifiez-la pour un `#ElseIf`.  
  
3.  Si tout le reste est en ordre, ajoutez une directive `#If` au début du bloc de compilation conditionnelle.  
  
## <a name="see-also"></a>Voir aussi  
 [#If...Then...#Else, directives](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
