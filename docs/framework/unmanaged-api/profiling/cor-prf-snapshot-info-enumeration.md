---
title: COR_PRF_SNAPSHOT_INFO, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_SNAPSHOT_INFO
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_SNAPSHOT_INFO
helpviewer_keywords:
- COR_PRF_SNAPSHOT_INFO enumeration [.NET Framework profiling]
ms.assetid: a5906b2a-ad4a-4cc6-a421-2d7d8adf7468
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fa85fb2cebb47ecbd7b0f091cb79f6ea0936b1cb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59177838"
---
# <a name="corprfsnapshotinfo-enumeration"></a><span data-ttu-id="0c00e-102">COR_PRF_SNAPSHOT_INFO, énumération</span><span class="sxs-lookup"><span data-stu-id="0c00e-102">COR_PRF_SNAPSHOT_INFO Enumeration</span></span>
<span data-ttu-id="0c00e-103">Spécifie la quantité de données à retourner avec un instantané de pile dans chaque appel à du profileur [StackSnapshotCallback](../../../../docs/framework/unmanaged-api/profiling/stacksnapshotcallback-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="0c00e-103">Specifies how much data to pass back with a stack snapshot in each call to the profiler's [StackSnapshotCallback](../../../../docs/framework/unmanaged-api/profiling/stacksnapshotcallback-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c00e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c00e-104">Syntax</span></span>  
  
```  
typedef enum _COR_PRF_SNAPSHOT_INFO {  
    COR_PRF_SNAPSHOT_DEFAULT = 0x0,  
    COR_PRF_SNAPSHOT_REGISTER_CONTEXT = 0x1,  
    COR_PRF_SNAPSHOT_X86_OPTIMIZED = 0X2  
} COR_PRF_SNAPSHOT_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="0c00e-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0c00e-105">Members</span></span>  
  
|<span data-ttu-id="0c00e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="0c00e-106">Members</span></span>|<span data-ttu-id="0c00e-107">Description</span><span class="sxs-lookup"><span data-stu-id="0c00e-107">Description</span></span>|  
|-------------|-----------------|  
|`COR_PRF_SNAPSHOT_DEFAULT`|<span data-ttu-id="0c00e-108">Indique que les valeurs doivent être passées pour tous les `StackSnapshotCallback` paramètres, sauf le `context` paramètre.</span><span class="sxs-lookup"><span data-stu-id="0c00e-108">Indicates that values must be passed for all `StackSnapshotCallback` parameters, except the `context` parameter.</span></span>|  
|`COR_PRF_SNAPSHOT_REGISTER_CONTEXT`|<span data-ttu-id="0c00e-109">Indique que les valeurs doivent être passées pour tous les `StackSnapshotCallback` paramètres, y compris le `context` paramètre.</span><span class="sxs-lookup"><span data-stu-id="0c00e-109">Indicates that values must be passed for all `StackSnapshotCallback` parameters, including the `context` parameter.</span></span>|  
|`COR_PRF_SNAPSHOT_X86_OPTIMIZED`|<span data-ttu-id="0c00e-110">Indique qu’un algorithme de parcours de pile alternatif plus simple sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="0c00e-110">Indicates that a simpler, alternative stack-walking algorithm will be used.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0c00e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0c00e-111">Remarks</span></span>  
 <span data-ttu-id="0c00e-112">Les valeurs sont fournies par le `COR_PRF_SNAPSHOT_INFO` énumération sont passés comme paramètres à la [DoStackSnapshot](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-dostacksnapshot-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="0c00e-112">Values that are provided by the `COR_PRF_SNAPSHOT_INFO` enumeration are passed as parameters to the [DoStackSnapshot](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-dostacksnapshot-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c00e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c00e-113">Requirements</span></span>  
 <span data-ttu-id="0c00e-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0c00e-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c00e-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="0c00e-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="0c00e-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0c00e-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0c00e-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c00e-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c00e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c00e-118">See also</span></span>

- [<span data-ttu-id="0c00e-119">DoStackSnapshot, méthode</span><span class="sxs-lookup"><span data-stu-id="0c00e-119">DoStackSnapshot Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-dostacksnapshot-method.md)
- [<span data-ttu-id="0c00e-120">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="0c00e-120">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
