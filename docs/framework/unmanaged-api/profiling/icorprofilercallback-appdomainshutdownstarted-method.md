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
ms.openlocfilehash: fd1e5daada8793e94980afc5f0cf509915bd288e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33450926"
---
# <a name="icorprofilercallbackappdomainshutdownstarted-method"></a><span data-ttu-id="950ec-102">ICorProfilerCallback::AppDomainShutdownStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="950ec-102">ICorProfilerCallback::AppDomainShutdownStarted Method</span></span>
<span data-ttu-id="950ec-103">Notifie le profileur qu’un domaine d’application est en cours de déchargement d’un processus.</span><span class="sxs-lookup"><span data-stu-id="950ec-103">Notifies the profiler that an application domain is being unloaded from a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="950ec-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="950ec-104">Syntax</span></span>  
  
```  
HRESULT AppDomainShutdownStarted(  
    [in] AppDomainID appDomainId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="950ec-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="950ec-105">Parameters</span></span>  
 `appDomainId`  
 <span data-ttu-id="950ec-106">[in] Identifie le domaine dans lequel sont stockés les assemblys de l’application.</span><span class="sxs-lookup"><span data-stu-id="950ec-106">[in] Identifies the domain in which the application's assemblies are stored.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="950ec-107">Notes</span><span class="sxs-lookup"><span data-stu-id="950ec-107">Remarks</span></span>  
 <span data-ttu-id="950ec-108">La valeur de `appDomainId` n’est pas valide pour toute demande d’informations après le `AppDomainShutdownStarted` retours de méthode, il s’agit permet du profileur d’obtenir des informations sur ce domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="950ec-108">The value of `appDomainId` is not valid for any information request after the `AppDomainShutdownStarted` method returns — this is the profiler's last chance to get information about this application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="950ec-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="950ec-109">Requirements</span></span>  
 <span data-ttu-id="950ec-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="950ec-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="950ec-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="950ec-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="950ec-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="950ec-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="950ec-113">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="950ec-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="950ec-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="950ec-114">See Also</span></span>  
 [<span data-ttu-id="950ec-115">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="950ec-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
