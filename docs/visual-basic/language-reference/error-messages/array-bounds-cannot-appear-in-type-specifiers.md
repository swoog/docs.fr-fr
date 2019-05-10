---
title: Les tailles de tableau ne peuvent pas figurer dans les spécificateurs de type
ms.date: 07/20/2015
f1_keywords:
- vbc30638
- bc30638
helpviewer_keywords:
- BC30638
ms.assetid: 93b654f4-70fa-4a48-baed-ffae42075550
ms.openlocfilehash: 50e1cd0e41da467a9e816c8e5d64d09a36923d65
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64665747"
---
# <a name="array-bounds-cannot-appear-in-type-specifiers"></a><span data-ttu-id="546ce-102">Les tailles de tableau ne peuvent pas figurer dans les spécificateurs de type</span><span class="sxs-lookup"><span data-stu-id="546ce-102">Array bounds cannot appear in type specifiers</span></span>
<span data-ttu-id="546ce-103">Les tailles de tableau ne peuvent pas être déclarés en tant que partie d’un spécificateur de type de données.</span><span class="sxs-lookup"><span data-stu-id="546ce-103">Array sizes cannot be declared as part of a data type specifier.</span></span>  
  
 <span data-ttu-id="546ce-104">**ID d’erreur :** BC30638</span><span class="sxs-lookup"><span data-stu-id="546ce-104">**Error ID:** BC30638</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="546ce-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="546ce-105">To correct this error</span></span>  
  
- <span data-ttu-id="546ce-106">Spécifiez la taille du tableau qui suit immédiatement le nom de variable au lieu de passer la taille du tableau après le type, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="546ce-106">Specify the size of the array immediately following the variable name instead of placing the array size after the type, as shown in the following example.</span></span>  
  
    ```  
    Dim Array(8) As Integer   
    ```  
  
- <span data-ttu-id="546ce-107">Définir un tableau et initialisez-le avec le nombre souhaité d’éléments, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="546ce-107">Define an array and initialize it with the desired number of elements, as shown in the following example.</span></span>  
  
    ```  
    Dim Array2() As Integer = New Integer(8) {}  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="546ce-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="546ce-108">See also</span></span>

- [<span data-ttu-id="546ce-109">Tableaux</span><span class="sxs-lookup"><span data-stu-id="546ce-109">Arrays</span></span>](../../../visual-basic/programming-guide/language-features/arrays/index.md)
