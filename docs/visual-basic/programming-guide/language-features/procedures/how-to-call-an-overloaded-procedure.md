---
title: 'Comment : appeler une procédure surchargée (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], overloading
- procedures [Visual Basic], calling
- procedures [Visual Basic], multiple versions
- procedure calls [Visual Basic], overloaded
ms.assetid: 3bb331fb-f6bc-406f-9ca0-9609b497014c
ms.openlocfilehash: 802a312d6ec6640594f3c6b662202d1ffcf2376d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33649124"
---
# <a name="how-to-call-an-overloaded-procedure-visual-basic"></a><span data-ttu-id="b368f-102">Comment : appeler une procédure surchargée (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b368f-102">How to: Call an Overloaded Procedure (Visual Basic)</span></span>
<span data-ttu-id="b368f-103">L’avantage de la surcharge d’une procédure est la flexibilité de l’appel.</span><span class="sxs-lookup"><span data-stu-id="b368f-103">The advantage of overloading a procedure is in the flexibility of the call.</span></span> <span data-ttu-id="b368f-104">Le code appelant peut obtenir les informations que nécessaires pour passer à la procédure, puis appelez un seul nom de procédure, quel que soit les arguments, il passe.</span><span class="sxs-lookup"><span data-stu-id="b368f-104">The calling code can obtain the information it needs to pass to the procedure and then call a single procedure name, no matter what arguments it is passing.</span></span>  
  
### <a name="to-call-a-procedure-that-has-more-than-one-version-defined"></a><span data-ttu-id="b368f-105">Pour appeler une procédure qui possède plusieurs versions définies</span><span class="sxs-lookup"><span data-stu-id="b368f-105">To call a procedure that has more than one version defined</span></span>  
  
1.  <span data-ttu-id="b368f-106">Dans le code appelant, déterminez les données à passer à la procédure.</span><span class="sxs-lookup"><span data-stu-id="b368f-106">In the calling code, determine which data to pass to the procedure.</span></span>  
  
2.  <span data-ttu-id="b368f-107">Écrire l’appel de procédure de façon normale, présenter les données dans la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="b368f-107">Write the procedure call in the normal way, presenting the data in the argument list.</span></span> <span data-ttu-id="b368f-108">Assurez-vous que les arguments correspondent à la liste des paramètres de l’une des versions définies pour la procédure.</span><span class="sxs-lookup"><span data-stu-id="b368f-108">Be sure the arguments match the parameter list in one of the versions defined for the procedure.</span></span>  
  
3.  <span data-ttu-id="b368f-109">Il est inutile de déterminer la version de la procédure à appeler.</span><span class="sxs-lookup"><span data-stu-id="b368f-109">You do not have to determine which version of the procedure to call.</span></span> <span data-ttu-id="b368f-110">Visual Basic passe le contrôle à la version correspondant à votre liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="b368f-110">Visual Basic passes control to the version matching your argument list.</span></span>  
  
     <span data-ttu-id="b368f-111">L’exemple suivant appelle la `post` procédure déclarée dans [Comment : définir plusieurs Versions d’une procédure](./how-to-define-multiple-versions-of-a-procedure.md).</span><span class="sxs-lookup"><span data-stu-id="b368f-111">The following example calls the `post` procedure declared in [How to: Define Multiple Versions of a Procedure](./how-to-define-multiple-versions-of-a-procedure.md).</span></span> <span data-ttu-id="b368f-112">Il obtient l’identification de client, détermine s’il est un `String` ou `Integer`, puis, dans les deux cas, appelle la même procédure.</span><span class="sxs-lookup"><span data-stu-id="b368f-112">It obtains the customer identification, determines whether it is a `String` or an `Integer`, and then in either case calls the same procedure.</span></span>  
  
     [!code-vb[VbVbcnProcedures#56](./codesnippet/VisualBasic/how-to-call-an-overloaded-procedure_1.vb)]  
  
     [!code-vb[VbVbcnProcedures#57](./codesnippet/VisualBasic/how-to-call-an-overloaded-procedure_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="b368f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b368f-113">See Also</span></span>  
 [<span data-ttu-id="b368f-114">Procédures</span><span class="sxs-lookup"><span data-stu-id="b368f-114">Procedures</span></span>](./index.md)  
 [<span data-ttu-id="b368f-115">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="b368f-115">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)  
 [<span data-ttu-id="b368f-116">Surcharge de procédure</span><span class="sxs-lookup"><span data-stu-id="b368f-116">Procedure Overloading</span></span>](./procedure-overloading.md)  
 [<span data-ttu-id="b368f-117">Procédures de dépannage</span><span class="sxs-lookup"><span data-stu-id="b368f-117">Troubleshooting Procedures</span></span>](./troubleshooting-procedures.md)  
 [<span data-ttu-id="b368f-118">Guide pratique : définir plusieurs versions d’une procédure</span><span class="sxs-lookup"><span data-stu-id="b368f-118">How to: Define Multiple Versions of a Procedure</span></span>](./how-to-define-multiple-versions-of-a-procedure.md)  
 [<span data-ttu-id="b368f-119">Guide pratique : surcharger une procédure qui accepte des paramètres optionnels</span><span class="sxs-lookup"><span data-stu-id="b368f-119">How to: Overload a Procedure that Takes Optional Parameters</span></span>](./how-to-overload-a-procedure-that-takes-optional-parameters.md)  
 [<span data-ttu-id="b368f-120">Guide pratique : surcharger une procédure qui accepte un nombre indéfini de paramètres</span><span class="sxs-lookup"><span data-stu-id="b368f-120">How to: Overload a Procedure that Takes an Indefinite Number of Parameters</span></span>](./how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters.md)  
 [<span data-ttu-id="b368f-121">Considérations sur les surcharges de procédures</span><span class="sxs-lookup"><span data-stu-id="b368f-121">Considerations in Overloading Procedures</span></span>](./considerations-in-overloading-procedures.md)  
 [<span data-ttu-id="b368f-122">Résolution de surcharge</span><span class="sxs-lookup"><span data-stu-id="b368f-122">Overload Resolution</span></span>](./overload-resolution.md)  
 [<span data-ttu-id="b368f-123">Overloads</span><span class="sxs-lookup"><span data-stu-id="b368f-123">Overloads</span></span>](../../../../visual-basic/language-reference/modifiers/overloads.md)
