---
title: Aucune méthode 'Main' accessible avec une signature appropriée n'a été trouvée dans '<name>'
ms.date: 07/20/2015
f1_keywords:
- bc30737
- vbc30737
helpviewer_keywords:
- BC30737
ms.assetid: 3f40bacd-3fac-4741-b204-852f693d4340
ms.openlocfilehash: f5053bddf4b9ba791ad6d0733e1dd89c4ded91bd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58818356"
---
# <a name="no-accessible-main-method-with-an-appropriate-signature-was-found-in-name"></a><span data-ttu-id="1579f-102">Aucune méthode 'Main' accessible avec une signature appropriée a été trouvée dans '\<nom >'</span><span class="sxs-lookup"><span data-stu-id="1579f-102">No accessible 'Main' method with an appropriate signature was found in '\<name>'</span></span>
<span data-ttu-id="1579f-103">Applications de ligne de commande doivent avoir un `Sub Main` défini.</span><span class="sxs-lookup"><span data-stu-id="1579f-103">Command-line applications must have a `Sub Main` defined.</span></span> <span data-ttu-id="1579f-104">`Main` doit être déclarée comme `Public Shared` si elle est définie dans une classe, ou en tant que `Public` s’il est défini dans un module.</span><span class="sxs-lookup"><span data-stu-id="1579f-104">`Main` must be declared as `Public Shared` if it is defined in a class, or as `Public` if defined in a module.</span></span>  
  
 <span data-ttu-id="1579f-105">**ID d’erreur :** BC30737</span><span class="sxs-lookup"><span data-stu-id="1579f-105">**Error ID:** BC30737</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="1579f-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="1579f-106">To correct this error</span></span>  
  
-   <span data-ttu-id="1579f-107">Définir un `Public Sub Main` procédure pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="1579f-107">Define a `Public Sub Main` procedure for your project.</span></span> <span data-ttu-id="1579f-108">Déclarez-le en tant que `Shared` si et seulement si vous la définissez au sein d’une classe.</span><span class="sxs-lookup"><span data-stu-id="1579f-108">Declare it as `Shared` if and only if you define it inside a class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1579f-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1579f-109">See also</span></span>

- [<span data-ttu-id="1579f-110">Structure d’un programme Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1579f-110">Structure of a Visual Basic Program</span></span>](../../../visual-basic/programming-guide/program-structure/structure-of-a-visual-basic-program.md)
- [<span data-ttu-id="1579f-111">Procédures</span><span class="sxs-lookup"><span data-stu-id="1579f-111">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)
