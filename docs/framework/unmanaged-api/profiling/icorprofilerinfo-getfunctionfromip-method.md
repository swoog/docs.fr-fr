---
title: ICorProfilerInfo::GetFunctionFromIP, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetFunctionFromIP
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetFunctionFromIP
helpviewer_keywords:
- GetFunctionFromIP method [.NET Framework profiling]
- ICorProfilerInfo::GetFunctionFromIP method [.NET Framework profiling]
ms.assetid: f069802a-198f-46dd-9f09-4f77adffc9ba
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2b0859d2f6d4ea2abf72867f2a803132cbd04225
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54568645"
---
# <a name="icorprofilerinfogetfunctionfromip-method"></a><span data-ttu-id="68b76-102">ICorProfilerInfo::GetFunctionFromIP, méthode</span><span class="sxs-lookup"><span data-stu-id="68b76-102">ICorProfilerInfo::GetFunctionFromIP Method</span></span>
<span data-ttu-id="68b76-103">Mappe un pointeur d’instruction de code managé à un `FunctionID`.</span><span class="sxs-lookup"><span data-stu-id="68b76-103">Maps a managed code instruction pointer to a `FunctionID`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="68b76-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68b76-104">Syntax</span></span>  
  
```  
HRESULT GetFunctionFromIP(  
    [in]  LPCBYTE    ip,  
    [out] FunctionID *pFunctionId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="68b76-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68b76-105">Parameters</span></span>  
 `ip`  
 <span data-ttu-id="68b76-106">[in] Le pointeur d’instruction dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="68b76-106">[in] The instruction pointer in managed code.</span></span>  
  
 `pFunctionId`  
 <span data-ttu-id="68b76-107">[out] L’ID de la fonction retournée.</span><span class="sxs-lookup"><span data-stu-id="68b76-107">[out] The returned function ID.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="68b76-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="68b76-108">Requirements</span></span>  
 <span data-ttu-id="68b76-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="68b76-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="68b76-110">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="68b76-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="68b76-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="68b76-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="68b76-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="68b76-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="68b76-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68b76-113">See also</span></span>
- [<span data-ttu-id="68b76-114">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="68b76-114">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
