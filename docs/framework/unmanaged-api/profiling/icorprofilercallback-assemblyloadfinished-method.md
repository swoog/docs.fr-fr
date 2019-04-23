---
title: ICorProfilerCallback::AssemblyLoadFinished, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AssemblyLoadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AssemblyLoadFinished
helpviewer_keywords:
- ICorProfilerCallback::AssemblyLoadFinished method [.NET Framework profiling]
- AssemblyLoadFinished method [.NET Framework profiling]
ms.assetid: 86d98f39-52e6-4c61-a625-9760f695ff12
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e32af790c755f65b5435455c326d011656da19ed
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59198372"
---
# <a name="icorprofilercallbackassemblyloadfinished-method"></a><span data-ttu-id="457aa-102">ICorProfilerCallback::AssemblyLoadFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="457aa-102">ICorProfilerCallback::AssemblyLoadFinished Method</span></span>
<span data-ttu-id="457aa-103">Notifie le profileur qu’un assembly a été chargé.</span><span class="sxs-lookup"><span data-stu-id="457aa-103">Notifies the profiler that an assembly has finished loading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="457aa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="457aa-104">Syntax</span></span>  
  
```  
HRESULT AssemblyLoadFinished(  
    [in] AssemblyID assemblyId,  
    [in] HRESULT    hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="457aa-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="457aa-105">Parameters</span></span>  
 `assemblyId`  
 <span data-ttu-id="457aa-106">[in] Identifie l’assembly qui a été chargé.</span><span class="sxs-lookup"><span data-stu-id="457aa-106">[in] Identifies the assembly that was loaded.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="457aa-107">[in] HRESULT qui indique si l’assembly chargé avec succès.</span><span class="sxs-lookup"><span data-stu-id="457aa-107">[in] An HRESULT that indicates whether the assembly finished loading successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="457aa-108">Notes</span><span class="sxs-lookup"><span data-stu-id="457aa-108">Remarks</span></span>  
 <span data-ttu-id="457aa-109">La valeur de `assemblyId` n’est pas valide pour une demande d’informations jusqu'à ce que le `AssemblyLoadFinished` méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="457aa-109">The value of `assemblyId` is not valid for an information request until the `AssemblyLoadFinished` method is called.</span></span>  
  
 <span data-ttu-id="457aa-110">Certaines parties du chargement de l’assembly peuvent continuer après le `AssemblyLoadFinished` rappel.</span><span class="sxs-lookup"><span data-stu-id="457aa-110">Some parts of loading the assembly might continue after the `AssemblyLoadFinished` callback.</span></span> <span data-ttu-id="457aa-111">Un HRESULT d’échec dans `hrStatus` indique un échec.</span><span class="sxs-lookup"><span data-stu-id="457aa-111">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="457aa-112">Toutefois, un HRESULT de réussite dans `hrStatus` indique uniquement que la première partie du chargement de l’assembly a réussi.</span><span class="sxs-lookup"><span data-stu-id="457aa-112">However, a success HRESULT in `hrStatus` indicates only that the first part of loading the assembly has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="457aa-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="457aa-113">Requirements</span></span>  
 <span data-ttu-id="457aa-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="457aa-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="457aa-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="457aa-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="457aa-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="457aa-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="457aa-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="457aa-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="457aa-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="457aa-118">See also</span></span>

- [<span data-ttu-id="457aa-119">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="457aa-119">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
