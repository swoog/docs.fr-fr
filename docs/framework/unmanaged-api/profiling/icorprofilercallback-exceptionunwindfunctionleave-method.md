---
title: ICorProfilerCallback::ExceptionUnwindFunctionLeave, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionUnwindFunctionLeave
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionUnwindFunctionLeave
helpviewer_keywords:
- ICorProfilerCallback::ExceptionUnwindFunctionLeave method [.NET Framework profiling]
- ExceptionUnwindFunctionLeave method [.NET Framework profiling]
ms.assetid: ebaad1d5-ee0a-4cb0-96bc-8ba5d371b747
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 305c8c7abf778ea68efe06f3bdb57af001ea1b9a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61597347"
---
# <a name="icorprofilercallbackexceptionunwindfunctionleave-method"></a><span data-ttu-id="601ec-102">ICorProfilerCallback::ExceptionUnwindFunctionLeave, méthode</span><span class="sxs-lookup"><span data-stu-id="601ec-102">ICorProfilerCallback::ExceptionUnwindFunctionLeave Method</span></span>
<span data-ttu-id="601ec-103">Notifie le profileur que la phase de déroulement de la gestion des exceptions a terminé le déroulement d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="601ec-103">Notifies the profiler that the unwind phase of exception handling has finished unwinding a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="601ec-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="601ec-104">Syntax</span></span>  
  
```  
HRESULT ExceptionUnwindFunctionLeave();  
```  
  
## <a name="remarks"></a><span data-ttu-id="601ec-105">Notes</span><span class="sxs-lookup"><span data-stu-id="601ec-105">Remarks</span></span>  
 <span data-ttu-id="601ec-106">Lorsque le `ExceptionUnwindFunctionLeave` est appelée, l’instance de fonction et ses données de pile sont supprimés de la pile.</span><span class="sxs-lookup"><span data-stu-id="601ec-106">When the `ExceptionUnwindFunctionLeave` method is called, the function instance and its stack data are removed from the stack.</span></span>  
  
 <span data-ttu-id="601ec-107">Le profileur ne doit pas bloquer pendant cet appel, car la pile ne peut pas être dans un état qui autorise le garbage collection, et par conséquent, le garbage collection préemptif ne peut pas être activé.</span><span class="sxs-lookup"><span data-stu-id="601ec-107">The profiler should not block during this call because the stack may not be in a state that allows garbage collection, and therefore preemptive garbage collection cannot be enabled.</span></span> <span data-ttu-id="601ec-108">Si le profileur bloque et un garbage collection est tentée, le runtime bloque jusqu'à ce que ce rappel renvoie.</span><span class="sxs-lookup"><span data-stu-id="601ec-108">If the profiler blocks here and a garbage collection is attempted, the runtime will block until this callback returns.</span></span>  
  
 <span data-ttu-id="601ec-109">En outre, pendant cet appel, le profileur doit appeler pas dans le code managé ou de quelque manière qu’une allocation de mémoire managée.</span><span class="sxs-lookup"><span data-stu-id="601ec-109">Also, during this call, the profiler must not call into managed code or in any way cause a managed-memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="601ec-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="601ec-110">Requirements</span></span>  
 <span data-ttu-id="601ec-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="601ec-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="601ec-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="601ec-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="601ec-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="601ec-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="601ec-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="601ec-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="601ec-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="601ec-115">See also</span></span>

- [<span data-ttu-id="601ec-116">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="601ec-116">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="601ec-117">ExceptionUnwindFunctionEnter, méthode</span><span class="sxs-lookup"><span data-stu-id="601ec-117">ExceptionUnwindFunctionEnter Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionunwindfunctionenter-method.md)
