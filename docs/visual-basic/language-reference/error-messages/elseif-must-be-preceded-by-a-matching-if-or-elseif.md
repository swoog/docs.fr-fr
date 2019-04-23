---
title: "'#ElseIf' doit être précédé d'un '#If' ou '#ElseIf' correspondant"
ms.date: 07/20/2015
f1_keywords:
- vbc30014
- bc30014
helpviewer_keywords:
- BC30014
ms.assetid: 5215585e-2efa-485a-9efe-9833a1cc83a0
ms.openlocfilehash: 4832fb80cfbe42c7a1303e0de69f36784711c05a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59311056"
---
# <a name="elseif-must-be-preceded-by-a-matching-if-or-elseif"></a>'#ElseIf' doit être précédé d'un '#If' ou '#ElseIf' correspondant
`#ElseIf` est une directive de compilation conditionnelle. Un `#ElseIf` clause doit être précédée d’une mise en correspondance `#If` ou `#ElseIf` clause.  
  
 **ID d’erreur :** BC30014  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Vérifiez que précédente `#If` ou `#ElseIf` n’a pas été séparés à partir de ce `#ElseIf` par un bloc de compilation conditionnelle intermédiaire ou mal placé `#End If`.  
  
2. Si le `#ElseIf` est précédé par un `#Else` directive, supprimez le `#Else` ou remplacez-le par un `#ElseIf`.  
  
3. Si tout le reste est en ordre, ajoutez une directive `#If` au début du bloc de compilation conditionnelle.  
  
## <a name="see-also"></a>Voir aussi

- [#If...Then...#Else, directives](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
