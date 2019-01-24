---
title: Les tableaux déclarés en tant que membres de structures ne peuvent pas être déclarés avec une taille initiale
ms.date: 07/20/2015
f1_keywords:
- vbc31043
- bc31043
helpviewer_keywords:
- BC31043
ms.assetid: 5bd90c71-1b78-444b-91e1-4789451ef085
ms.openlocfilehash: 06e5e36f3e0522e0449c0ef9698f3a1b01b9cb5f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549065"
---
# <a name="arrays-declared-as-structure-members-cannot-be-declared-with-an-initial-size"></a>Les tableaux déclarés en tant que membres de structures ne peuvent pas être déclarés avec une taille initiale
Un tableau dans une structure est déclaré avec une taille initiale. Vous ne pouvez pas initialiser n’importe quel élément de structure et déclaration d’une taille de tableau est une forme d’initialisation.  
  
 **ID d’erreur :** BC31043  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Définir le tableau dans votre structure comme dynamique (sans taille initiale).  
  
2.  Si vous avez besoin d’une certaine taille du tableau, vous pouvez redimensionner un tableau dynamique avec un [instruction ReDim](../../../visual-basic/language-reference/statements/redim-statement.md) lorsque votre code s’exécute. L'exemple suivant illustre ce comportement.  
  
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
- [Tableaux](../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [Guide pratique pour déclarer une structure](../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
