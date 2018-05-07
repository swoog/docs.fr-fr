---
title: Les tailles de tableau ne peuvent pas figurer dans les spécificateurs de type
ms.date: 07/20/2015
f1_keywords:
- vbc30638
- bc30638
helpviewer_keywords:
- BC30638
ms.assetid: 93b654f4-70fa-4a48-baed-ffae42075550
ms.openlocfilehash: 45787db51de562f2266c587fd2bb15ef29ebefbe
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="array-bounds-cannot-appear-in-type-specifiers"></a>Les tailles de tableau ne peuvent pas figurer dans les spécificateurs de type
Les tailles de tableau ne peuvent pas être déclarés en tant que partie d’un spécificateur de type de données.  
  
 **ID d’erreur :** BC30638  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Spécifiez la taille du tableau qui suit immédiatement le nom de variable au lieu de passer la taille du tableau après le type, comme illustré dans l’exemple suivant.  
  
    ```  
    Dim Array(8) As Integer   
    ```  
  
-   Définir un tableau et initialisez-le avec le nombre voulu d’éléments, comme indiqué dans l’exemple suivant.  
  
    ```  
    Dim Array2() As Integer = New Integer(8) {}  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 [Tableaux](../../../visual-basic/programming-guide/language-features/arrays/index.md)
