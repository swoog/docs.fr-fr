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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59341879"
---
# <a name="optional-expected"></a><span data-ttu-id="bfa1a-102">'Optional' attendu</span><span class="sxs-lookup"><span data-stu-id="bfa1a-102">'Optional' expected</span></span>
<span data-ttu-id="bfa1a-103">Un argument facultatif dans une déclaration de procédure est suivi d’un argument obligatoire.</span><span class="sxs-lookup"><span data-stu-id="bfa1a-103">An optional argument in a procedure declaration is followed by a required argument.</span></span> <span data-ttu-id="bfa1a-104">Tous les arguments qui suivent un argument facultatif doivent également être facultatifs.</span><span class="sxs-lookup"><span data-stu-id="bfa1a-104">Every argument following an optional argument must also be optional.</span></span>  
  
 <span data-ttu-id="bfa1a-105">**ID d’erreur :** BC30202</span><span class="sxs-lookup"><span data-stu-id="bfa1a-105">**Error ID:** BC30202</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="bfa1a-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="bfa1a-106">To correct this error</span></span>  
  
1. <span data-ttu-id="bfa1a-107">Si l’argument est destiné à être requis, déplacez-le à faire précéder le premier argument facultatif dans la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="bfa1a-107">If the argument is intended to be required, move it to precede the first optional argument in the argument list.</span></span>  
  
2. <span data-ttu-id="bfa1a-108">Si l’argument est destiné à être facultatif, utilisez le `Optional` mot clé.</span><span class="sxs-lookup"><span data-stu-id="bfa1a-108">If the argument is intended to be optional, use the `Optional` keyword.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bfa1a-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfa1a-109">See also</span></span>

- [<span data-ttu-id="bfa1a-110">Paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="bfa1a-110">Optional Parameters</span></span>](../../../visual-basic/programming-guide/language-features/procedures/optional-parameters.md)
