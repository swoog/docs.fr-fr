---
title: ICorProfilerInfo::SetILFunctionBody, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.SetILFunctionBody
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::SetILFunctionBody
helpviewer_keywords:
- ICorProfilerInfo::SetILFunctionBody method [.NET Framework profiling]
- SetILFunctionBody method [.NET Framework profiling]
ms.assetid: b159c712-00f4-4fc7-a990-40bf9f642e8f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 886bb706be30481c082012bf057a001f37903b16
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33461654"
---
# <a name="icorprofilerinfosetilfunctionbody-method"></a><span data-ttu-id="fe804-102">ICorProfilerInfo::SetILFunctionBody, méthode</span><span class="sxs-lookup"><span data-stu-id="fe804-102">ICorProfilerInfo::SetILFunctionBody Method</span></span>
<span data-ttu-id="fe804-103">Remplace le corps de la fonction spécifiée dans le module spécifié.</span><span class="sxs-lookup"><span data-stu-id="fe804-103">Replaces the body of the specified function in the specified module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe804-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe804-104">Syntax</span></span>  
  
```  
HRESULT SetILFunctionBody(  
    [in] ModuleID    moduleId,  
    [in] mdMethodDef methodid,  
    [in] LPCBYTE     pbNewILMethodHeader);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fe804-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe804-105">Parameters</span></span>  
 `moduleId`  
 <span data-ttu-id="fe804-106">[in] L’ID du module dans lequel la fonction réside.</span><span class="sxs-lookup"><span data-stu-id="fe804-106">[in] The ID of the module in which the function resides.</span></span>  
  
 `methodid`  
 <span data-ttu-id="fe804-107">[in] Le jeton de la fonction pour laquelle remplacer le corps.</span><span class="sxs-lookup"><span data-stu-id="fe804-107">[in] The token of the function for which to replace the body.</span></span>  
  
 `pbNewILMethodHeader`  
 <span data-ttu-id="fe804-108">[in] Le nouvel en-tête pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="fe804-108">[in] The new header for the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fe804-109">Notes</span><span class="sxs-lookup"><span data-stu-id="fe804-109">Remarks</span></span>  
 <span data-ttu-id="fe804-110">Le `SetILFunctionBody` méthode remplace l’adresse virtuelle relative de la fonction dans les métadonnées afin qu’elle pointe vers le nouveau corps de fonction et ajuste les structures de données internes selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="fe804-110">The `SetILFunctionBody` method replaces the relative virtual address of the function in the metadata so that it points to the new function body, and adjusts any internal data structures as required.</span></span>  
  
 <span data-ttu-id="fe804-111">Le `SetILFunctionBody` méthode peut être appelée uniquement sur les fonctions qui n’ont jamais été compilées par un compilateur juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="fe804-111">The `SetILFunctionBody` method can be called on only those functions that have never been compiled by a just-in-time (JIT) compiler.</span></span>  
  
 <span data-ttu-id="fe804-112">Utilisez le [ICorProfilerInfo::GetILFunctionBodyAllocator](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getilfunctionbodyallocator-method.md) méthode d’allocation d’espace pour la nouvelle méthode pour vous assurer que la mémoire tampon est compatible.</span><span class="sxs-lookup"><span data-stu-id="fe804-112">Use the [ICorProfilerInfo::GetILFunctionBodyAllocator](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getilfunctionbodyallocator-method.md) method to allocate space for the new method to ensure that the buffer is compatible.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe804-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe804-113">Requirements</span></span>  
 <span data-ttu-id="fe804-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fe804-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe804-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fe804-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="fe804-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fe804-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fe804-117">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe804-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe804-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe804-118">See Also</span></span>  
 [<span data-ttu-id="fe804-119">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="fe804-119">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
