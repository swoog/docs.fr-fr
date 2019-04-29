---
title: ICorProfilerCallback::JITCompilationFinished, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.JITCompilationFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::JITCompilationFinished
helpviewer_keywords:
- JITCompilationFinished method [.NET Framework profiling]
- ICorProfilerCallback::JITCompilationFinished method [.NET Framework profiling]
ms.assetid: 8dcd7537-d0c6-498c-8a56-2c060310ef65
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1abc4dd209581c9f7c8e950ea1addc74c611d248
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61787944"
---
# <a name="icorprofilercallbackjitcompilationfinished-method"></a><span data-ttu-id="71f72-102">ICorProfilerCallback::JITCompilationFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="71f72-102">ICorProfilerCallback::JITCompilationFinished Method</span></span>
<span data-ttu-id="71f72-103">Notifie le profileur que le compilateur juste-à-temps (JIT) a terminé la compilation d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="71f72-103">Notifies the profiler that the just-in-time (JIT) compiler has finished compiling a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="71f72-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71f72-104">Syntax</span></span>  
  
```  
HRESULT JITCompilationFinished(  
    [in] FunctionID functionId,  
    [in] HRESULT    hrStatus,  
    [in] BOOL       fIsSafeToBlock);  
```  
  
## <a name="parameters"></a><span data-ttu-id="71f72-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71f72-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="71f72-106">[in] L’ID de la fonction qui a été compilée.</span><span class="sxs-lookup"><span data-stu-id="71f72-106">[in] The ID of the function that was compiled.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="71f72-107">[in] Une valeur indiquant si la compilation a réussi.</span><span class="sxs-lookup"><span data-stu-id="71f72-107">[in] A value indicating whether compilation was successful.</span></span>  
  
 `fIsSafeToBlock`  
 <span data-ttu-id="71f72-108">[in] Une valeur qui indique au profileur si un blocage affectera le fonctionnement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="71f72-108">[in] A value indicating to the profiler whether blocking will affect the operation of the runtime.</span></span> <span data-ttu-id="71f72-109">La valeur est `true` si le blocage peut entraîner l’exécution pour attendre que le thread appelant retourner à partir de ce rappel ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="71f72-109">The value is `true` if blocking may cause the runtime to wait for the calling thread to return from this callback; otherwise, `false`.</span></span>  
  
 <span data-ttu-id="71f72-110">Bien que la valeur `true` ne nuise pas au runtime, elle peut fausser les résultats de profilage.</span><span class="sxs-lookup"><span data-stu-id="71f72-110">Although a value of `true` will not harm the runtime, it can skew the profiling results.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="71f72-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71f72-111">Requirements</span></span>  
 <span data-ttu-id="71f72-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="71f72-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="71f72-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="71f72-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="71f72-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="71f72-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="71f72-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="71f72-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71f72-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71f72-116">See also</span></span>

- [<span data-ttu-id="71f72-117">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="71f72-117">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="71f72-118">JITCompilationStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="71f72-118">JITCompilationStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-jitcompilationstarted-method.md)
