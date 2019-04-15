---
ms.openlocfilehash: 3cd5052dffcb059c240a310e0b89384f28409264
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234466"
---
### <a name="calls-to-systemwindowsinputpencontextdisable-on-touch-enabled-systems-may-throw-an-argumentexception"></a><span data-ttu-id="5c1be-101">Les appels à System.Windows.Input.PenContext.Disable sur des systèmes tactiles peuvent lever une exception ArgumentException</span><span class="sxs-lookup"><span data-stu-id="5c1be-101">Calls to System.Windows.Input.PenContext.Disable on touch-enabled systems may throw an ArgumentException</span></span>

|   |   |
|---|---|
|<span data-ttu-id="5c1be-102">Détails</span><span class="sxs-lookup"><span data-stu-id="5c1be-102">Details</span></span>|<span data-ttu-id="5c1be-103">Dans certaines circonstances, les appels à la méthode <strong>System.Windows.Intput.PenContext.Disable</strong> interne sur des systèmes tactiles peuvent lever une exception <code>T:System.ArgumentException</code> non gérée en raison de la réentrance.</span><span class="sxs-lookup"><span data-stu-id="5c1be-103">Under some circumstances, calls to the internal <strong>System.Windows.Intput.PenContext.Disable</strong> method on touch-enabled systems may throw an unhandled <code>T:System.ArgumentException</code> because of reentrancy.</span></span>|
|<span data-ttu-id="5c1be-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="5c1be-104">Suggestion</span></span>|<span data-ttu-id="5c1be-105">Ce problème a été résolu dans le .NET Framework 4.7.</span><span class="sxs-lookup"><span data-stu-id="5c1be-105">This issue has been addressed in the .NET Framework 4.7.</span></span> <span data-ttu-id="5c1be-106">Pour éviter cette exception, effectuez une mise à niveau avec une version du .NET Framework supérieure ou égale à 4.7.</span><span class="sxs-lookup"><span data-stu-id="5c1be-106">To prevent the exception, upgrade to a version of the .NET Framework starting with the .NET Framework 4.7.</span></span>|
|<span data-ttu-id="5c1be-107">Portée</span><span class="sxs-lookup"><span data-stu-id="5c1be-107">Scope</span></span>|<span data-ttu-id="5c1be-108">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5c1be-108">Edge</span></span>|
|<span data-ttu-id="5c1be-109">Version</span><span class="sxs-lookup"><span data-stu-id="5c1be-109">Version</span></span>|<span data-ttu-id="5c1be-110">4.6.1</span><span class="sxs-lookup"><span data-stu-id="5c1be-110">4.6.1</span></span>|
|<span data-ttu-id="5c1be-111">Type</span><span class="sxs-lookup"><span data-stu-id="5c1be-111">Type</span></span>|<span data-ttu-id="5c1be-112">Reciblage</span><span class="sxs-lookup"><span data-stu-id="5c1be-112">Retargeting</span></span>|
