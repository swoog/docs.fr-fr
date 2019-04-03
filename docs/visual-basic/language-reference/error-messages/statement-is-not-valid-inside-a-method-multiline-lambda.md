---
title: Instruction n’est pas valide à l’intérieur d’une expression lambda multiligne (méthode)
ms.date: 07/20/2015
f1_keywords:
- vbc30024
- bc30024
helpviewer_keywords:
- BC30024
ms.assetid: 758e7a8f-429b-42c1-9a78-778e5b480e04
ms.openlocfilehash: 994cafc44a37d16d0f70caec560f530c6a836ec0
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58841561"
---
# <a name="statement-is-not-valid-inside-a-methodmultiline-lambda"></a><span data-ttu-id="f0b26-102">Instruction non valide dans une méthode ou une expression lambda multiligne</span><span class="sxs-lookup"><span data-stu-id="f0b26-102">Statement is not valid inside a method/multiline lambda</span></span>
<span data-ttu-id="f0b26-103">L’instruction n’est pas valide dans un `Sub`, `Function`, propriété `Get`, ou une propriété `Set` procédure.</span><span class="sxs-lookup"><span data-stu-id="f0b26-103">The statement is not valid within a `Sub`, `Function`, property `Get`, or property `Set` procedure.</span></span> <span data-ttu-id="f0b26-104">Certaines instructions peuvent être placées au niveau du module ou de la classe.</span><span class="sxs-lookup"><span data-stu-id="f0b26-104">Some statements can be placed at the module or class level.</span></span> <span data-ttu-id="f0b26-105">D’autres, tels que `Option Strict`, doit être au niveau de l’espace de noms et précéder toutes les autres déclarations.</span><span class="sxs-lookup"><span data-stu-id="f0b26-105">Others, such as `Option Strict`, must be at namespace level and precede all other declarations.</span></span>  
  
 <span data-ttu-id="f0b26-106">**ID d’erreur :** BC30024</span><span class="sxs-lookup"><span data-stu-id="f0b26-106">**Error ID:** BC30024</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f0b26-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f0b26-107">To correct this error</span></span>  
  
-   <span data-ttu-id="f0b26-108">Supprimez l’instruction de la procédure.</span><span class="sxs-lookup"><span data-stu-id="f0b26-108">Remove the statement from the procedure.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0b26-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0b26-109">See also</span></span>

- [<span data-ttu-id="f0b26-110">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="f0b26-110">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)
- [<span data-ttu-id="f0b26-111">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="f0b26-111">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)
- [<span data-ttu-id="f0b26-112">Get (instruction)</span><span class="sxs-lookup"><span data-stu-id="f0b26-112">Get Statement</span></span>](../../../visual-basic/language-reference/statements/get-statement.md)
- [<span data-ttu-id="f0b26-113">Set (instruction)</span><span class="sxs-lookup"><span data-stu-id="f0b26-113">Set Statement</span></span>](../../../visual-basic/language-reference/statements/set-statement.md)
