---
title: Activation du débogage JIT-attach
ms.date: 03/30/2017
helpviewer_keywords:
- JIT-attach debugging
- debugging [.NET Framework], JIT-attach debugging
ms.assetid: f91fc5f7-de5a-4f23-b6ac-f450e63c662e
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f1696f9054d44a5f80a1f67cc38e315a8627d295
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59078782"
---
# <a name="enabling-jit-attach-debugging"></a><span data-ttu-id="030cc-102">Activation du débogage JIT-attach</span><span class="sxs-lookup"><span data-stu-id="030cc-102">Enabling JIT-Attach Debugging</span></span>
<span data-ttu-id="030cc-103">Débogage JIT-attach est l’expression utilisée pour décrire l’attachement d’un débogueur à un processus quand vous rencontrez des erreurs. Le débogage JIT-attach peut aussi être déclenché par des méthodes ou des fonctions spécifiques.</span><span class="sxs-lookup"><span data-stu-id="030cc-103">JIT-attach debugging is the phrase used to describe attaching a debugger to a process when you encounter errors, or it can be triggered by specific methods or functions.</span></span>  
  
 <span data-ttu-id="030cc-104">Le débogage JIT-attach est utilisé dans les conditions d’erreur suivantes :</span><span class="sxs-lookup"><span data-stu-id="030cc-104">JIT-attach debugging is used under the following fault conditions:</span></span>  
  
-   <span data-ttu-id="030cc-105">Exceptions non gérées (dans le code natif et managé)</span><span class="sxs-lookup"><span data-stu-id="030cc-105">Unhandled exceptions (in both native and managed code).</span></span>  
  
-   <xref:System.Environment.FailFast%2A?displayProperty=nameWithType> <span data-ttu-id="030cc-106">méthode ou [RaiseFailFastException](https://go.microsoft.com/fwlink/?LinkId=182107) (fonction) (famille Windows 7).</span><span class="sxs-lookup"><span data-stu-id="030cc-106">method or [RaiseFailFastException](https://go.microsoft.com/fwlink/?LinkId=182107) function (Windows 7 family).</span></span>  
  
-   <span data-ttu-id="030cc-107">Erreurs irrécupérables du runtime</span><span class="sxs-lookup"><span data-stu-id="030cc-107">Runtime fatal errors.</span></span>  
  
 <span data-ttu-id="030cc-108">Le débogage JIT-attach est également déclenché par des appels aux fonctions et méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="030cc-108">JIT-attach debugging is also triggered by calls to the following methods and functions:</span></span>  
  
-   <xref:System.Diagnostics.Debugger.Launch%2A?displayProperty=nameWithType> <span data-ttu-id="030cc-109">.</span><span class="sxs-lookup"><span data-stu-id="030cc-109">method.</span></span>  
  
-   <xref:System.Diagnostics.Debugger.Break%2A?displayProperty=nameWithType> <span data-ttu-id="030cc-110">.</span><span class="sxs-lookup"><span data-stu-id="030cc-110">method.</span></span>  
  
-   <span data-ttu-id="030cc-111">Fonction [DebugBreak](https://go.microsoft.com/fwlink/?LinkId=182106) (Win32)</span><span class="sxs-lookup"><span data-stu-id="030cc-111">[DebugBreak](https://go.microsoft.com/fwlink/?LinkId=182106) function (Win32).</span></span>  
  
 <span data-ttu-id="030cc-112">Avant le [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], le .NET Framework fournissait des clés de Registre distinctes pour contrôler le comportement des débogueurs natifs et managés.</span><span class="sxs-lookup"><span data-stu-id="030cc-112">Before the [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], the .NET Framework provided separate registry keys to control the behavior of native and managed debuggers.</span></span> <span data-ttu-id="030cc-113">En commençant par le [!INCLUDE[net_v40_short](../../../includes/net-v40-short-md.md)], contrôle est consolidé sous une clé de Registre unique : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\Current Version\AeDebug.</span><span class="sxs-lookup"><span data-stu-id="030cc-113">Starting with the [!INCLUDE[net_v40_short](../../../includes/net-v40-short-md.md)], control is consolidated under a single registry key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\Current Version\AeDebug.</span></span> <span data-ttu-id="030cc-114">Les valeurs que vous pouvez définir pour cette clé déterminent si un débogueur est appelé et, dans l’affirmative, s’il est appelé avec une boîte de dialogue qui nécessite une interaction utilisateur.</span><span class="sxs-lookup"><span data-stu-id="030cc-114">The values you can set for that key determine whether a debugger is invoked, and, if so, whether it is invoked with a dialog box that requires user interaction.</span></span> <span data-ttu-id="030cc-115">Pour plus d’informations sur la définition de cette clé de Registre, consultez [configuration du débogage automatique](https://go.microsoft.com/fwlink/?LinkId=181767).</span><span class="sxs-lookup"><span data-stu-id="030cc-115">For information about setting this registry key, see [Configuring Automatic Debugging](https://go.microsoft.com/fwlink/?LinkId=181767).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="030cc-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="030cc-116">See also</span></span>

- [<span data-ttu-id="030cc-117">Débogage, traçage et profilage</span><span class="sxs-lookup"><span data-stu-id="030cc-117">Debugging, Tracing, and Profiling</span></span>](../../../docs/framework/debug-trace-profile/index.md)
- [<span data-ttu-id="030cc-118">Simplification du débogage d'une image</span><span class="sxs-lookup"><span data-stu-id="030cc-118">Making an Image Easier to Debug</span></span>](../../../docs/framework/debug-trace-profile/making-an-image-easier-to-debug.md)
