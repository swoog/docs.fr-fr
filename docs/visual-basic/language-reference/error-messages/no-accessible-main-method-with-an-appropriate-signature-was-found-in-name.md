---
title: Aucune méthode 'Main' accessible avec une signature appropriée n'a été trouvée dans '<name>'
ms.date: 07/20/2015
f1_keywords:
- bc30737
- vbc30737
helpviewer_keywords:
- BC30737
ms.assetid: 3f40bacd-3fac-4741-b204-852f693d4340
ms.openlocfilehash: 559c905d1e2e2de4500771a93d6116f9630011ba
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64591979"
---
# <a name="no-accessible-main-method-with-an-appropriate-signature-was-found-in-name"></a><span data-ttu-id="e0f0b-102">Aucune méthode 'Main' accessible avec une signature appropriée a été trouvée dans '\<nom >'</span><span class="sxs-lookup"><span data-stu-id="e0f0b-102">No accessible 'Main' method with an appropriate signature was found in '\<name>'</span></span>
<span data-ttu-id="e0f0b-103">Applications de ligne de commande doivent avoir un `Sub Main` défini.</span><span class="sxs-lookup"><span data-stu-id="e0f0b-103">Command-line applications must have a `Sub Main` defined.</span></span> <span data-ttu-id="e0f0b-104">`Main` doit être déclarée comme `Public Shared` si elle est définie dans une classe, ou en tant que `Public` s’il est défini dans un module.</span><span class="sxs-lookup"><span data-stu-id="e0f0b-104">`Main` must be declared as `Public Shared` if it is defined in a class, or as `Public` if defined in a module.</span></span>  
  
 <span data-ttu-id="e0f0b-105">**ID d’erreur :** BC30737</span><span class="sxs-lookup"><span data-stu-id="e0f0b-105">**Error ID:** BC30737</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="e0f0b-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="e0f0b-106">To correct this error</span></span>  
  
- <span data-ttu-id="e0f0b-107">Définir un `Public Sub Main` procédure pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="e0f0b-107">Define a `Public Sub Main` procedure for your project.</span></span> <span data-ttu-id="e0f0b-108">Déclarez-le en tant que `Shared` si et seulement si vous la définissez au sein d’une classe.</span><span class="sxs-lookup"><span data-stu-id="e0f0b-108">Declare it as `Shared` if and only if you define it inside a class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0f0b-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0f0b-109">See also</span></span>

- [<span data-ttu-id="e0f0b-110">Structure d’un programme Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e0f0b-110">Structure of a Visual Basic Program</span></span>](../../../visual-basic/programming-guide/program-structure/structure-of-a-visual-basic-program.md)
- [<span data-ttu-id="e0f0b-111">Procédures</span><span class="sxs-lookup"><span data-stu-id="e0f0b-111">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)
