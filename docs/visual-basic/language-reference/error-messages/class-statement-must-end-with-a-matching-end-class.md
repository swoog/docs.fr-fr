---
title: '&#39;Classe&#39; instruction doit se terminer par une mise en correspondance &#39;End Class&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30481
- bc30481
helpviewer_keywords:
- BC30481
ms.assetid: 583f3029-bc3a-4e06-866f-92dbecc46f19
ms.openlocfilehash: 4e80ce58048bfa7f2fecc65e7167479df07bf57c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715086"
---
# <a name="39class39-statement-must-end-with-a-matching-39end-class39"></a>&#39;Classe&#39; instruction doit se terminer par une mise en correspondance &#39;End Class&#39;
`Class` permet de lancer un `Class` bloquer ; il ne peut donc apparaître au début du bloc, avec une mise en correspondance `End Class` instruction fin du bloc. Soit vous avez un redondant `Class` instruction, ou vous n’avez pas terminé votre `Class` bloc avec `End Class`.  
  
 **ID d’erreur :** BC30481  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Recherchez et supprimez l’instruction `Class` inutile.  
  
-   Conclure le `Class` bloc avec une mise en correspondance `End Class`.  
  
## <a name="see-also"></a>Voir aussi
- [Fin \<mot clé > instruction](../../../visual-basic/language-reference/statements/end-keyword-statement.md)
- [Class (instruction)](../../../visual-basic/language-reference/statements/class-statement.md)
