---
title: '&#39;ReDim&#39; ne pouvez modifier la dimension la plus à droite'
ms.date: 07/20/2015
f1_keywords:
- vbrArray_TypeMismatch
ms.assetid: d53cf41b-7a7a-466c-a29a-920d99698fa9
ms.openlocfilehash: 94e0fe81f7e750a67943b68f2db700e3a7831da1
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43482715"
---
# <a name="39redim39-can-only-change-the-right-most-dimension"></a><span data-ttu-id="60928-102">&#39;ReDim&#39; ne pouvez modifier la dimension la plus à droite</span><span class="sxs-lookup"><span data-stu-id="60928-102">&#39;ReDim&#39; can only change the right-most dimension</span></span>
<span data-ttu-id="60928-103">Une instruction `ReDim` a tenté d’utiliser le mot clé `Preserve` pour modifier une dimension d’un tableau qui n’est pas la dernière dimension.</span><span class="sxs-lookup"><span data-stu-id="60928-103">A `ReDim` statement attempted to use the `Preserve` keyword to change a dimension of an array that is not the last dimension.</span></span> <span data-ttu-id="60928-104">Lors de l’utilisation de `Preserve`, vous pouvez redimensionner uniquement la dernière dimension d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="60928-104">When using `Preserve`, you can resize only the last dimension of an array.</span></span> <span data-ttu-id="60928-105">Pour toutes les autres dimensions, vous devez spécifier la même taille que pour le tableau existant.</span><span class="sxs-lookup"><span data-stu-id="60928-105">For all other dimensions, you must specify the same size as for the existing array.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="60928-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="60928-106">To correct this error</span></span>  
  
-   <span data-ttu-id="60928-107">Supprimez le mot clé `Preserve` .</span><span class="sxs-lookup"><span data-stu-id="60928-107">Remove the `Preserve` keyword.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="60928-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60928-108">See Also</span></span>  
 [<span data-ttu-id="60928-109">Tableaux en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="60928-109">Arrays in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/arrays/index.md)  
 [<span data-ttu-id="60928-110">Dimensions du tableau en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="60928-110">Array dimensions in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/arrays/array-dimensions.md)  
 [<span data-ttu-id="60928-111">ReDim (instruction)</span><span class="sxs-lookup"><span data-stu-id="60928-111">ReDim Statement</span></span>](../../visual-basic/language-reference/statements/redim-statement.md)  
 [<span data-ttu-id="60928-112">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="60928-112">Dim Statement</span></span>](../../visual-basic/language-reference/statements/dim-statement.md)  
 [<span data-ttu-id="60928-113">Conserver - supprimer</span><span class="sxs-lookup"><span data-stu-id="60928-113">Preserve - delete</span></span>](https://msdn.microsoft.com/library/91badeab-b4e0-48b6-92c9-9f0c8f995d81)
