---
title: Assistant Débogage managé raceOnRCWCleanup
ms.date: 03/30/2017
helpviewer_keywords:
- RCW
- managed debugging assistants (MDAs), RCWs
- race on RCW cleanup
- MDAs (managed debugging assistants), RCWs
- RaceOnRCWCleanup MDA
- runtime callable wrappers
ms.assetid: bee1e9b1-50a8-4c89-9cd9-7dd6b2458187
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 628790bb8229dc519589c122235f07a38ba57c1c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59100234"
---
# <a name="raceonrcwcleanup-mda"></a><span data-ttu-id="6af2d-102">Assistant Débogage managé raceOnRCWCleanup</span><span class="sxs-lookup"><span data-stu-id="6af2d-102">raceOnRCWCleanup MDA</span></span>
<span data-ttu-id="6af2d-103">L’Assistant Débogage managé (MDA) `raceOnRCWCleanup` est activé quand le Common Language Runtime (CLR) détecte qu’un [wrapper RCW](../../../docs/framework/interop/runtime-callable-wrapper.md) est en cours d’utilisation au moment où un appel visant à le libérer est effectué à l’aide d’une commande telle que la méthode <xref:System.Runtime.InteropServices.Marshal.ReleaseComObject%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="6af2d-103">The `raceOnRCWCleanup` managed debugging assistant (MDA) is activated when the common language runtime (CLR) detects that a [Runtime Callable Wrapper](../../../docs/framework/interop/runtime-callable-wrapper.md) (RCW) is in use when a call to release it is made using a command such as the <xref:System.Runtime.InteropServices.Marshal.ReleaseComObject%2A?displayProperty=nameWithType> method.</span></span>  
  
## <a name="symptoms"></a><span data-ttu-id="6af2d-104">Symptômes</span><span class="sxs-lookup"><span data-stu-id="6af2d-104">Symptoms</span></span>  
 <span data-ttu-id="6af2d-105">Violations d'accès ou altération de la mémoire pendant ou après la libération d'un RCW à l'aide de <xref:System.Runtime.InteropServices.Marshal.ReleaseComObject%2A> ou d'une méthode similaire.</span><span class="sxs-lookup"><span data-stu-id="6af2d-105">Access violations or memory corruption during or after freeing an RCW using <xref:System.Runtime.InteropServices.Marshal.ReleaseComObject%2A> or a similar method.</span></span>  
  
## <a name="cause"></a><span data-ttu-id="6af2d-106">Cause</span><span class="sxs-lookup"><span data-stu-id="6af2d-106">Cause</span></span>  
 <span data-ttu-id="6af2d-107">Le RCW est en cours d'utilisation sur un autre thread ou sur la pile des threads de libération,</span><span class="sxs-lookup"><span data-stu-id="6af2d-107">The RCW is in use on another thread or on the freeing thread stack.</span></span>  <span data-ttu-id="6af2d-108">et ne peut donc pas être libéré.</span><span class="sxs-lookup"><span data-stu-id="6af2d-108">An RCW that is in use cannot be released.</span></span>  
  
## <a name="resolution"></a><span data-ttu-id="6af2d-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="6af2d-109">Resolution</span></span>  
 <span data-ttu-id="6af2d-110">Ne libérez pas un RCW qui pourrait être utilisé dans le thread actuel ou dans d'autres threads.</span><span class="sxs-lookup"><span data-stu-id="6af2d-110">Do not free an RCW that could be in use either in the current or in other threads.</span></span>  
  
## <a name="effect-on-the-runtime"></a><span data-ttu-id="6af2d-111">Effet sur le runtime</span><span class="sxs-lookup"><span data-stu-id="6af2d-111">Effect on the Runtime</span></span>  
 <span data-ttu-id="6af2d-112">Cet Assistant Débogage managé n'a aucun effet sur le CLR.</span><span class="sxs-lookup"><span data-stu-id="6af2d-112">This MDA has no effect on the CLR.</span></span>  
  
## <a name="output"></a><span data-ttu-id="6af2d-113">Sortie</span><span class="sxs-lookup"><span data-stu-id="6af2d-113">Output</span></span>  
 <span data-ttu-id="6af2d-114">Message décrivant l'erreur.</span><span class="sxs-lookup"><span data-stu-id="6af2d-114">A message describing the error.</span></span>  
  
## <a name="configuration"></a><span data-ttu-id="6af2d-115">Configuration</span><span class="sxs-lookup"><span data-stu-id="6af2d-115">Configuration</span></span>  
  
```xml  
<mdaConfig>  
  <assistants>  
    <raceOnRCWCleanup/>  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6af2d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6af2d-116">See also</span></span>

- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [<span data-ttu-id="6af2d-117">Diagnostic d'erreurs avec les Assistants de débogage managés</span><span class="sxs-lookup"><span data-stu-id="6af2d-117">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [<span data-ttu-id="6af2d-118">Marshaling d’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="6af2d-118">Interop Marshaling</span></span>](../../../docs/framework/interop/interop-marshaling.md)
