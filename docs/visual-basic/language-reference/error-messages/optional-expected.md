---
title: "'Optional' attendu"
ms.date: 07/20/2015
f1_keywords:
- bc30202
- vbc30202
helpviewer_keywords:
- BC30202
ms.assetid: 6f75060c-2db4-4a79-b5d1-5780c09a74cd
ms.openlocfilehash: 71a25784f357a7e596093b314ed5b3d721d6f92c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946586"
---
# <a name="optional-expected"></a><span data-ttu-id="c58d9-102">'Optional' attendu</span><span class="sxs-lookup"><span data-stu-id="c58d9-102">'Optional' expected</span></span>
<span data-ttu-id="c58d9-103">Un argument facultatif dans une déclaration de procédure est suivi d’un argument obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c58d9-103">An optional argument in a procedure declaration is followed by a required argument.</span></span> <span data-ttu-id="c58d9-104">Tous les arguments qui suivent un argument facultatif doivent également être facultatifs.</span><span class="sxs-lookup"><span data-stu-id="c58d9-104">Every argument following an optional argument must also be optional.</span></span>  
  
 <span data-ttu-id="c58d9-105">**ID d’erreur :** BC30202</span><span class="sxs-lookup"><span data-stu-id="c58d9-105">**Error ID:** BC30202</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="c58d9-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="c58d9-106">To correct this error</span></span>  
  
1. <span data-ttu-id="c58d9-107">Si l’argument est destiné à être requis, déplacez-le à faire précéder le premier argument facultatif dans la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="c58d9-107">If the argument is intended to be required, move it to precede the first optional argument in the argument list.</span></span>  
  
2. <span data-ttu-id="c58d9-108">Si l’argument est destiné à être facultatif, utilisez le `Optional` mot clé.</span><span class="sxs-lookup"><span data-stu-id="c58d9-108">If the argument is intended to be optional, use the `Optional` keyword.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c58d9-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c58d9-109">See also</span></span>

- [<span data-ttu-id="c58d9-110">Paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="c58d9-110">Optional Parameters</span></span>](../../../visual-basic/programming-guide/language-features/procedures/optional-parameters.md)
