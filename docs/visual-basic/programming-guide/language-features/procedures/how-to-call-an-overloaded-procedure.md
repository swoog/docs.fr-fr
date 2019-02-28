---
title: 'Procédure : Appeler une procédure surchargée (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], overloading
- procedures [Visual Basic], calling
- procedures [Visual Basic], multiple versions
- procedure calls [Visual Basic], overloaded
ms.assetid: 3bb331fb-f6bc-406f-9ca0-9609b497014c
ms.openlocfilehash: f13fdae9617fa2af21978979cad6f90a15140a4a
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56969997"
---
# <a name="how-to-call-an-overloaded-procedure-visual-basic"></a><span data-ttu-id="e5ec6-102">Procédure : Appeler une procédure surchargée (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e5ec6-102">How to: Call an Overloaded Procedure (Visual Basic)</span></span>
<span data-ttu-id="e5ec6-103">L’avantage de la surcharge d’une procédure est la flexibilité de l’appel.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-103">The advantage of overloading a procedure is in the flexibility of the call.</span></span> <span data-ttu-id="e5ec6-104">Le code appelant peut obtenir les informations que nécessaires pour passer à la procédure, puis appelez un seul nom de procédure, quel que soit les arguments, il a réussi.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-104">The calling code can obtain the information it needs to pass to the procedure and then call a single procedure name, no matter what arguments it is passing.</span></span>  
  
### <a name="to-call-a-procedure-that-has-more-than-one-version-defined"></a><span data-ttu-id="e5ec6-105">Pour appeler une procédure qui possède plusieurs versions définies</span><span class="sxs-lookup"><span data-stu-id="e5ec6-105">To call a procedure that has more than one version defined</span></span>  
  
1.  <span data-ttu-id="e5ec6-106">Dans le code appelant, déterminez les données à transmettre à la procédure.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-106">In the calling code, determine which data to pass to the procedure.</span></span>  
  
2.  <span data-ttu-id="e5ec6-107">Écrire l’appel de procédure de façon normale, présenter les données dans la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-107">Write the procedure call in the normal way, presenting the data in the argument list.</span></span> <span data-ttu-id="e5ec6-108">N’oubliez pas les arguments correspondent à la liste des paramètres dans une des versions définies pour la procédure.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-108">Be sure the arguments match the parameter list in one of the versions defined for the procedure.</span></span>  
  
3.  <span data-ttu-id="e5ec6-109">Il est inutile déterminer la version de la procédure à appeler.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-109">You do not have to determine which version of the procedure to call.</span></span> <span data-ttu-id="e5ec6-110">Visual Basic passe le contrôle à la version correspondant à votre liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-110">Visual Basic passes control to the version matching your argument list.</span></span>  
  
     <span data-ttu-id="e5ec6-111">L’exemple suivant appelle la `post` procédure déclarée dans [Comment : Définir plusieurs Versions d’une procédure](./how-to-define-multiple-versions-of-a-procedure.md).</span><span class="sxs-lookup"><span data-stu-id="e5ec6-111">The following example calls the `post` procedure declared in [How to: Define Multiple Versions of a Procedure](./how-to-define-multiple-versions-of-a-procedure.md).</span></span> <span data-ttu-id="e5ec6-112">Il obtient l’identification de client, détermine s’il est un `String` ou un `Integer`, puis, dans les deux cas, appelle la même procédure.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-112">It obtains the customer identification, determines whether it is a `String` or an `Integer`, and then in either case calls the same procedure.</span></span>  
  
     [!code-vb[VbVbcnProcedures#56](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#56)]  
  
     [!code-vb[VbVbcnProcedures#57](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#57)]  
  
## <a name="see-also"></a><span data-ttu-id="e5ec6-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5ec6-113">See also</span></span>
- [<span data-ttu-id="e5ec6-114">Procédures</span><span class="sxs-lookup"><span data-stu-id="e5ec6-114">Procedures</span></span>](./index.md)
- [<span data-ttu-id="e5ec6-115">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="e5ec6-115">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="e5ec6-116">Surcharge de procédure</span><span class="sxs-lookup"><span data-stu-id="e5ec6-116">Procedure Overloading</span></span>](./procedure-overloading.md)
- [<span data-ttu-id="e5ec6-117">Procédures de dépannage</span><span class="sxs-lookup"><span data-stu-id="e5ec6-117">Troubleshooting Procedures</span></span>](./troubleshooting-procedures.md)
- [<span data-ttu-id="e5ec6-118">Guide pratique pour Définir plusieurs Versions d’une procédure</span><span class="sxs-lookup"><span data-stu-id="e5ec6-118">How to: Define Multiple Versions of a Procedure</span></span>](./how-to-define-multiple-versions-of-a-procedure.md)
- [<span data-ttu-id="e5ec6-119">Guide pratique pour Surcharger une procédure qui accepte des paramètres optionnels</span><span class="sxs-lookup"><span data-stu-id="e5ec6-119">How to: Overload a Procedure that Takes Optional Parameters</span></span>](./how-to-overload-a-procedure-that-takes-optional-parameters.md)
- [<span data-ttu-id="e5ec6-120">Guide pratique pour Surcharger une procédure qui accepte un nombre indéfini de paramètres</span><span class="sxs-lookup"><span data-stu-id="e5ec6-120">How to: Overload a Procedure that Takes an Indefinite Number of Parameters</span></span>](./how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters.md)
- [<span data-ttu-id="e5ec6-121">Considérations sur les surcharges de procédures</span><span class="sxs-lookup"><span data-stu-id="e5ec6-121">Considerations in Overloading Procedures</span></span>](./considerations-in-overloading-procedures.md)
- [<span data-ttu-id="e5ec6-122">Résolution de surcharge</span><span class="sxs-lookup"><span data-stu-id="e5ec6-122">Overload Resolution</span></span>](./overload-resolution.md)
- [<span data-ttu-id="e5ec6-123">Overloads</span><span class="sxs-lookup"><span data-stu-id="e5ec6-123">Overloads</span></span>](../../../../visual-basic/language-reference/modifiers/overloads.md)
