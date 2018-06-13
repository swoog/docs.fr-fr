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
ms.openlocfilehash: a79a9c925392b0ab5e50269479b2f693f1a9b58d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33451238"
---
# <a name="icorprofilercallbackexceptionunwindfunctionleave-method"></a><span data-ttu-id="36eaf-102">ICorProfilerCallback::ExceptionUnwindFunctionLeave, méthode</span><span class="sxs-lookup"><span data-stu-id="36eaf-102">ICorProfilerCallback::ExceptionUnwindFunctionLeave Method</span></span>
<span data-ttu-id="36eaf-103">Notifie le profileur que la phase de déroulement de la gestion des exceptions a terminé le déroulement d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="36eaf-103">Notifies the profiler that the unwind phase of exception handling has finished unwinding a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="36eaf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36eaf-104">Syntax</span></span>  
  
```  
HRESULT ExceptionUnwindFunctionLeave();  
```  
  
## <a name="remarks"></a><span data-ttu-id="36eaf-105">Notes</span><span class="sxs-lookup"><span data-stu-id="36eaf-105">Remarks</span></span>  
 <span data-ttu-id="36eaf-106">Lorsque le `ExceptionUnwindFunctionLeave` est appelée, l’instance de la fonction et ses données de pile sont supprimées de la pile.</span><span class="sxs-lookup"><span data-stu-id="36eaf-106">When the `ExceptionUnwindFunctionLeave` method is called, the function instance and its stack data are removed from the stack.</span></span>  
  
 <span data-ttu-id="36eaf-107">Le profileur ne doit pas bloquer pendant cet appel, car la pile ne peut pas être dans un état qui autorise le garbage collection, et par conséquent, le garbage collection préemptif ne peut pas être activé.</span><span class="sxs-lookup"><span data-stu-id="36eaf-107">The profiler should not block during this call because the stack may not be in a state that allows garbage collection, and therefore preemptive garbage collection cannot be enabled.</span></span> <span data-ttu-id="36eaf-108">Si le profileur bloque et un garbage collection est tentée, le runtime bloque jusqu'à ce que ce rappel retourne.</span><span class="sxs-lookup"><span data-stu-id="36eaf-108">If the profiler blocks here and a garbage collection is attempted, the runtime will block until this callback returns.</span></span>  
  
 <span data-ttu-id="36eaf-109">En outre, au cours de cet appel, le profileur doit appeler pas dans le code managé ou de quelque manière qu’une allocation de mémoire managée.</span><span class="sxs-lookup"><span data-stu-id="36eaf-109">Also, during this call, the profiler must not call into managed code or in any way cause a managed-memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="36eaf-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="36eaf-110">Requirements</span></span>  
 <span data-ttu-id="36eaf-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="36eaf-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="36eaf-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="36eaf-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="36eaf-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="36eaf-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="36eaf-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="36eaf-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="36eaf-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36eaf-115">See Also</span></span>  
 [<span data-ttu-id="36eaf-116">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="36eaf-116">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="36eaf-117">ExceptionUnwindFunctionEnter, méthode</span><span class="sxs-lookup"><span data-stu-id="36eaf-117">ExceptionUnwindFunctionEnter Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionunwindfunctionenter-method.md)
