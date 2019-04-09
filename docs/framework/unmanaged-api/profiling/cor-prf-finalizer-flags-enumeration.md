---
title: COR_PRF_FINALIZER_FLAGS, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_FINALIZER_FLAGS
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_FINALIZER_FLAGS
helpviewer_keywords:
- COR_PRF_FINALIZER_FLAGS enumeration [.NET Framework profiling]
ms.assetid: 297d7721-3911-4f36-9e34-d9da0c33e22a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d5037f335e8d66c341d70d91d955a1ac7571b823
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59123758"
---
# <a name="corprffinalizerflags-enumeration"></a><span data-ttu-id="470a9-102">COR_PRF_FINALIZER_FLAGS, énumération</span><span class="sxs-lookup"><span data-stu-id="470a9-102">COR_PRF_FINALIZER_FLAGS Enumeration</span></span>
<span data-ttu-id="470a9-103">Décrit le finaliseur pour un objet.</span><span class="sxs-lookup"><span data-stu-id="470a9-103">Describes the finalizer for an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="470a9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="470a9-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_FINALIZER_CRITICAL = 0x1  
} COR_PRF_FINALIZER_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="470a9-105">Membres</span><span class="sxs-lookup"><span data-stu-id="470a9-105">Members</span></span>  
  
|<span data-ttu-id="470a9-106">Membre</span><span class="sxs-lookup"><span data-stu-id="470a9-106">Member</span></span>|<span data-ttu-id="470a9-107">Description</span><span class="sxs-lookup"><span data-stu-id="470a9-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_FINALIZER_CRITICAL`|<span data-ttu-id="470a9-108">Le finaliseur est critique.</span><span class="sxs-lookup"><span data-stu-id="470a9-108">The finalizer is critical.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="470a9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="470a9-109">Remarks</span></span>  
 <span data-ttu-id="470a9-110">Le `COR_PRF_FINALIZER_FLAGS` énumération est utilisée par le [ICorProfilerCallback2::FinalizeableObjectQueued](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-finalizeableobjectqueued-method.md) méthode pour décrire le finaliseur pour un objet.</span><span class="sxs-lookup"><span data-stu-id="470a9-110">The `COR_PRF_FINALIZER_FLAGS` enumeration is used by the [ICorProfilerCallback2::FinalizeableObjectQueued](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-finalizeableobjectqueued-method.md) method to describe the finalizer for an object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="470a9-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="470a9-111">Requirements</span></span>  
 <span data-ttu-id="470a9-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="470a9-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="470a9-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="470a9-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="470a9-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="470a9-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="470a9-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="470a9-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="470a9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="470a9-116">See also</span></span>

- [<span data-ttu-id="470a9-117">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="470a9-117">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
