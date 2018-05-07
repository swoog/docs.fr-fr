---
title: Les tableaux déclarés en tant que membres de structures ne peuvent pas être déclarés avec une taille initiale
ms.date: 07/20/2015
f1_keywords:
- vbc31043
- bc31043
helpviewer_keywords:
- BC31043
ms.assetid: 5bd90c71-1b78-444b-91e1-4789451ef085
ms.openlocfilehash: 0a7424e5dbfadd78c4071ba5b76086b7f6c9b94a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="arrays-declared-as-structure-members-cannot-be-declared-with-an-initial-size"></a>Les tableaux déclarés en tant que membres de structures ne peuvent pas être déclarés avec une taille initiale
Un tableau dans une structure est déclaré avec une taille initiale. Vous ne pouvez pas initialiser n’importe quel élément de structure, et la déclaration d’une taille de tableau est une forme de l’initialisation.  
  
 **ID d’erreur :** BC31043  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Définissez le tableau dans votre structure en tant que dynamique (sans taille initiale).  
  
2.  Si vous avez besoin d’une certaine taille de tableau, vous pouvez redimensionner un tableau dynamique avec un [instruction ReDim](../../../visual-basic/language-reference/statements/redim-statement.md) lorsque votre code est en cours d’exécution. L'exemple suivant illustre ce comportement.  
  
    ```  
    Structure demoStruct  
        Public demoArray() As Integer  
    End Structure  
    Sub useStruct()  
        Dim struct As demoStruct  
        ReDim struct.demoArray(9)  
        Struct.demoArray(2) = 777  
    End Sub  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 [Tableaux](../../../visual-basic/programming-guide/language-features/arrays/index.md)  
 [Guide pratique : déclarer une structure](../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
