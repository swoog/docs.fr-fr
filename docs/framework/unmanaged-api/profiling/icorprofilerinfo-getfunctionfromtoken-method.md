---
title: ICorProfilerInfo::GetFunctionFromToken, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetFunctionFromToken
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetFunctionFromToken
helpviewer_keywords:
- ICorProfilerInfo::GetFunctionFromToken method [.NET Framework profiling]
- GetFunctionFromToken method, ICorProfilerInfo interface [.NET Framework profiling]
ms.assetid: 0eed759f-cce8-405d-88dc-9ee293a38928
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5f4fb2292154a2660a2db3f0b3962fcf2114e385
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59099973"
---
# <a name="icorprofilerinfogetfunctionfromtoken-method"></a><span data-ttu-id="64bf2-102">ICorProfilerInfo::GetFunctionFromToken, méthode</span><span class="sxs-lookup"><span data-stu-id="64bf2-102">ICorProfilerInfo::GetFunctionFromToken Method</span></span>
<span data-ttu-id="64bf2-103">Obtient l’ID d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="64bf2-103">Gets the ID of a function.</span></span> <span data-ttu-id="64bf2-104">Cette méthode est obsolète dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="64bf2-104">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="64bf2-105">Utilisez le [ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getfunctionfromtokenandtypeargs-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="64bf2-105">Use the [ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getfunctionfromtokenandtypeargs-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64bf2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64bf2-106">Syntax</span></span>  
  
```  
HRESULT GetFunctionFromToken(  
    [in]  ModuleID   moduleId,  
    [in]  mdToken    token,  
    [out] FunctionID *pFunctionId);  
```  
  
## <a name="remarks"></a><span data-ttu-id="64bf2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="64bf2-107">Remarks</span></span>  
 <span data-ttu-id="64bf2-108">Le `GetFunctionFromToken` méthode ne fonctionne pas pour les fonctions génériques ou des fonctions dans des types génériques ; il est désormais obsolète.</span><span class="sxs-lookup"><span data-stu-id="64bf2-108">The `GetFunctionFromToken` method will not work for generic functions or functions in generic types; it is now obsolete.</span></span> <span data-ttu-id="64bf2-109">Utilisez `ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs` pour toutes les fonctions.</span><span class="sxs-lookup"><span data-stu-id="64bf2-109">Use `ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs` for all functions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="64bf2-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64bf2-110">Requirements</span></span>  
 <span data-ttu-id="64bf2-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="64bf2-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="64bf2-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="64bf2-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="64bf2-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="64bf2-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="64bf2-114">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="64bf2-114">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64bf2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64bf2-115">See also</span></span>

- [<span data-ttu-id="64bf2-116">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="64bf2-116">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
