---
title: ICorProfilerInfo::EndInprocDebugging, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.EndInprocDebugging
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::EndInprocDebugging
helpviewer_keywords:
- ICorProfilerInfo::EndInprocDebugging method [.NET Framework profiling]
- EndInprocDebugging method [.NET Framework profiling]
ms.assetid: 35bc1188-9767-4141-8038-60ea015b99ac
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bcae66fd30c29a0a3c9bd0b5ffc2047efdf3788d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049659"
---
# <a name="icorprofilerinfoendinprocdebugging-method"></a><span data-ttu-id="79fb8-102">ICorProfilerInfo::EndInprocDebugging, méthode</span><span class="sxs-lookup"><span data-stu-id="79fb8-102">ICorProfilerInfo::EndInprocDebugging Method</span></span>
<span data-ttu-id="79fb8-103">Arrête une session de débogage in-process.</span><span class="sxs-lookup"><span data-stu-id="79fb8-103">Shuts down an in-process debugging session.</span></span> <span data-ttu-id="79fb8-104">Cette méthode est obsolète dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="79fb8-104">This method is obsolete in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79fb8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79fb8-105">Syntax</span></span>  
  
```  
HRESULT EndInprocDebugging(  
    [in]  DWORD dwProfilerContext);  
```  
  
## <a name="parameters"></a><span data-ttu-id="79fb8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79fb8-106">Parameters</span></span>  
 `dwProfilerContext`  
 <span data-ttu-id="79fb8-107">[in] Une valeur qui identifie la session de débogage.</span><span class="sxs-lookup"><span data-stu-id="79fb8-107">[in] A value that identifies the debugging session.</span></span> <span data-ttu-id="79fb8-108">Cette valeur doit être la même que celle reçue dans le [ICorProfilerInfo::BeginInprocDebugging](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-begininprocdebugging-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="79fb8-108">This value must be the same as that received in the [ICorProfilerInfo::BeginInprocDebugging](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-begininprocdebugging-method.md) method.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="79fb8-109">Notes</span><span class="sxs-lookup"><span data-stu-id="79fb8-109">Remarks</span></span>  
 <span data-ttu-id="79fb8-110">Vous devez appeler [ICorProfilerInfo::BeginInprocDebugging](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-begininprocdebugging-method.md) et `EndInprocDebugging` au sein de la même méthode de rappel.</span><span class="sxs-lookup"><span data-stu-id="79fb8-110">You must call [ICorProfilerInfo::BeginInprocDebugging](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-begininprocdebugging-method.md) and `EndInprocDebugging` within the same callback method.</span></span>  
  
 <span data-ttu-id="79fb8-111">Les services de débogage CLR pris en charge limitée dans le processus de débogage dans les versions 1.0 et 1.1 du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="79fb8-111">The CLR debugging services supported limited in-process debugging in the .NET Framework versions 1.0 and 1.1.</span></span> <span data-ttu-id="79fb8-112">Dans le processus de débogage activé un profileur d’utiliser les parties de l’inspection de l’API de débogage.</span><span class="sxs-lookup"><span data-stu-id="79fb8-112">In-process debugging enabled a profiler to use the inspection portions of the debugging API.</span></span> <span data-ttu-id="79fb8-113">Toutefois, en raison des commentaires client, dans le processus de débogage a été supprimé depuis le .NET Framework version 2.0 et remplacé par un ensemble de fonctionnalités qui sont plus adaptées à l’API de profilage.</span><span class="sxs-lookup"><span data-stu-id="79fb8-113">However, due to customer feedback, in-process debugging has been removed from the .NET Framework in version 2.0, and replaced with a set of functionality that is more in line with the profiling API.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79fb8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79fb8-114">Requirements</span></span>  
 <span data-ttu-id="79fb8-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="79fb8-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79fb8-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="79fb8-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="79fb8-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="79fb8-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="79fb8-118">**Version du .NET framework :** 1.0</span><span class="sxs-lookup"><span data-stu-id="79fb8-118">**.NET Framework Version:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79fb8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79fb8-119">See also</span></span>

- [<span data-ttu-id="79fb8-120">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="79fb8-120">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
