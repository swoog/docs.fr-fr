---
title: COR_PRF_MISC, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_MISC
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_MISC
helpviewer_keywords:
- COR_PRF_MISC enumeration [.NET Framework profiling]
ms.assetid: 619bb5de-e309-48b6-a3af-32d935a0ff46
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3b40ac5f49288f7b30018e0c8c727e3ce6b73ae8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61599193"
---
# <a name="corprfmisc-enumeration"></a><span data-ttu-id="e8ffe-102">COR_PRF_MISC, énumération</span><span class="sxs-lookup"><span data-stu-id="e8ffe-102">COR_PRF_MISC Enumeration</span></span>
<span data-ttu-id="e8ffe-103">Contient des valeurs de constante qui spécifient des identificateurs spéciaux.</span><span class="sxs-lookup"><span data-stu-id="e8ffe-103">Contains constant values that specify special identifiers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8ffe-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8ffe-104">Syntax</span></span>  
  
```  
typedef enum {  
    PROFILER_PARENT_UNKNOWN = 0xFFFFFFFD,  
    PROFILER_GLOBAL_CLASS   = 0xFFFFFFFE,  
    PROFILER_GLOBAL_MODULE  = 0xFFFFFFFF  
} COR_PRF_MISC;  
```  
  
## <a name="members"></a><span data-ttu-id="e8ffe-105">Membres</span><span class="sxs-lookup"><span data-stu-id="e8ffe-105">Members</span></span>  
  
|<span data-ttu-id="e8ffe-106">Membre</span><span class="sxs-lookup"><span data-stu-id="e8ffe-106">Member</span></span>|<span data-ttu-id="e8ffe-107">Description</span><span class="sxs-lookup"><span data-stu-id="e8ffe-107">Description</span></span>|  
|------------|-----------------|  
|`PROFILER_PARENT_UNKNOWN`|<span data-ttu-id="e8ffe-108">L’identificateur par défaut utilisé par [ICorProfilerInfo::GetModuleInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getmoduleinfo-method.md) pour un module qui n’a pas encore été attaché à un assembly.</span><span class="sxs-lookup"><span data-stu-id="e8ffe-108">The default identifier used by [ICorProfilerInfo::GetModuleInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getmoduleinfo-method.md) for a module that has not yet been attached to an assembly.</span></span>|  
|`PROFILER_GLOBAL_CLASS`|<span data-ttu-id="e8ffe-109">L’identificateur de classe par défaut pour les constantes globales qui n’appartiennent pas à une classe.</span><span class="sxs-lookup"><span data-stu-id="e8ffe-109">The default class identifier for global constants that do not belong to a class.</span></span>|  
|`PROFILER_GLOBAL_MODULE`|<span data-ttu-id="e8ffe-110">L’identificateur de module par défaut pour les objets globaux qui n’appartiennent pas à un module.</span><span class="sxs-lookup"><span data-stu-id="e8ffe-110">The default module identifier for global objects that do not belong to a module.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e8ffe-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8ffe-111">Requirements</span></span>  
 <span data-ttu-id="e8ffe-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e8ffe-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8ffe-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e8ffe-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e8ffe-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e8ffe-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e8ffe-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8ffe-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8ffe-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8ffe-116">See also</span></span>

- [<span data-ttu-id="e8ffe-117">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="e8ffe-117">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
