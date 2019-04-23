---
title: Un caractère '.' ou '!' de début ne peut apparaître que dans une instruction 'With'
ms.date: 07/20/2015
f1_keywords:
- vbc30157
- bc30157
helpviewer_keywords:
- BC30157
ms.assetid: 70daaee1-14f9-45b7-9f30-53794310b95e
ms.openlocfilehash: 15390fb506fe9bca10f6917f5b26451a5569bece
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59322847"
---
# <a name="leading--or--can-only-appear-inside-a-with-statement"></a><span data-ttu-id="37de2-102">Un caractère '.' ou '!' de début ne peut apparaître que dans une instruction 'With'</span><span class="sxs-lookup"><span data-stu-id="37de2-102">Leading '.' or '!' can only appear inside a 'With' statement</span></span>
<span data-ttu-id="37de2-103">Un point (.) ou un point d’exclamation ( !) qui n’est pas à l’intérieur un `With` bloc se produit sans expression à gauche.</span><span class="sxs-lookup"><span data-stu-id="37de2-103">A period (.) or exclamation point (!) that is not inside a `With` block occurs without an expression on the left.</span></span> <span data-ttu-id="37de2-104">Accès au membre (`.`) et l’accès au membre de dictionnaire (`!`) nécessitent une expression spécifiant l’élément qui contient le membre.</span><span class="sxs-lookup"><span data-stu-id="37de2-104">Member access (`.`) and dictionary member access (`!`) require an expression specifying the element that contains the member.</span></span> <span data-ttu-id="37de2-105">Cela doit apparaître immédiatement à gauche de l’accesseur ou comme cible d’un `With` bloc contenant l’accès au membre.</span><span class="sxs-lookup"><span data-stu-id="37de2-105">This must appear immediately to the left of the accessor or as the target of a `With` block containing the member access.</span></span>  
  
 <span data-ttu-id="37de2-106">**ID d’erreur :** BC30157</span><span class="sxs-lookup"><span data-stu-id="37de2-106">**Error ID:** BC30157</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="37de2-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="37de2-107">To correct this error</span></span>  
  
1. <span data-ttu-id="37de2-108">Vérifiez que le `With` bloc est correctement formaté.</span><span class="sxs-lookup"><span data-stu-id="37de2-108">Ensure that the `With` block is correctly formatted.</span></span>  
  
2. <span data-ttu-id="37de2-109">S’il existe aucune `With` bloquer, ajoutez une expression à gauche de l’accesseur qui correspond à un élément défini contenant le membre.</span><span class="sxs-lookup"><span data-stu-id="37de2-109">If there is no `With` block, add an expression to the left of the accessor that evaluates to a defined element containing the member.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37de2-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37de2-110">See also</span></span>

- [<span data-ttu-id="37de2-111">Caractères spéciaux dans le code</span><span class="sxs-lookup"><span data-stu-id="37de2-111">Special Characters in Code</span></span>](../../../visual-basic/programming-guide/program-structure/special-characters-in-code.md)
- [<span data-ttu-id="37de2-112">With...End With (instruction)</span><span class="sxs-lookup"><span data-stu-id="37de2-112">With...End With Statement</span></span>](../../../visual-basic/language-reference/statements/with-end-with-statement.md)
