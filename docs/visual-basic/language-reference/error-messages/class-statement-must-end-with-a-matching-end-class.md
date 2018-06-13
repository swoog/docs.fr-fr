---
title: '&#39;Classe&#39; instruction doit se terminer par une mise en correspondance &#39;End Class&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30481
- bc30481
helpviewer_keywords:
- BC30481
ms.assetid: 583f3029-bc3a-4e06-866f-92dbecc46f19
ms.openlocfilehash: 7c9051b15f6d9cf37d7d0245f758905467d5bbc5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33585513"
---
# <a name="39class39-statement-must-end-with-a-matching-39end-class39"></a>&#39;Classe&#39; instruction doit se terminer par une mise en correspondance &#39;End Class&#39;
`Class` permet de lancer un `Class` bloquer ; par conséquent, elle ne peut apparaître au début du bloc, avec une mise en correspondance `End Class` instruction termine le bloc. Soit vous avez un redondant `Class` instruction, ou vous n’avez pas terminé votre `Class` bloc avec `End Class`.  
  
 **ID d’erreur :** BC30481  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Recherchez et supprimez l’inutiles `Class` instruction.  
  
-   Conclure le `Class` bloc avec une mise en correspondance `End Class`.  
  
## <a name="see-also"></a>Voir aussi  
 [Fin \<mot clé > instruction](../../../visual-basic/language-reference/statements/end-keyword-statement.md)  
 [Class (instruction)](../../../visual-basic/language-reference/statements/class-statement.md)
