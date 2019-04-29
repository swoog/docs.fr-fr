---
title: Les tailles de tableau ne peuvent pas figurer dans les spécificateurs de type
ms.date: 07/20/2015
f1_keywords:
- vbc30638
- bc30638
helpviewer_keywords:
- BC30638
ms.assetid: 93b654f4-70fa-4a48-baed-ffae42075550
ms.openlocfilehash: f20ed883005641082eb89e2effa5221594910ffe
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61935354"
---
# <a name="array-bounds-cannot-appear-in-type-specifiers"></a><span data-ttu-id="ffa35-102">Les tailles de tableau ne peuvent pas figurer dans les spécificateurs de type</span><span class="sxs-lookup"><span data-stu-id="ffa35-102">Array bounds cannot appear in type specifiers</span></span>
<span data-ttu-id="ffa35-103">Les tailles de tableau ne peuvent pas être déclarés en tant que partie d’un spécificateur de type de données.</span><span class="sxs-lookup"><span data-stu-id="ffa35-103">Array sizes cannot be declared as part of a data type specifier.</span></span>  
  
 <span data-ttu-id="ffa35-104">**ID d’erreur :** BC30638</span><span class="sxs-lookup"><span data-stu-id="ffa35-104">**Error ID:** BC30638</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ffa35-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="ffa35-105">To correct this error</span></span>  
  
- <span data-ttu-id="ffa35-106">Spécifiez la taille du tableau qui suit immédiatement le nom de variable au lieu de passer la taille du tableau après le type, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="ffa35-106">Specify the size of the array immediately following the variable name instead of placing the array size after the type, as shown in the following example.</span></span>  
  
    ```  
    Dim Array(8) As Integer   
    ```  
  
- <span data-ttu-id="ffa35-107">Définir un tableau et initialisez-le avec le nombre souhaité d’éléments, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="ffa35-107">Define an array and initialize it with the desired number of elements, as shown in the following example.</span></span>  
  
    ```  
    Dim Array2() As Integer = New Integer(8) {}  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="ffa35-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffa35-108">See also</span></span>

- [<span data-ttu-id="ffa35-109">Tableaux</span><span class="sxs-lookup"><span data-stu-id="ffa35-109">Arrays</span></span>](../../../visual-basic/programming-guide/language-features/arrays/index.md)
