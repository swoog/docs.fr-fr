---
title: Non accessible &#39;principal&#39; méthode avec une signature appropriée a été trouvé dans &#39; &lt;nom&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- bc30737
- vbc30737
helpviewer_keywords:
- BC30737
ms.assetid: 3f40bacd-3fac-4741-b204-852f693d4340
ms.openlocfilehash: 6a60e26a2bd0e31c0f92dbbfb2518c75f304d9f1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33593218"
---
# <a name="no-accessible-39main39-method-with-an-appropriate-signature-was-found-in-39ltnamegt39"></a><span data-ttu-id="55b48-102">Non accessible &#39;principal&#39; méthode avec une signature appropriée a été trouvé dans &#39; &lt;nom&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="55b48-102">No accessible &#39;Main&#39; method with an appropriate signature was found in &#39;&lt;name&gt;&#39;</span></span>
<span data-ttu-id="55b48-103">Les applications de ligne de commande doivent avoir un `Sub Main` défini.</span><span class="sxs-lookup"><span data-stu-id="55b48-103">Command-line applications must have a `Sub Main` defined.</span></span> <span data-ttu-id="55b48-104">`Main` doit être déclarée comme `Public Shared` si elle est définie dans une classe, ou en tant que `Public` s’il est défini dans un module.</span><span class="sxs-lookup"><span data-stu-id="55b48-104">`Main` must be declared as `Public Shared` if it is defined in a class, or as `Public` if defined in a module.</span></span>  
  
 <span data-ttu-id="55b48-105">**ID d’erreur :** BC30737</span><span class="sxs-lookup"><span data-stu-id="55b48-105">**Error ID:** BC30737</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="55b48-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="55b48-106">To correct this error</span></span>  
  
-   <span data-ttu-id="55b48-107">Définir un `Public Sub Main` procédure pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="55b48-107">Define a `Public Sub Main` procedure for your project.</span></span> <span data-ttu-id="55b48-108">Déclarez-le en tant que `Shared` si et seulement si vous la définissez au sein d’une classe.</span><span class="sxs-lookup"><span data-stu-id="55b48-108">Declare it as `Shared` if and only if you define it inside a class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="55b48-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55b48-109">See Also</span></span>  
 [<span data-ttu-id="55b48-110">Structure d’un programme Visual Basic</span><span class="sxs-lookup"><span data-stu-id="55b48-110">Structure of a Visual Basic Program</span></span>](../../../visual-basic/programming-guide/program-structure/structure-of-a-visual-basic-program.md)  
 [<span data-ttu-id="55b48-111">Procédures</span><span class="sxs-lookup"><span data-stu-id="55b48-111">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)
