---
title: 'Procédure : Reportez-vous à l’Instance actuelle d’un objet (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], object
- objects [Visual Basic], referring to current instance
- instances [Visual Basic], referring to current
- current instance
- object variables [Visual Basic]
ms.assetid: 7f9b2c77-03cd-428f-adc2-b18070226e7c
ms.openlocfilehash: 3c44748798d5ed554fc9fbded9c3a4d981a66d2f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58823361"
---
# <a name="how-to-refer-to-the-current-instance-of-an-object-visual-basic"></a>Procédure : Reportez-vous à l’Instance actuelle d’un objet (Visual Basic)
Le *instance actuelle* d’un objet est l’instance dans laquelle le code est en cours d’exécution.  
  
 Vous utilisez le `Me` mot clé pour faire référence à l’instance actuelle.  
  
### <a name="to-refer-to-the-current-instance"></a>Pour faire référence à l’instance actuelle  
  
-   Utiliser le `Me` mot clé où vous utiliseriez normalement le nom d’une variable objet.  
  
    ```  
    Me.ForeColor = System.Drawing.Color.Crimson  
    Me.Close()  
    ```  
  
     Bien que `Me` se comporte comme un objet variable, vous ne pouvez pas déclarez-le ou quoi que ce soit à lui affecter. `Me` fait toujours référence à l’instance actuelle.  
  
## <a name="see-also"></a>Voir aussi

- [Variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [Assignation des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [Me, My, MyBase et MyClass](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
