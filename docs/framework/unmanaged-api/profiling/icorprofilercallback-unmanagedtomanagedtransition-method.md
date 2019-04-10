---
title: ICorProfilerCallback::UnmanagedToManagedTransition, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.UnmanagedToManagedTransition
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::UnmanagedToManagedTransition
helpviewer_keywords:
- ICorProfilerCallback::UnmanagedToManagedTransition method [.NET Framework profiling]
- UnmanagedToManagedTransition method [.NET Framework profiling]
ms.assetid: ade2cc01-9b81-4e09-a5f9-b3b9dda27e96
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 312f133c263becfd815f1b4ad48dff4892963aaf
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59227845"
---
# <a name="icorprofilercallbackunmanagedtomanagedtransition-method"></a><span data-ttu-id="86027-102">ICorProfilerCallback::UnmanagedToManagedTransition, méthode</span><span class="sxs-lookup"><span data-stu-id="86027-102">ICorProfilerCallback::UnmanagedToManagedTransition Method</span></span>
<span data-ttu-id="86027-103">Notifie le profileur qu’une transition du code non managé au code managé s’est produite.</span><span class="sxs-lookup"><span data-stu-id="86027-103">Notifies the profiler that a transition from unmanaged code to managed code has occurred.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86027-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86027-104">Syntax</span></span>  
  
```  
HRESULT UnmanagedToManagedTransition(  
    [in] FunctionID functionId,  
    [in] COR_PRF_TRANSITION_REASON reason);  
```  
  
## <a name="parameters"></a><span data-ttu-id="86027-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86027-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="86027-106">[in] L’ID de la fonction est appelée.</span><span class="sxs-lookup"><span data-stu-id="86027-106">[in] The ID of the function that is being called.</span></span>  
  
 `reason`  
 <span data-ttu-id="86027-107">[in] Une valeur de la [COR_PRF_TRANSITION_REASON](../../../../docs/framework/unmanaged-api/profiling/cor-prf-transition-reason-enumeration.md) énumération qui indique si la transition s’est produite en raison d’un appel dans le code managé à partir de code non managé, ou en raison d’un retour à partir d’une fonction non managée appelée par un objet managé.</span><span class="sxs-lookup"><span data-stu-id="86027-107">[in] A value of the [COR_PRF_TRANSITION_REASON](../../../../docs/framework/unmanaged-api/profiling/cor-prf-transition-reason-enumeration.md) enumeration that indicates whether the transition occurred because of a call into managed code from unmanaged code, or because of a return from an unmanaged function called by a managed one.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="86027-108">Notes</span><span class="sxs-lookup"><span data-stu-id="86027-108">Remarks</span></span>  
 <span data-ttu-id="86027-109">Si la valeur de `reason` est COR_PRF_TRANSITION_RETURN et `functionId` n’est ne pas null, la fonction ID est celle de la fonction non managée et n’a jamais été compilé à l’aide du compilateur juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="86027-109">If the value of `reason` is COR_PRF_TRANSITION_RETURN and `functionId` is not null, the function ID is that of the unmanaged function, and will never have been compiled using the just-in-time (JIT) compiler.</span></span> <span data-ttu-id="86027-110">Fonctions non managées ont des informations de base qui s’y rapportent, comme un nom et des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="86027-110">Unmanaged functions have some basic information associated with them, such as a name and some metadata.</span></span>  
  
 <span data-ttu-id="86027-111">Si la valeur de `reason` est COR_PRF_TRANSITION_CALL, il est possible que la fonction appelée (autrement dit, la fonction managée) n’a pas encore été compilé par JIT.</span><span class="sxs-lookup"><span data-stu-id="86027-111">If the value of `reason` is COR_PRF_TRANSITION_CALL, it may be possible that the called function (that is, the managed function) has not yet been JIT-compiled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86027-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86027-112">Requirements</span></span>  
 <span data-ttu-id="86027-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="86027-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86027-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="86027-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="86027-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="86027-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="86027-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="86027-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="86027-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86027-117">See also</span></span>

- [<span data-ttu-id="86027-118">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="86027-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="86027-119">ManagedToUnmanagedTransition, méthode</span><span class="sxs-lookup"><span data-stu-id="86027-119">ManagedToUnmanagedTransition Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-managedtounmanagedtransition-method.md)
- [<span data-ttu-id="86027-120">Utilisation d'un PInvoke explicite en C++ (attribut DllImport)</span><span class="sxs-lookup"><span data-stu-id="86027-120">Using Explicit PInvoke in C++ (DllImport Attribute)</span></span>](/cpp/dotnet/using-explicit-pinvoke-in-cpp-dllimport-attribute)
- [<span data-ttu-id="86027-121">Utilisation de l'interopérabilité C++ (PInvoke implicite)</span><span class="sxs-lookup"><span data-stu-id="86027-121">Using C++ Interop (Implicit PInvoke)</span></span>](/cpp/dotnet/using-cpp-interop-implicit-pinvoke)
