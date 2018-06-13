---
title: ICorProfilerInfo::ForceGC, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.ForceGC
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::ForceGC
helpviewer_keywords:
- ICorProfilerInfo::ForceGC method [.NET Framework profiling]
- ForceGC method [.NET Framework profiling]
ms.assetid: 0da1ef80-d242-4636-87d0-43e0470b342a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 06601b1aa675dd9ecf023a9f83d881ba1591ac52
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33454471"
---
# <a name="icorprofilerinfoforcegc-method"></a><span data-ttu-id="ca13e-102">ICorProfilerInfo::ForceGC, méthode</span><span class="sxs-lookup"><span data-stu-id="ca13e-102">ICorProfilerInfo::ForceGC Method</span></span>
<span data-ttu-id="ca13e-103">Force un garbage collection pour se produire dans le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="ca13e-103">Forces garbage collection to occur within the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca13e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca13e-104">Syntax</span></span>  
  
```  
HRESULT ForceGC();  
```  
  
## <a name="remarks"></a><span data-ttu-id="ca13e-105">Notes</span><span class="sxs-lookup"><span data-stu-id="ca13e-105">Remarks</span></span>  
 <span data-ttu-id="ca13e-106">Le `ForceGC` méthode doit être appelée uniquement à partir d’un thread qui n’a jamais exécuté du code managé et n’a pas de rappels de profileur sur sa pile.</span><span class="sxs-lookup"><span data-stu-id="ca13e-106">The `ForceGC` method must be called only from a thread that has never run managed code and does not have any profiler callbacks on its stack.</span></span> <span data-ttu-id="ca13e-107">L’implémentation la plus commode consiste à créer un thread séparé dans le profileur appelle `ForceGC` quand il est signalé.</span><span class="sxs-lookup"><span data-stu-id="ca13e-107">The most convenient implementation is to create a separate thread within the profiler that calls `ForceGC` when signaled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca13e-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ca13e-108">Requirements</span></span>  
 <span data-ttu-id="ca13e-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ca13e-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca13e-110">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ca13e-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ca13e-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ca13e-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ca13e-112">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca13e-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca13e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca13e-113">See Also</span></span>  
 [<span data-ttu-id="ca13e-114">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="ca13e-114">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
