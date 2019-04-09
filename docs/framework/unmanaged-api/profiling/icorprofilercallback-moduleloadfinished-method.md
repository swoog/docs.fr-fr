---
title: ICorProfilerCallback::ModuleLoadFinished, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleLoadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleLoadFinished
helpviewer_keywords:
- ModuleLoadFinished method [.NET Framework profiling]
- ICorProfilerCallback::ModuleLoadFinished method [.NET Framework profiling]
ms.assetid: 050649e5-ffc0-4458-a0a4-d9ee128a219e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 354d2f278bcb0618b823b7300079278fc4c3315c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59157343"
---
# <a name="icorprofilercallbackmoduleloadfinished-method"></a><span data-ttu-id="681b7-102">ICorProfilerCallback::ModuleLoadFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="681b7-102">ICorProfilerCallback::ModuleLoadFinished Method</span></span>
<span data-ttu-id="681b7-103">Notifie le profileur qu’un module a été chargé.</span><span class="sxs-lookup"><span data-stu-id="681b7-103">Notifies the profiler that a module has finished loading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="681b7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="681b7-104">Syntax</span></span>  
  
```  
HRESULT ModuleLoadFinished(  
    [in] ModuleID moduleId,  
    [in] HRESULT  hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="681b7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="681b7-105">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="681b7-106">[in] L’ID du module qui le chargement est terminé.</span><span class="sxs-lookup"><span data-stu-id="681b7-106">[in] The ID of the module that has finished loading.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="681b7-107">[in] HRESULT qui indique si le module a été chargé avec succès.</span><span class="sxs-lookup"><span data-stu-id="681b7-107">[in] An HRESULT that indicates whether the module was loaded successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="681b7-108">Notes</span><span class="sxs-lookup"><span data-stu-id="681b7-108">Remarks</span></span>  
 <span data-ttu-id="681b7-109">La valeur de `moduleId` n’est pas valide pour une demande d’informations jusqu'à ce que le `ModuleLoadFinished` méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="681b7-109">The value of `moduleId` is not valid for an information request until the `ModuleLoadFinished` method is called.</span></span>  
  
 <span data-ttu-id="681b7-110">Certaines parties du chargement du module peuvent continuer après le `ModuleLoadFinished` rappel.</span><span class="sxs-lookup"><span data-stu-id="681b7-110">Some parts of loading the module might continue after the `ModuleLoadFinished` callback.</span></span> <span data-ttu-id="681b7-111">Un HRESULT d’échec dans `hrStatus` indique un échec.</span><span class="sxs-lookup"><span data-stu-id="681b7-111">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="681b7-112">Toutefois, un HRESULT de réussite dans `hrStatus` indique uniquement que la première partie du chargement du module a réussi.</span><span class="sxs-lookup"><span data-stu-id="681b7-112">However, a success HRESULT in `hrStatus` indicates only that the first part of loading the module has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="681b7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="681b7-113">Requirements</span></span>  
 <span data-ttu-id="681b7-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="681b7-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="681b7-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="681b7-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="681b7-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="681b7-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="681b7-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="681b7-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="681b7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="681b7-118">See also</span></span>

- [<span data-ttu-id="681b7-119">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="681b7-119">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="681b7-120">ModuleLoadStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="681b7-120">ModuleLoadStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadstarted-method.md)
