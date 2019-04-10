---
title: Les tableaux déclarés en tant que membres de structures ne peuvent pas être déclarés avec une taille initiale
ms.date: 07/20/2015
f1_keywords:
- vbc31043
- bc31043
helpviewer_keywords:
- BC31043
ms.assetid: 5bd90c71-1b78-444b-91e1-4789451ef085
ms.openlocfilehash: 5d58b531b670715716e849cd37227bc899195df6
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59335301"
---
# <a name="arrays-declared-as-structure-members-cannot-be-declared-with-an-initial-size"></a><span data-ttu-id="9c1c9-102">Les tableaux déclarés en tant que membres de structures ne peuvent pas être déclarés avec une taille initiale</span><span class="sxs-lookup"><span data-stu-id="9c1c9-102">Arrays declared as structure members cannot be declared with an initial size</span></span>
<span data-ttu-id="9c1c9-103">Un tableau dans une structure est déclaré avec une taille initiale.</span><span class="sxs-lookup"><span data-stu-id="9c1c9-103">An array in a structure is declared with an initial size.</span></span> <span data-ttu-id="9c1c9-104">Vous ne pouvez pas initialiser n’importe quel élément de structure et déclaration d’une taille de tableau est une forme d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="9c1c9-104">You cannot initialize any structure element, and declaring an array size is one form of initialization.</span></span>  
  
 <span data-ttu-id="9c1c9-105">**ID d’erreur :** BC31043</span><span class="sxs-lookup"><span data-stu-id="9c1c9-105">**Error ID:** BC31043</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="9c1c9-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="9c1c9-106">To correct this error</span></span>  
  
1. <span data-ttu-id="9c1c9-107">Définir le tableau dans votre structure comme dynamique (sans taille initiale).</span><span class="sxs-lookup"><span data-stu-id="9c1c9-107">Define the array in your structure as dynamic (no initial size).</span></span>  
  
2. <span data-ttu-id="9c1c9-108">Si vous avez besoin d’une certaine taille du tableau, vous pouvez redimensionner un tableau dynamique avec un [instruction ReDim](../../../visual-basic/language-reference/statements/redim-statement.md) lorsque votre code s’exécute.</span><span class="sxs-lookup"><span data-stu-id="9c1c9-108">If you require a certain size of array, you can redimension a dynamic array with a [ReDim Statement](../../../visual-basic/language-reference/statements/redim-statement.md) when your code is running.</span></span> <span data-ttu-id="9c1c9-109">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="9c1c9-109">The following example illustrates this.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="9c1c9-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c1c9-110">See also</span></span>

- [<span data-ttu-id="9c1c9-111">Tableaux</span><span class="sxs-lookup"><span data-stu-id="9c1c9-111">Arrays</span></span>](../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [<span data-ttu-id="9c1c9-112">Procédure : Déclarer une Structure</span><span class="sxs-lookup"><span data-stu-id="9c1c9-112">How to: Declare a Structure</span></span>](../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
