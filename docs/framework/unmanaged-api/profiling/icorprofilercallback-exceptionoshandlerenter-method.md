---
title: ICorProfilerCallback::ExceptionOSHandlerEnter, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionOSHandlerEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionOSHandlerEnter
helpviewer_keywords:
- ExceptionOSHandlerEnter method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionOSHandlerEnter method [.NET Framework profiling]
ms.assetid: 09238b9b-9359-4780-89dc-2f5e4f57920e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1fcdd52e648b2461036921772b6b5684ba6aec22
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59175836"
---
# <a name="icorprofilercallbackexceptionoshandlerenter-method"></a><span data-ttu-id="024a2-102">ICorProfilerCallback::ExceptionOSHandlerEnter, méthode</span><span class="sxs-lookup"><span data-stu-id="024a2-102">ICorProfilerCallback::ExceptionOSHandlerEnter Method</span></span>
<span data-ttu-id="024a2-103">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="024a2-103">Not implemented.</span></span> <span data-ttu-id="024a2-104">Un profileur qui a besoin d’informations sur les exceptions non managées doit obtenir ces informations par d’autres moyens.</span><span class="sxs-lookup"><span data-stu-id="024a2-104">A profiler that needs unmanaged exception information must obtain this information through other means.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="024a2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="024a2-105">Syntax</span></span>  
  
```  
HRESULT ExceptionOSHandlerEnter(  
    [in] UINT_PTR __unused);  
```  
  
## <a name="requirements"></a><span data-ttu-id="024a2-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="024a2-106">Requirements</span></span>  
 <span data-ttu-id="024a2-107">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="024a2-107">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="024a2-108">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="024a2-108">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="024a2-109">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="024a2-109">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="024a2-110">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="024a2-110">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="024a2-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="024a2-111">See also</span></span>

- [<span data-ttu-id="024a2-112">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="024a2-112">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
