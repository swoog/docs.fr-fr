---
title: "Comment : référencer l'instance actuelle d'un objet (Visual Basic)"
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], object
- objects [Visual Basic], referring to current instance
- instances [Visual Basic], referring to current
- current instance
- object variables [Visual Basic]
ms.assetid: 7f9b2c77-03cd-428f-adc2-b18070226e7c
ms.openlocfilehash: c1b79f1b6a9768941d6fe966c5b5886ea742f808
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-refer-to-the-current-instance-of-an-object-visual-basic"></a>Comment : référencer l'instance actuelle d'un objet (Visual Basic)
Le *instance actuelle* d’un objet est l’instance dans laquelle le code est en cours d’exécution.  
  
 Vous utilisez la `Me` (mot clé) pour faire référence à l’instance actuelle.  
  
### <a name="to-refer-to-the-current-instance"></a>Pour faire référence à l’instance actuelle  
  
-   Utilisez le `Me` mot clé où vous utiliseriez normalement le nom d’une variable objet.  
  
    ```  
    Me.ForeColor = System.Drawing.Color.Crimson  
    Me.Close()  
    ```  
  
     Bien que `Me` se comporte comme un objet variable, vous ne peut pas déclarer ou affectez-lui quoi que ce soit. `Me` fait toujours référence à l’instance actuelle.  
  
## <a name="see-also"></a>Voir aussi  
 [Variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)  
 [Assignation des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)  
 [Me, My, MyBase et MyClass](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
