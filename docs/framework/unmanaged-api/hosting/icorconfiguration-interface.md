---
title: ICorConfiguration, interface
ms.date: 03/30/2017
api_name:
- ICorConfiguration
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorConfiguration
helpviewer_keywords:
- ICorConfiguration interface [.NET Framework hosting]
ms.assetid: aaf96116-372b-4538-afb1-9e0fcdac1f98
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 63699f0af69b3a7623c5e9da156c2ff8ae83ccfc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437511"
---
# <a name="icorconfiguration-interface"></a><span data-ttu-id="476f9-102">ICorConfiguration, interface</span><span class="sxs-lookup"><span data-stu-id="476f9-102">ICorConfiguration Interface</span></span>
<span data-ttu-id="476f9-103">Fournit des méthodes pour configurer le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="476f9-103">Provides methods for configuring the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="476f9-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="476f9-104">Methods</span></span>  
  
|<span data-ttu-id="476f9-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="476f9-105">Method</span></span>|<span data-ttu-id="476f9-106">Description</span><span class="sxs-lookup"><span data-stu-id="476f9-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="476f9-107">AddDebuggerSpecialThread, méthode</span><span class="sxs-lookup"><span data-stu-id="476f9-107">AddDebuggerSpecialThread Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-adddebuggerspecialthread-method.md)|<span data-ttu-id="476f9-108">Indique aux services de débogage qu’un thread particulier doit être autorisé à continuer de s’exécuter pendant que le débogueur arrête les scénarios de débogage managés ou une application.</span><span class="sxs-lookup"><span data-stu-id="476f9-108">Indicates to the debugging services that a particular thread should be allowed to continue executing while the debugger has an application stopped during managed or unmanaged debugging scenarios.</span></span>|  
|[<span data-ttu-id="476f9-109">SetDebuggerThreadControl, méthode</span><span class="sxs-lookup"><span data-stu-id="476f9-109">SetDebuggerThreadControl Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-setdebuggerthreadcontrol-method.md)|<span data-ttu-id="476f9-110">Définit l’interface de rappel qui appellent les services de débogage comme threads CLR sont bloqués et débloqués pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="476f9-110">Sets the callback interface that the debugging services will call as CLR threads are blocked and unblocked for debugging.</span></span>|  
|[<span data-ttu-id="476f9-111">SetGCHostControl, méthode</span><span class="sxs-lookup"><span data-stu-id="476f9-111">SetGCHostControl Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-setgchostcontrol-method.md)|<span data-ttu-id="476f9-112">Définit l’interface de rappel à utiliser par le garbage collector de demander à l’hôte de modifier les limites de mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="476f9-112">Sets the callback interface to be used by the garbage collector to request the host to change the limits of virtual memory.</span></span>|  
|[<span data-ttu-id="476f9-113">SetGCThreadControl, méthode</span><span class="sxs-lookup"><span data-stu-id="476f9-113">SetGCThreadControl Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-setgcthreadcontrol-method.md)|<span data-ttu-id="476f9-114">Définit l’interface de rappel pour la planification des threads pour les tâches non-runtime qui seraient sinon bloqués pour un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="476f9-114">Sets the callback interface for scheduling threads for non-runtime tasks that would otherwise be blocked for a garbage collection.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="476f9-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="476f9-115">Requirements</span></span>  
 <span data-ttu-id="476f9-116">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="476f9-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="476f9-117">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="476f9-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="476f9-118">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="476f9-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="476f9-119">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="476f9-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="476f9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="476f9-120">See Also</span></span>  
 [<span data-ttu-id="476f9-121">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="476f9-121">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="476f9-122">CorRuntimeHost, coclasse</span><span class="sxs-lookup"><span data-stu-id="476f9-122">CorRuntimeHost Coclass</span></span>](../../../../docs/framework/unmanaged-api/hosting/corruntimehost-coclass.md)
