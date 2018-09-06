---
title: Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne
ms.date: 07/20/2015
f1_keywords:
- vbrDiagnosticInfo_FullOSName
ms.assetid: f69da02b-eb9a-4284-bb9e-3025517ae6c1
ms.openlocfilehash: 192033348a779591a54860505d5d707a802c415a
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43778241"
---
# <a name="could-not-obtain-full-operation-system-name-due-to-internal-error"></a><span data-ttu-id="4c0f6-102">Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne</span><span class="sxs-lookup"><span data-stu-id="4c0f6-102">Could not obtain full operation system name due to internal error</span></span>
<span data-ttu-id="4c0f6-103">Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne.</span><span class="sxs-lookup"><span data-stu-id="4c0f6-103">Could not obtain full operation system name due to internal error.</span></span> <span data-ttu-id="4c0f6-104">Ceci peut être dû au fait que WMI est absent de l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="4c0f6-104">This might be caused by WMI not existing on the current machine.</span></span>  
  
 <span data-ttu-id="4c0f6-105">Un appel à la propriété `My.Computer.Info.OSFullName` a échoué.</span><span class="sxs-lookup"><span data-stu-id="4c0f6-105">A call to the `My.Computer.Info.OSFullName` property failed.</span></span> <span data-ttu-id="4c0f6-106">WMI (Windows Management Instrumentation) n’est peut-être pas installé sur l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="4c0f6-106">A possible cause for this failure is if Windows Management Instrumentation (WMI) is not installed on the current computer.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="4c0f6-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="4c0f6-107">To correct this error</span></span>  
  
1.  <span data-ttu-id="4c0f6-108">Ajoutez un bloc `Try...Catch` autour de l’appel à la propriété `My.Computer.Info.OSFullName` .</span><span class="sxs-lookup"><span data-stu-id="4c0f6-108">Add a `Try...Catch` block around the call to the `My.Computer.Info.OSFullName` property.</span></span>  
  
2.  <span data-ttu-id="4c0f6-109">Pour plus d’informations sur WMI et comment l’installer, accédez à et recherchez « Windows Management Instrumentation Core ».</span><span class="sxs-lookup"><span data-stu-id="4c0f6-109">For more information about WMI and how to install it, go to  and search for "Windows Management Instrumentation Core".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c0f6-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c0f6-110">See Also</span></span>  
 [<span data-ttu-id="4c0f6-111">My.Computer.Info.OSFullName</span><span class="sxs-lookup"><span data-stu-id="4c0f6-111">My.Computer.Info.OSFullName</span></span>](xref:Microsoft.VisualBasic.Devices.ComputerInfo.OSFullName)  
 [<span data-ttu-id="4c0f6-112">Exceptions et gestion des erreurs dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4c0f6-112">Exception and Error Handling in Visual Basic</span></span>](https://msdn.microsoft.com/library/3e351e73-cf23-40ab-8b60-05794160529e)  
 [<span data-ttu-id="4c0f6-113">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="4c0f6-113">Try...Catch...Finally Statement</span></span>](../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
