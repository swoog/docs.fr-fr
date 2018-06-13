---
title: Interface de ICorProfilerInfo6
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo6
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: 6f2bb148-1e2b-4e45-a5a5-0ceddc40064b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: da1aab48e2eef229bb31e9443a5549c3f9fbc621
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33455300"
---
# <a name="icorprofilerinfo6-interface"></a><span data-ttu-id="285ff-102">Interface de ICorProfilerInfo6</span><span class="sxs-lookup"><span data-stu-id="285ff-102">ICorProfilerInfo6 Interface</span></span>
<span data-ttu-id="285ff-103">[Pris en charge dans le .NET Framework 4.6 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="285ff-103">[Supported in the .NET Framework 4.6 and later versions]</span></span>  
  
 <span data-ttu-id="285ff-104">Une sous-classe de [ICorProfilerInfo5](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-interface.md) qui fournit un énumérateur pour toutes les méthodes qui sont définis dans un module NGen donné et l’inline une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="285ff-104">A subclass of [ICorProfilerInfo5](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-interface.md) that provides an enumerator for all methods that are defined in a given NGen module and inline a given method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="285ff-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="285ff-105">Methods</span></span>  
  
|<span data-ttu-id="285ff-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="285ff-106">Method</span></span>|<span data-ttu-id="285ff-107">Description</span><span class="sxs-lookup"><span data-stu-id="285ff-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="285ff-108">ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="285ff-108">ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo6-enumngenmodulemethodsinliningthismethod-method.md)|<span data-ttu-id="285ff-109">Retourne un énumérateur pour toutes les méthodes qui appartiennent à un module NGen donné et qui sont incorporées dans le corps d’une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="285ff-109">Returns an enumerator for all methods that belong to a given NGen module and that are inlined in the body of a given method.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="285ff-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="285ff-110">Requirements</span></span>  
 <span data-ttu-id="285ff-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="285ff-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="285ff-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="285ff-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="285ff-113">**Versions du .NET framework :** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="285ff-113">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="285ff-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="285ff-114">See Also</span></span>  
 [<span data-ttu-id="285ff-115">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="285ff-115">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
