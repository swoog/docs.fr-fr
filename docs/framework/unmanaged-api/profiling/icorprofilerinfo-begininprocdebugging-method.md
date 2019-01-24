---
title: ICorProfilerInfo::BeginInprocDebugging, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.BeginInprocDebugging
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::BeginInprocDebugging
helpviewer_keywords:
- BeginInprocDebugging method [.NET Framework profiling]
- ICorProfilerInfo::BeginInprocDebugging method [.NET Framework profiling]
ms.assetid: c5c82c69-99f8-4447-aee0-42cca0a5eb5c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 330a159e056018d702eec7e4fef80c3d8e041212
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54630799"
---
# <a name="icorprofilerinfobegininprocdebugging-method"></a><span data-ttu-id="1b297-102">ICorProfilerInfo::BeginInprocDebugging, méthode</span><span class="sxs-lookup"><span data-stu-id="1b297-102">ICorProfilerInfo::BeginInprocDebugging Method</span></span>
<span data-ttu-id="1b297-103">Initialise intra-processus prise en charge de débogage.</span><span class="sxs-lookup"><span data-stu-id="1b297-103">Initializes in-process debugging support.</span></span> <span data-ttu-id="1b297-104">Cette méthode est obsolète dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="1b297-104">This method is obsolete in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1b297-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b297-105">Syntax</span></span>  
  
```  
HRESULT BeginInprocDebugging(  
    [in]  BOOL   fThisThreadOnly,  
    [out] DWORD *pdwProfilerContext);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1b297-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b297-106">Parameters</span></span>  
 `fThisThreadOnly`  
 <span data-ttu-id="1b297-107">[in] Définissez cette valeur sur `true` pour initialiser la prise en charge du débogage pour le thread actuel uniquement ; affectez-lui la valeur `false` pour initialiser la prise en charge du débogage pour tous les threads.</span><span class="sxs-lookup"><span data-stu-id="1b297-107">[in] Set this value to `true` to initialize debugging support for only the current thread; set it to `false` to initialize debugging support for all threads.</span></span>  
  
 `pdwProfilerContext`  
 <span data-ttu-id="1b297-108">[out] Pointeur vers une valeur retournée qui identifie la session de débogage.</span><span class="sxs-lookup"><span data-stu-id="1b297-108">[out] The pointer to a returned value that identifies the debugging session.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1b297-109">Notes</span><span class="sxs-lookup"><span data-stu-id="1b297-109">Remarks</span></span>  
 <span data-ttu-id="1b297-110">Les services de débogage CLR pris en charge limitée dans le processus de débogage dans les versions 1.0 et 1.1 du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="1b297-110">The CLR debugging services supported limited in-process debugging in the .NET Framework versions 1.0 and 1.1.</span></span> <span data-ttu-id="1b297-111">Dans le processus de débogage activé un profileur d’utiliser les parties de l’inspection de l’API de débogage.</span><span class="sxs-lookup"><span data-stu-id="1b297-111">In-process debugging enabled a profiler to use the inspection portions of the debugging API.</span></span> <span data-ttu-id="1b297-112">Toutefois, en raison des commentaires client, dans le processus de débogage a été supprimé depuis le .NET Framework version 2.0 et remplacé par un ensemble de fonctionnalités qui sont plus adaptées à l’API de profilage.</span><span class="sxs-lookup"><span data-stu-id="1b297-112">However, due to customer feedback, in-process debugging has been removed from the .NET Framework in version 2.0, and replaced with a set of functionality that is more in line with the profiling API.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1b297-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1b297-113">Requirements</span></span>  
 <span data-ttu-id="1b297-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1b297-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1b297-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="1b297-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="1b297-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1b297-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1b297-117">**Version du .NET framework :** 1.0</span><span class="sxs-lookup"><span data-stu-id="1b297-117">**.NET Framework Version:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b297-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b297-118">See also</span></span>
- [<span data-ttu-id="1b297-119">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="1b297-119">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
