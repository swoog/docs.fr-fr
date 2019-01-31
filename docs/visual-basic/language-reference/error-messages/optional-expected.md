---
title: "'Optional' attendu"
ms.date: 07/20/2015
f1_keywords:
- bc30202
- vbc30202
helpviewer_keywords:
- BC30202
ms.assetid: 6f75060c-2db4-4a79-b5d1-5780c09a74cd
ms.openlocfilehash: 0ad0d0890b73103a0678b13409a24190329d37d4
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266324"
---
# <a name="optional-expected"></a><span data-ttu-id="f1c01-102">'Optional' attendu</span><span class="sxs-lookup"><span data-stu-id="f1c01-102">'Optional' expected</span></span>
<span data-ttu-id="f1c01-103">Un argument facultatif dans une déclaration de procédure est suivi d’un argument obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f1c01-103">An optional argument in a procedure declaration is followed by a required argument.</span></span> <span data-ttu-id="f1c01-104">Tous les arguments qui suivent un argument facultatif doivent également être facultatifs.</span><span class="sxs-lookup"><span data-stu-id="f1c01-104">Every argument following an optional argument must also be optional.</span></span>  
  
 <span data-ttu-id="f1c01-105">**ID d’erreur :** BC30202</span><span class="sxs-lookup"><span data-stu-id="f1c01-105">**Error ID:** BC30202</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f1c01-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f1c01-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="f1c01-107">Si l’argument est destiné à être requis, déplacez-le à faire précéder le premier argument facultatif dans la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="f1c01-107">If the argument is intended to be required, move it to precede the first optional argument in the argument list.</span></span>  
  
2.  <span data-ttu-id="f1c01-108">Si l’argument est destiné à être facultatif, utilisez le `Optional` mot clé.</span><span class="sxs-lookup"><span data-stu-id="f1c01-108">If the argument is intended to be optional, use the `Optional` keyword.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1c01-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1c01-109">See also</span></span>
- [<span data-ttu-id="f1c01-110">Paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="f1c01-110">Optional Parameters</span></span>](../../../visual-basic/programming-guide/language-features/procedures/optional-parameters.md)
