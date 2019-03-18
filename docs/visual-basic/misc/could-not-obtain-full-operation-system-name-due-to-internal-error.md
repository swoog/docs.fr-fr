---
title: Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne
ms.date: 07/20/2015
f1_keywords:
- vbrDiagnosticInfo_FullOSName
ms.assetid: f69da02b-eb9a-4284-bb9e-3025517ae6c1
ms.openlocfilehash: 6a0e24743c861ba92fc284a84fa4ef26e2ee48a8
ms.sourcegitcommit: 5c1abeec15fbddcc7dbaa729fabc1f1f29f12045
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2019
ms.locfileid: "58022746"
---
# <a name="could-not-obtain-full-operation-system-name-due-to-internal-error"></a><span data-ttu-id="3e89c-102">Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne</span><span class="sxs-lookup"><span data-stu-id="3e89c-102">Could not obtain full operation system name due to internal error</span></span>
<span data-ttu-id="3e89c-103">Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne.</span><span class="sxs-lookup"><span data-stu-id="3e89c-103">Could not obtain full operation system name due to internal error.</span></span> <span data-ttu-id="3e89c-104">Ceci peut être dû au fait que WMI est absent de l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="3e89c-104">This might be caused by WMI not existing on the current machine.</span></span>  
  
 <span data-ttu-id="3e89c-105">Un appel à la propriété `My.Computer.Info.OSFullName` a échoué.</span><span class="sxs-lookup"><span data-stu-id="3e89c-105">A call to the `My.Computer.Info.OSFullName` property failed.</span></span> <span data-ttu-id="3e89c-106">WMI (Windows Management Instrumentation) n’est peut-être pas installé sur l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="3e89c-106">A possible cause for this failure is if Windows Management Instrumentation (WMI) is not installed on the current computer.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="3e89c-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="3e89c-107">To correct this error</span></span>  
  
1.  <span data-ttu-id="3e89c-108">Ajoutez un bloc `Try...Catch` autour de l’appel à la propriété `My.Computer.Info.OSFullName` .</span><span class="sxs-lookup"><span data-stu-id="3e89c-108">Add a `Try...Catch` block around the call to the `My.Computer.Info.OSFullName` property.</span></span>  
  
2.  <span data-ttu-id="3e89c-109">Pour plus d’informations sur WMI et comment l’installer, accédez à et recherchez « Windows Management Instrumentation Core ».</span><span class="sxs-lookup"><span data-stu-id="3e89c-109">For more information about WMI and how to install it, go to  and search for "Windows Management Instrumentation Core".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e89c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e89c-110">See also</span></span>

- [<span data-ttu-id="3e89c-111">My.Computer.Info.OSFullName</span><span class="sxs-lookup"><span data-stu-id="3e89c-111">My.Computer.Info.OSFullName</span></span>](xref:Microsoft.VisualBasic.Devices.ComputerInfo.OSFullName)
- [<span data-ttu-id="3e89c-112">Gestion et levée d’exceptions dans .NET</span><span class="sxs-lookup"><span data-stu-id="3e89c-112">Handling and throwing exceptions in .NET</span></span>](../../standard/exceptions/index.md)
- [<span data-ttu-id="3e89c-113">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="3e89c-113">Try...Catch...Finally Statement</span></span>](../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
