---
title: 'Procédure : Déplacer des données dans et hors d’une Variable (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], retrieving values
- variables [Visual Basic], storing data
ms.assetid: 93744f46-bf78-4fa0-9640-1de01bc38d9a
ms.openlocfilehash: 9b34173ebb3226fa00610c124c7b680e18d80de9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54717942"
---
# <a name="how-to-move-data-into-and-out-of-a-variable-visual-basic"></a>Procédure : Déplacer des données dans et hors d’une Variable (Visual Basic)
Vous stockez une valeur dans une variable en plaçant le nom de variable sur le côté gauche d’une instruction d’assignation.  
  
## <a name="putting-data-in-a-variable"></a>Placer des données dans une Variable  
  
#### <a name="to-store-a-value-in-a-variable"></a>Pour stocker une valeur dans une variable  
  
-   Utilisez le nom de variable sur le côté gauche d’une instruction d’assignation.  
  
     L’exemple suivant définit la valeur de la variable `alpha`.  
  
    ```  
    alpha = (beta * 6.27) / (gamma + 2.1)  
    ```  
  
     La valeur générée sur le côté droit de l’instruction d’assignation est stockée dans la variable.  
  
## <a name="getting-data-from-a-variable"></a>Obtention de données à partir d’une Variable  
 Vous récupérez une valeur variable en incluant le nom de variable dans une expression.  
  
#### <a name="to-retrieve-a-value-from-a-variable"></a>Pour récupérer une valeur dans une variable  
  
-   Utilisez le nom de variable dans une expression. Vous pouvez utiliser une variable de n’importe où vous pouvez utiliser une constante ou un littéral, sauf dans une expression qui définit la valeur d’une constante.  
  
     ou  
  
-   Utiliser le nom de variable suivant égaux (`=`) connectez-vous à une instruction d’assignation.  
  
     L’exemple suivant lit la valeur de la variable `startValue` , puis utilise la valeur de la variable `counter` dans une expression.  
  
    ```  
    counter = startValue  
    cellValue = (counter + 5) ^ 2  
    ```  
  
     La valeur de la variable participe à l’expression comme une constante serait, puis il est stocké dans la variable ou la propriété sur le côté gauche de l’instruction d’assignation.  
  
## <a name="see-also"></a>Voir aussi
- [Variables](../../../../visual-basic/programming-guide/language-features/variables/index.md)
- [Déclaration de variable](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [Variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
