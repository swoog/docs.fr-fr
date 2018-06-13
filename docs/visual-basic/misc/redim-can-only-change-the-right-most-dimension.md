---
title: '&#39;ReDim&#39; peut changer que la dimension la plus à droite'
ms.date: 07/20/2015
f1_keywords:
- vbrArray_TypeMismatch
ms.assetid: d53cf41b-7a7a-466c-a29a-920d99698fa9
ms.openlocfilehash: efb98df13a7e3e378347b30b6fc00b90030ec194
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33641181"
---
# <a name="39redim39-can-only-change-the-right-most-dimension"></a><span data-ttu-id="b9218-102">&#39;ReDim&#39; peut changer que la dimension la plus à droite</span><span class="sxs-lookup"><span data-stu-id="b9218-102">&#39;ReDim&#39; can only change the right-most dimension</span></span>
<span data-ttu-id="b9218-103">Une instruction `ReDim` a tenté d’utiliser le mot clé `Preserve` pour modifier une dimension d’un tableau qui n’est pas la dernière dimension.</span><span class="sxs-lookup"><span data-stu-id="b9218-103">A `ReDim` statement attempted to use the `Preserve` keyword to change a dimension of an array that is not the last dimension.</span></span> <span data-ttu-id="b9218-104">Lors de l’utilisation de `Preserve`, vous pouvez redimensionner uniquement la dernière dimension d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="b9218-104">When using `Preserve`, you can resize only the last dimension of an array.</span></span> <span data-ttu-id="b9218-105">Pour toutes les autres dimensions, vous devez spécifier la même taille que pour le tableau existant.</span><span class="sxs-lookup"><span data-stu-id="b9218-105">For all other dimensions, you must specify the same size as for the existing array.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b9218-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="b9218-106">To correct this error</span></span>  
  
-   <span data-ttu-id="b9218-107">Supprimez le mot clé `Preserve` .</span><span class="sxs-lookup"><span data-stu-id="b9218-107">Remove the `Preserve` keyword.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9218-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9218-108">See Also</span></span>  
 [<span data-ttu-id="b9218-109">Tableaux en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b9218-109">Arrays in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/arrays/index.md)  
 [<span data-ttu-id="b9218-110">Dimensions du tableau dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b9218-110">Array dimensions in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/arrays/array-dimensions.md)  
 [<span data-ttu-id="b9218-111">ReDim (instruction)</span><span class="sxs-lookup"><span data-stu-id="b9218-111">ReDim Statement</span></span>](../../visual-basic/language-reference/statements/redim-statement.md)  
 [<span data-ttu-id="b9218-112">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="b9218-112">Dim Statement</span></span>](../../visual-basic/language-reference/statements/dim-statement.md)  
 [<span data-ttu-id="b9218-113">Conserver - supprimer</span><span class="sxs-lookup"><span data-stu-id="b9218-113">Preserve - delete</span></span>](http://msdn.microsoft.com/library/91badeab-b4e0-48b6-92c9-9f0c8f995d81)
