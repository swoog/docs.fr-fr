---
title: ICorProfilerCallback::ExceptionCLRCatcherFound, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionCLRCatcherFound
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionCLRCatcherFound
helpviewer_keywords:
- ICorProfilerCallback::ExceptionCLRCatcherFound method [.NET Framework profiling]
- ExceptionCLRCatcherFound method [.NET Framework profiling]
ms.assetid: 73fe8b4b-8f9a-4ba5-a10c-b26521396a66
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 33dc6a863af0c03066d5f01e5101c9a6cc6d5859
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33451121"
---
# <a name="icorprofilercallbackexceptionclrcatcherfound-method"></a><span data-ttu-id="c5908-102">ICorProfilerCallback::ExceptionCLRCatcherFound, méthode</span><span class="sxs-lookup"><span data-stu-id="c5908-102">ICorProfilerCallback::ExceptionCLRCatcherFound Method</span></span>
<span data-ttu-id="c5908-103">Appelé lorsqu’un `catch` bloquer pour une exception se trouve dans le common language runtime (CLR) lui-même.</span><span class="sxs-lookup"><span data-stu-id="c5908-103">Called when a `catch` block for an exception is found inside the common language runtime (CLR) itself.</span></span> <span data-ttu-id="c5908-104">Cette méthode est obsolète dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="c5908-104">This method is obsolete in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c5908-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5908-105">Syntax</span></span>  
  
```  
HRESULT ExceptionCLRCatcherFound();  
```  
  
## <a name="requirements"></a><span data-ttu-id="c5908-106">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c5908-106">Requirements</span></span>  
 <span data-ttu-id="c5908-107">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c5908-107">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c5908-108">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c5908-108">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c5908-109">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c5908-109">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c5908-110">**Version du .NET framework :** 1.0</span><span class="sxs-lookup"><span data-stu-id="c5908-110">**.NET Framework Version:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5908-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5908-111">See Also</span></span>  
 [<span data-ttu-id="c5908-112">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="c5908-112">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="c5908-113">ExceptionCLRCatcherExecute, méthode</span><span class="sxs-lookup"><span data-stu-id="c5908-113">ExceptionCLRCatcherExecute Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionclrcatcherexecute-method.md)
