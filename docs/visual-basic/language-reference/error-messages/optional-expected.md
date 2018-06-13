---
title: '&#39;Facultatif&#39; attendu'
ms.date: 07/20/2015
f1_keywords:
- bc30202
- vbc30202
helpviewer_keywords:
- BC30202
ms.assetid: 6f75060c-2db4-4a79-b5d1-5780c09a74cd
ms.openlocfilehash: 52e4288255a246f78730b33beb55f6d2d83ff214
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33593952"
---
# <a name="39optional39-expected"></a><span data-ttu-id="25029-102">&#39;Facultatif&#39; attendu</span><span class="sxs-lookup"><span data-stu-id="25029-102">&#39;Optional&#39; expected</span></span>
<span data-ttu-id="25029-103">Un argument facultatif dans une déclaration de procédure est suivi d’un argument obligatoire.</span><span class="sxs-lookup"><span data-stu-id="25029-103">An optional argument in a procedure declaration is followed by a required argument.</span></span> <span data-ttu-id="25029-104">Chaque argument d’un argument facultatif doit également être facultatif.</span><span class="sxs-lookup"><span data-stu-id="25029-104">Every argument following an optional argument must also be optional.</span></span>  
  
 <span data-ttu-id="25029-105">**ID d’erreur :** BC30202</span><span class="sxs-lookup"><span data-stu-id="25029-105">**Error ID:** BC30202</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="25029-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="25029-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="25029-107">Si l’argument est destiné à être nécessaire, déplacez afin qu’il précède le premier argument facultatif dans la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="25029-107">If the argument is intended to be required, move it to precede the first optional argument in the argument list.</span></span>  
  
2.  <span data-ttu-id="25029-108">Si l’argument est destiné à être facultatif, utilisez le `Optional` (mot clé).</span><span class="sxs-lookup"><span data-stu-id="25029-108">If the argument is intended to be optional, use the `Optional` keyword.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25029-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25029-109">See Also</span></span>  
 [<span data-ttu-id="25029-110">Paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="25029-110">Optional Parameters</span></span>](../../../visual-basic/programming-guide/language-features/procedures/optional-parameters.md)
