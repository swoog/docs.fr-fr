---
title: ICorProfilerCallback::ExceptionThrown, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionThrown
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionThrown
helpviewer_keywords:
- ExceptionThrown method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionThrown method [.NET Framework profiling]
ms.assetid: f1a23f3b-ac21-4905-8abf-8ea59f15af53
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e9cdbc2234519c0dba1a5004246492e7609ea2b3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59180490"
---
# <a name="icorprofilercallbackexceptionthrown-method"></a><span data-ttu-id="d14ff-102">ICorProfilerCallback::ExceptionThrown, méthode</span><span class="sxs-lookup"><span data-stu-id="d14ff-102">ICorProfilerCallback::ExceptionThrown Method</span></span>
<span data-ttu-id="d14ff-103">Notifie le profileur qu’une exception a été levée.</span><span class="sxs-lookup"><span data-stu-id="d14ff-103">Notifies the profiler that an exception has been thrown.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d14ff-104">Cette fonction est appelée uniquement si l’exception atteint le code managé.</span><span class="sxs-lookup"><span data-stu-id="d14ff-104">This function is called only if the exception reaches managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d14ff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d14ff-105">Syntax</span></span>  
  
```  
HRESULT ExceptionThrown(  
    [in] ObjectID thrownObjectId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d14ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d14ff-106">Parameters</span></span>  
 `thrownObjectId`  
 <span data-ttu-id="d14ff-107">[in] L’ID de l’objet qui a provoqué l’exception levée.</span><span class="sxs-lookup"><span data-stu-id="d14ff-107">[in] The ID of the object that caused the exception to be thrown.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d14ff-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d14ff-108">Remarks</span></span>  
 <span data-ttu-id="d14ff-109">Le profileur ne doit pas bloquer dans son implémentation de cette méthode, car la pile ne peut pas être dans un état qui autorise le garbage collection, et par conséquent, le garbage collection préemptif ne peut pas être activé.</span><span class="sxs-lookup"><span data-stu-id="d14ff-109">The profiler should not block in its implementation of this method because the stack may not be in a state that allows garbage collection, and therefore preemptive garbage collection cannot be enabled.</span></span> <span data-ttu-id="d14ff-110">Si le profileur bloque ici et le garbage collection est tenté, le runtime bloque jusqu'à ce que ce rappel renvoie.</span><span class="sxs-lookup"><span data-stu-id="d14ff-110">If the profiler blocks here and garbage collection is attempted, the runtime will block until this callback returns.</span></span>  
  
 <span data-ttu-id="d14ff-111">L’implémentation du profileur de cette méthode ne doit pas appeler dans du code managé ou de quelque manière qu’une allocation de mémoire managée.</span><span class="sxs-lookup"><span data-stu-id="d14ff-111">The profiler's implementation of this method should not call into managed code or in any way cause a managed-memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d14ff-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d14ff-112">Requirements</span></span>  
 <span data-ttu-id="d14ff-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d14ff-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d14ff-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d14ff-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d14ff-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d14ff-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="d14ff-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="d14ff-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="d14ff-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d14ff-117">See also</span></span>

- [<span data-ttu-id="d14ff-118">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="d14ff-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
