---
title: 'Comment : appeler une procédure surchargée (Visual Basic)'
ms.custom: ''
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], overloading
- procedures [Visual Basic], calling
- procedures [Visual Basic], multiple versions
- procedure calls [Visual Basic], overloaded
ms.assetid: 3bb331fb-f6bc-406f-9ca0-9609b497014c
caps.latest.revision: 12
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 5eca03de6b6dd2ca2b992196b1ae224f8fbf5068
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-call-an-overloaded-procedure-visual-basic"></a><span data-ttu-id="76505-102">Comment : appeler une procédure surchargée (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="76505-102">How to: Call an Overloaded Procedure (Visual Basic)</span></span>
<span data-ttu-id="76505-103">L’avantage de la surcharge d’une procédure est la flexibilité de l’appel.</span><span class="sxs-lookup"><span data-stu-id="76505-103">The advantage of overloading a procedure is in the flexibility of the call.</span></span> <span data-ttu-id="76505-104">Le code appelant peut obtenir les informations que nécessaires pour passer à la procédure, puis appelez un seul nom de procédure, quel que soit les arguments, il passe.</span><span class="sxs-lookup"><span data-stu-id="76505-104">The calling code can obtain the information it needs to pass to the procedure and then call a single procedure name, no matter what arguments it is passing.</span></span>  
  
### <a name="to-call-a-procedure-that-has-more-than-one-version-defined"></a><span data-ttu-id="76505-105">Pour appeler une procédure qui possède plusieurs versions définies</span><span class="sxs-lookup"><span data-stu-id="76505-105">To call a procedure that has more than one version defined</span></span>  
  
1.  <span data-ttu-id="76505-106">Dans le code appelant, déterminez les données à passer à la procédure.</span><span class="sxs-lookup"><span data-stu-id="76505-106">In the calling code, determine which data to pass to the procedure.</span></span>  
  
2.  <span data-ttu-id="76505-107">Écrire l’appel de procédure de façon normale, présenter les données dans la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="76505-107">Write the procedure call in the normal way, presenting the data in the argument list.</span></span> <span data-ttu-id="76505-108">Assurez-vous que les arguments correspondent à la liste des paramètres de l’une des versions définies pour la procédure.</span><span class="sxs-lookup"><span data-stu-id="76505-108">Be sure the arguments match the parameter list in one of the versions defined for the procedure.</span></span>  
  
3.  <span data-ttu-id="76505-109">Il est inutile de déterminer la version de la procédure à appeler.</span><span class="sxs-lookup"><span data-stu-id="76505-109">You do not have to determine which version of the procedure to call.</span></span> <span data-ttu-id="76505-110">Visual Basic passe le contrôle à la version correspondant à votre liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="76505-110">Visual Basic passes control to the version matching your argument list.</span></span>  
  
     <span data-ttu-id="76505-111">L’exemple suivant appelle la `post` procédure déclarée dans [Comment : définir plusieurs Versions d’une procédure](./how-to-define-multiple-versions-of-a-procedure.md).</span><span class="sxs-lookup"><span data-stu-id="76505-111">The following example calls the `post` procedure declared in [How to: Define Multiple Versions of a Procedure](./how-to-define-multiple-versions-of-a-procedure.md).</span></span> <span data-ttu-id="76505-112">Il obtient l’identification de client, détermine s’il est un `String` ou `Integer`, puis, dans les deux cas, appelle la même procédure.</span><span class="sxs-lookup"><span data-stu-id="76505-112">It obtains the customer identification, determines whether it is a `String` or an `Integer`, and then in either case calls the same procedure.</span></span>  
  
     [!code-vb[VbVbcnProcedures#56](./codesnippet/VisualBasic/how-to-call-an-overloaded-procedure_1.vb)]  
  
     [!code-vb[VbVbcnProcedures#57](./codesnippet/VisualBasic/how-to-call-an-overloaded-procedure_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="76505-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76505-113">See Also</span></span>  
 [<span data-ttu-id="76505-114">Procédures</span><span class="sxs-lookup"><span data-stu-id="76505-114">Procedures</span></span>](./index.md)  
 [<span data-ttu-id="76505-115">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="76505-115">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)  
 [<span data-ttu-id="76505-116">Surcharge de procédure</span><span class="sxs-lookup"><span data-stu-id="76505-116">Procedure Overloading</span></span>](./procedure-overloading.md)  
 [<span data-ttu-id="76505-117">Procédures de dépannage</span><span class="sxs-lookup"><span data-stu-id="76505-117">Troubleshooting Procedures</span></span>](./troubleshooting-procedures.md)  
 [<span data-ttu-id="76505-118">Guide pratique : définir plusieurs versions d’une procédure</span><span class="sxs-lookup"><span data-stu-id="76505-118">How to: Define Multiple Versions of a Procedure</span></span>](./how-to-define-multiple-versions-of-a-procedure.md)  
 [<span data-ttu-id="76505-119">Guide pratique : surcharger une procédure qui accepte des paramètres optionnels</span><span class="sxs-lookup"><span data-stu-id="76505-119">How to: Overload a Procedure that Takes Optional Parameters</span></span>](./how-to-overload-a-procedure-that-takes-optional-parameters.md)  
 [<span data-ttu-id="76505-120">Guide pratique : surcharger une procédure qui accepte un nombre indéfini de paramètres</span><span class="sxs-lookup"><span data-stu-id="76505-120">How to: Overload a Procedure that Takes an Indefinite Number of Parameters</span></span>](./how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters.md)  
 [<span data-ttu-id="76505-121">Considérations sur les surcharges de procédures</span><span class="sxs-lookup"><span data-stu-id="76505-121">Considerations in Overloading Procedures</span></span>](./considerations-in-overloading-procedures.md)  
 [<span data-ttu-id="76505-122">Résolution de surcharge</span><span class="sxs-lookup"><span data-stu-id="76505-122">Overload Resolution</span></span>](./overload-resolution.md)  
 [<span data-ttu-id="76505-123">Overloads</span><span class="sxs-lookup"><span data-stu-id="76505-123">Overloads</span></span>](../../../../visual-basic/language-reference/modifiers/overloads.md)
