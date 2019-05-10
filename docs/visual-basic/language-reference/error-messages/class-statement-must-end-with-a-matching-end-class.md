---
title: Une instruction 'Class' doit se terminer par une 'End Class' correspondante
ms.date: 07/20/2015
f1_keywords:
- vbc30481
- bc30481
helpviewer_keywords:
- BC30481
ms.assetid: 583f3029-bc3a-4e06-866f-92dbecc46f19
ms.openlocfilehash: 559595e9902ec2f0a19fd6b13e2c89fa1c2b52d7
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64602414"
---
# <a name="class-statement-must-end-with-a-matching-end-class"></a>Une instruction 'Class' doit se terminer par une 'End Class' correspondante
`Class` permet de lancer un `Class` bloquer ; il ne peut donc apparaître au début du bloc, avec une mise en correspondance `End Class` instruction fin du bloc. Soit vous avez un redondant `Class` instruction, ou vous n’avez pas terminé votre `Class` bloc avec `End Class`.  
  
 **ID d’erreur :** BC30481  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Recherchez et supprimez l’instruction `Class` inutile.  
  
- Conclure le `Class` bloc avec une mise en correspondance `End Class`.  
  
## <a name="see-also"></a>Voir aussi

- [Fin \<mot clé > instruction](../../../visual-basic/language-reference/statements/end-keyword-statement.md)
- [Class (instruction)](../../../visual-basic/language-reference/statements/class-statement.md)
