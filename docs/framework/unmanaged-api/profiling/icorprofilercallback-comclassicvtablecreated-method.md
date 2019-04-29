---
title: ICorProfilerCallback::COMClassicVTableCreated, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.COMClassicVTableCreated
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::COMClassicVTableCreated
helpviewer_keywords:
- COMClassicVTableCreated method [.NET Framework profiling]
- ICorProfilerCallback::COMClassicVTableCreated method [.NET Framework profiling]
ms.assetid: 6e1834ab-c359-498a-b10b-984ae23cdda4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4aa11b036c64ff6ffeec583c4cdd818d26067a74
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61598244"
---
# <a name="icorprofilercallbackcomclassicvtablecreated-method"></a><span data-ttu-id="59778-102">ICorProfilerCallback::COMClassicVTableCreated, méthode</span><span class="sxs-lookup"><span data-stu-id="59778-102">ICorProfilerCallback::COMClassicVTableCreated Method</span></span>
<span data-ttu-id="59778-103">Informe le profileur qu’une vtable d’interopérabilité COM pour l’IID et la classe spécifiée a été créée.</span><span class="sxs-lookup"><span data-stu-id="59778-103">Notifies the profiler that a COM interop vtable for the specified IID and class has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59778-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59778-104">Syntax</span></span>  
  
```  
HRESULT COMClassicVTableCreated(  
    [in] ClassID wrappedClassId,  
    [in] REFGUID implementedIID,  
    [in] void    *pVTable,  
    [in] ULONG   cSlots);  
```  
  
## <a name="parameters"></a><span data-ttu-id="59778-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59778-105">Parameters</span></span>  
 `wrappedClasId`  
 <span data-ttu-id="59778-106">[in] L’ID de la classe pour laquelle la vtable a été créée.</span><span class="sxs-lookup"><span data-stu-id="59778-106">[in] The ID of the class for which the vtable has been created.</span></span>  
  
 `implementedIID`  
 <span data-ttu-id="59778-107">[in] ID de l’interface implémentée par la classe.</span><span class="sxs-lookup"><span data-stu-id="59778-107">[in] The ID of the interface implemented by the class.</span></span> <span data-ttu-id="59778-108">Cette valeur peut être NULL si l’interface est uniquement interne.</span><span class="sxs-lookup"><span data-stu-id="59778-108">This value may be NULL if the interface is internal only.</span></span>  
  
 `pVTable`  
 <span data-ttu-id="59778-109">[in] Pointeur vers le début de la vtable.</span><span class="sxs-lookup"><span data-stu-id="59778-109">[in] A pointer to the start of the vtable.</span></span>  
  
 `cSlots`  
 <span data-ttu-id="59778-110">[in] Le nombre d’emplacements qui se trouvent dans la vtable.</span><span class="sxs-lookup"><span data-stu-id="59778-110">[in] The number of slots that are in the vtable.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="59778-111">Notes</span><span class="sxs-lookup"><span data-stu-id="59778-111">Remarks</span></span>  
 <span data-ttu-id="59778-112">Le profileur ne doit pas bloquer dans son implémentation de cette méthode, car la pile ne peut pas être dans un état qui autorise le garbage collection, et par conséquent, le garbage collection préemptif ne peut pas être activé.</span><span class="sxs-lookup"><span data-stu-id="59778-112">The profiler should not block in its implementation of this method because the stack may not be in a state that allows garbage collection, and therefore preemptive garbage collection cannot be enabled.</span></span> <span data-ttu-id="59778-113">Si le profileur bloque ici et le garbage collection est tenté, le runtime bloque jusqu'à ce que ce rappel renvoie.</span><span class="sxs-lookup"><span data-stu-id="59778-113">If the profiler blocks here and garbage collection is attempted, the runtime will block until this callback returns.</span></span>  
  
 <span data-ttu-id="59778-114">L’implémentation du profileur de cette méthode ne doit pas appeler dans du code managé ou de quelque manière qu’une allocation de mémoire managée.</span><span class="sxs-lookup"><span data-stu-id="59778-114">The profiler's implementation of this method should not call into managed code or in any way cause a managed-memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="59778-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59778-115">Requirements</span></span>  
 <span data-ttu-id="59778-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="59778-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="59778-117">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="59778-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="59778-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="59778-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="59778-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="59778-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59778-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59778-120">See also</span></span>

- [<span data-ttu-id="59778-121">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="59778-121">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="59778-122">COMClassicVTableDestroyed, méthode</span><span class="sxs-lookup"><span data-stu-id="59778-122">COMClassicVTableDestroyed Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-comclassicvtabledestroyed-method.md)
