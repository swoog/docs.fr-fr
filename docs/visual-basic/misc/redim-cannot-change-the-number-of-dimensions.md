---
title: "'ReDim' ne peut pas changer le nombre de dimensions"
ms.date: 07/20/2015
f1_keywords:
- vbrArray_RankMismatch
ms.assetid: 52505298-9985-4682-8f6e-ff7d56077f34
ms.openlocfilehash: 1e9695bbc7f104aa741de232f1f6d3c76df2cebf
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64591751"
---
# <a name="redim-cannot-change-the-number-of-dimensions"></a><span data-ttu-id="926f4-102">'ReDim' ne peut pas changer le nombre de dimensions</span><span class="sxs-lookup"><span data-stu-id="926f4-102">'ReDim' cannot change the number of dimensions</span></span>
<span data-ttu-id="926f4-103">Une opération tente d’utiliser l’instruction `ReDim` pour modifier le rang (nombre de dimensions) d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="926f4-103">An operation attempts to use the `ReDim` statement to change the rank (number of dimensions) of an array.</span></span> <span data-ttu-id="926f4-104">L’instruction`ReDim` peut modifier la taille d’une ou plusieurs dimensions d’un tableau qui a déjà été déclaré en bonne et due forme, mais elle ne peut pas modifier le rang d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="926f4-104">`ReDim` can change the size of one or more dimensions of an array that has already been formally declared, but it cannot change an array's rank.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="926f4-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="926f4-105">To correct this error</span></span>  
  
- <span data-ttu-id="926f4-106">Assurez-vous de bien vouloir modifier le rang du tableau et non la taille de ses dimensions et, si possible, utilisez `Dim` pour déclarer un nouveau tableau avec le rang souhaité.</span><span class="sxs-lookup"><span data-stu-id="926f4-106">Ensure that you intend to change the array's rank and not the sizes of its dimensions, and if possible, use `Dim` to declare a new array with the desired rank.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="926f4-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="926f4-107">See also</span></span>

- [<span data-ttu-id="926f4-108">Tableaux en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="926f4-108">Arrays in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/arrays/index.md)
- [<span data-ttu-id="926f4-109">Dimensions du tableau en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="926f4-109">Array dimensions in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/arrays/array-dimensions.md)
- [<span data-ttu-id="926f4-110">ReDim (instruction)</span><span class="sxs-lookup"><span data-stu-id="926f4-110">ReDim Statement</span></span>](../../visual-basic/language-reference/statements/redim-statement.md)
- [<span data-ttu-id="926f4-111">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="926f4-111">Dim Statement</span></span>](../../visual-basic/language-reference/statements/dim-statement.md)
