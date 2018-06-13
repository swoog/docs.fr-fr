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
ms.openlocfilehash: f2dc7c22ee075f347604864d8bee1a4e871da616
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33451764"
---
# <a name="icorprofilercallbackexceptionoshandlerenter-method"></a><span data-ttu-id="ee9e4-102">ICorProfilerCallback::ExceptionOSHandlerEnter, méthode</span><span class="sxs-lookup"><span data-stu-id="ee9e4-102">ICorProfilerCallback::ExceptionOSHandlerEnter Method</span></span>
<span data-ttu-id="ee9e4-103">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ee9e4-103">Not implemented.</span></span> <span data-ttu-id="ee9e4-104">Un profileur qui a besoin d’informations sur les exceptions non managées doit obtenir ces informations par d’autres moyens.</span><span class="sxs-lookup"><span data-stu-id="ee9e4-104">A profiler that needs unmanaged exception information must obtain this information through other means.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ee9e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee9e4-105">Syntax</span></span>  
  
```  
HRESULT ExceptionOSHandlerEnter(  
    [in] UINT_PTR __unused);  
```  
  
## <a name="requirements"></a><span data-ttu-id="ee9e4-106">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ee9e4-106">Requirements</span></span>  
 <span data-ttu-id="ee9e4-107">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ee9e4-107">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ee9e4-108">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ee9e4-108">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ee9e4-109">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ee9e4-109">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ee9e4-110">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ee9e4-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee9e4-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee9e4-111">See Also</span></span>  
 [<span data-ttu-id="ee9e4-112">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="ee9e4-112">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
