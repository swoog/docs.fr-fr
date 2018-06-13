---
title: Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne
ms.date: 07/20/2015
f1_keywords:
- vbrDiagnosticInfo_FullOSName
ms.assetid: f69da02b-eb9a-4284-bb9e-3025517ae6c1
ms.openlocfilehash: f85ca5f7f325cb0dd2b8fc55d3f90f6abdfd4a7c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33635075"
---
# <a name="could-not-obtain-full-operation-system-name-due-to-internal-error"></a><span data-ttu-id="44b32-102">Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne</span><span class="sxs-lookup"><span data-stu-id="44b32-102">Could not obtain full operation system name due to internal error</span></span>
<span data-ttu-id="44b32-103">Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne.</span><span class="sxs-lookup"><span data-stu-id="44b32-103">Could not obtain full operation system name due to internal error.</span></span> <span data-ttu-id="44b32-104">Ceci peut être dû au fait que WMI est absent de l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="44b32-104">This might be caused by WMI not existing on the current machine.</span></span>  
  
 <span data-ttu-id="44b32-105">Un appel à la propriété `My.Computer.Info.OSFullName` a échoué.</span><span class="sxs-lookup"><span data-stu-id="44b32-105">A call to the `My.Computer.Info.OSFullName` property failed.</span></span> <span data-ttu-id="44b32-106">WMI (Windows Management Instrumentation) n’est peut-être pas installé sur l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="44b32-106">A possible cause for this failure is if Windows Management Instrumentation (WMI) is not installed on the current computer.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="44b32-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="44b32-107">To correct this error</span></span>  
  
1.  <span data-ttu-id="44b32-108">Ajoutez un bloc `Try...Catch` autour de l’appel à la propriété `My.Computer.Info.OSFullName` .</span><span class="sxs-lookup"><span data-stu-id="44b32-108">Add a `Try...Catch` block around the call to the `My.Computer.Info.OSFullName` property.</span></span>  
  
2.  <span data-ttu-id="44b32-109">Pour plus d’informations sur WMI et comment l’installer, accédez à et recherchez « Windows Management Instrumentation Core ».</span><span class="sxs-lookup"><span data-stu-id="44b32-109">For more information about WMI and how to install it, go to  and search for "Windows Management Instrumentation Core".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44b32-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44b32-110">See Also</span></span>  
 [<span data-ttu-id="44b32-111">My.Computer.Info.OSFullName</span><span class="sxs-lookup"><span data-stu-id="44b32-111">My.Computer.Info.OSFullName</span></span>](xref:Microsoft.VisualBasic.Devices.ComputerInfo.OSFullName)  
 [<span data-ttu-id="44b32-112">Exceptions et gestion des erreurs dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="44b32-112">Exception and Error Handling in Visual Basic</span></span>](http://msdn.microsoft.com/library/3e351e73-cf23-40ab-8b60-05794160529e)  
 [<span data-ttu-id="44b32-113">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="44b32-113">Try...Catch...Finally Statement</span></span>](../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
