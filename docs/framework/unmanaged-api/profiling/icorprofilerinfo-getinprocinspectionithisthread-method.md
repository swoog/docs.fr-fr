---
title: ICorProfilerInfo::GetInprocInspectionIThisThread, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetInprocInspectionIThisThread
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetInprocInspectionIThisThread
helpviewer_keywords:
- ICorProfilerInfo::GetInprocInspectionIThisThread method [.NET Framework profiling]
- GetInprocInspectionIThisThread method [.NET Framework profiling]
ms.assetid: badddccd-f85c-416e-9f0f-419eab2c9d42
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 24b7af4b44d51da06e9d65104f1b469ef1d83b8a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59219432"
---
# <a name="icorprofilerinfogetinprocinspectionithisthread-method"></a><span data-ttu-id="ea8bc-102">ICorProfilerInfo::GetInprocInspectionIThisThread, méthode</span><span class="sxs-lookup"><span data-stu-id="ea8bc-102">ICorProfilerInfo::GetInprocInspectionIThisThread Method</span></span>
<span data-ttu-id="ea8bc-103">Obtient un objet qui peut être interrogé pour l’interface ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="ea8bc-103">Gets an object that can be queried for the ICorDebugThread interface.</span></span> <span data-ttu-id="ea8bc-104">Cette méthode est obsolète dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="ea8bc-104">This method is obsolete in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea8bc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea8bc-105">Syntax</span></span>  
  
```  
HRESULT GetInprocInspectionIThisThread(  
    [out] IUnknown **ppicd);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ea8bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea8bc-106">Parameters</span></span>  
 `ppicd`  
 <span data-ttu-id="ea8bc-107">[out](/cpp/atl/iunknown) objet qui peut être interrogé pour la `ICorDebugThread` interface.</span><span class="sxs-lookup"><span data-stu-id="ea8bc-107">[out](/cpp/atl/iunknown) object that can be queried for the `ICorDebugThread` interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ea8bc-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ea8bc-108">Remarks</span></span>  
 <span data-ttu-id="ea8bc-109">Le débogage des services du common language runtime (CLR) prise en charge limitée dans le processus de débogage dans le .NET Framework version 1.0.</span><span class="sxs-lookup"><span data-stu-id="ea8bc-109">The common language runtime (CLR) debugging services supported limited in-process debugging in the .NET Framework version 1.0.</span></span> <span data-ttu-id="ea8bc-110">Dans le processus de débogage activé un profileur d’utiliser les parties de l’inspection de l’API de débogage.</span><span class="sxs-lookup"><span data-stu-id="ea8bc-110">In-process debugging enabled a profiler to use the inspection portions of the debugging API.</span></span> <span data-ttu-id="ea8bc-111">À la suite de commentaires des clients, dans le processus de débogage a été supprimé depuis le .NET Framework version 2.0 et remplacé par un ensemble de fonctionnalités qui sont plus adaptées à l’API de profilage.</span><span class="sxs-lookup"><span data-stu-id="ea8bc-111">As a result of customer feedback, in-process debugging has been removed from the .NET Framework in version 2.0, and replaced with a set of functionality that is more in line with the profiling API.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ea8bc-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea8bc-112">Requirements</span></span>  
 <span data-ttu-id="ea8bc-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ea8bc-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ea8bc-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ea8bc-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ea8bc-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ea8bc-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ea8bc-116">**Version du .NET framework :** 1.0</span><span class="sxs-lookup"><span data-stu-id="ea8bc-116">**.NET Framework Version:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ea8bc-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea8bc-117">See also</span></span>

- [<span data-ttu-id="ea8bc-118">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="ea8bc-118">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
