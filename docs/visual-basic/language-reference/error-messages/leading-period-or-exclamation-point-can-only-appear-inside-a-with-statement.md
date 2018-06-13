---
title: Début &#39;. &#39; ou &#39;! &#39; ne peut apparaître qu’à l’intérieur d’un &#39;avec&#39; instruction
ms.date: 07/20/2015
f1_keywords:
- vbc30157
- bc30157
helpviewer_keywords:
- BC30157
ms.assetid: 70daaee1-14f9-45b7-9f30-53794310b95e
ms.openlocfilehash: 7802b8e0aaf3dff83d5bfbe11f0b8bb1b5bb46cb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33589445"
---
# <a name="leading-3939-or-3939-can-only-appear-inside-a-39with39-statement"></a><span data-ttu-id="f2ec2-102">Début &#39;. &#39; ou &#39;! &#39; ne peut apparaître qu’à l’intérieur d’un &#39;avec&#39; instruction</span><span class="sxs-lookup"><span data-stu-id="f2ec2-102">Leading &#39;.&#39; or &#39;!&#39; can only appear inside a &#39;With&#39; statement</span></span>
<span data-ttu-id="f2ec2-103">Un point (.) ou un point d’exclamation ( !) qui n’est pas à l’intérieur un `With` bloc se produit sans expression à gauche.</span><span class="sxs-lookup"><span data-stu-id="f2ec2-103">A period (.) or exclamation point (!) that is not inside a `With` block occurs without an expression on the left.</span></span> <span data-ttu-id="f2ec2-104">Accès aux membres (`.`) et l’accès au membre dictionnaire (`!`) requiert une expression spécifiant l’élément qui contient le membre.</span><span class="sxs-lookup"><span data-stu-id="f2ec2-104">Member access (`.`) and dictionary member access (`!`) require an expression specifying the element that contains the member.</span></span> <span data-ttu-id="f2ec2-105">Celui-ci doit apparaître immédiatement à gauche de l’accesseur ou comme cible d’un `With` bloc contenant l’accès au membre.</span><span class="sxs-lookup"><span data-stu-id="f2ec2-105">This must appear immediately to the left of the accessor or as the target of a `With` block containing the member access.</span></span>  
  
 <span data-ttu-id="f2ec2-106">**ID d’erreur :** BC30157</span><span class="sxs-lookup"><span data-stu-id="f2ec2-106">**Error ID:** BC30157</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f2ec2-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f2ec2-107">To correct this error</span></span>  
  
1.  <span data-ttu-id="f2ec2-108">Vérifiez que le `With` bloc est correctement formaté.</span><span class="sxs-lookup"><span data-stu-id="f2ec2-108">Ensure that the `With` block is correctly formatted.</span></span>  
  
2.  <span data-ttu-id="f2ec2-109">S’il existe aucune `With` bloquer, ajoutez une expression à gauche de l’accesseur qui correspond à un élément défini contenant le membre.</span><span class="sxs-lookup"><span data-stu-id="f2ec2-109">If there is no `With` block, add an expression to the left of the accessor that evaluates to a defined element containing the member.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2ec2-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2ec2-110">See Also</span></span>  
 [<span data-ttu-id="f2ec2-111">Caractères spéciaux dans le code</span><span class="sxs-lookup"><span data-stu-id="f2ec2-111">Special Characters in Code</span></span>](../../../visual-basic/programming-guide/program-structure/special-characters-in-code.md)  
 [<span data-ttu-id="f2ec2-112">With...End With (instruction)</span><span class="sxs-lookup"><span data-stu-id="f2ec2-112">With...End With Statement</span></span>](../../../visual-basic/language-reference/statements/with-end-with-statement.md)
