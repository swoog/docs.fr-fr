---
title: ICorProfilerCallback::AppDomainShutdownStarted, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AppDomainShutdownStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AppDomainShutdownStarted
helpviewer_keywords:
- AppDomainShutdownStarted method [.NET Framework profiling]
- ICorProfilerCallback::AppDomainShutdownStarted method [.NET Framework profiling]
ms.assetid: d23a3408-b525-4aec-a186-2ac7ca65d7a4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f422e99a5f6a4153368304ff0b33bbc55381575a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59177110"
---
# <a name="icorprofilercallbackappdomainshutdownstarted-method"></a><span data-ttu-id="dc583-102">ICorProfilerCallback::AppDomainShutdownStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="dc583-102">ICorProfilerCallback::AppDomainShutdownStarted Method</span></span>
<span data-ttu-id="dc583-103">Notifie le profileur qu’un domaine d’application est en cours de déchargement d’un processus.</span><span class="sxs-lookup"><span data-stu-id="dc583-103">Notifies the profiler that an application domain is being unloaded from a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc583-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc583-104">Syntax</span></span>  
  
```  
HRESULT AppDomainShutdownStarted(  
    [in] AppDomainID appDomainId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dc583-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc583-105">Parameters</span></span>  
 `appDomainId`  
 <span data-ttu-id="dc583-106">[in] Identifie le domaine dans lequel sont stockés les assemblys de l’application.</span><span class="sxs-lookup"><span data-stu-id="dc583-106">[in] Identifies the domain in which the application's assemblies are stored.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dc583-107">Notes</span><span class="sxs-lookup"><span data-stu-id="dc583-107">Remarks</span></span>  
 <span data-ttu-id="dc583-108">La valeur de `appDomainId` n’est pas valide pour toute demande d’informations après la `AppDomainShutdownStarted` retourne de la méthode, il s’agit dernière chance du profileur d’obtenir des informations sur ce domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="dc583-108">The value of `appDomainId` is not valid for any information request after the `AppDomainShutdownStarted` method returns — this is the profiler's last chance to get information about this application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dc583-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc583-109">Requirements</span></span>  
 <span data-ttu-id="dc583-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dc583-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dc583-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="dc583-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="dc583-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dc583-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="dc583-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="dc583-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="dc583-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc583-114">See also</span></span>

- [<span data-ttu-id="dc583-115">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="dc583-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
