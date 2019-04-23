---
title: COR_PRF_GC_ROOT_KIND, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_GC_ROOT_KIND
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_GC_ROOT_KIND
helpviewer_keywords:
- COR_PRF_GC_ROOT_KIND enumeration [.NET Framework profiling]
ms.assetid: b9fb1c03-417f-41d4-aed4-02cb4ade8def
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7dfbba3cef8afadfc6e12e53ea328c4fc7165ca0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59206757"
---
# <a name="corprfgcrootkind-enumeration"></a><span data-ttu-id="71dfa-102">COR_PRF_GC_ROOT_KIND, énumération</span><span class="sxs-lookup"><span data-stu-id="71dfa-102">COR_PRF_GC_ROOT_KIND Enumeration</span></span>
<span data-ttu-id="71dfa-103">Indique le type de racine de garbage collection qui est exposé par le [ICorProfilerCallback2::RootReferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-rootreferences2-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="71dfa-103">Indicates the kind of garbage collection root that is exposed by the [ICorProfilerCallback2::RootReferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-rootreferences2-method.md) callback.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="71dfa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71dfa-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_GC_ROOT_STACK = 1,  
    COR_PRF_GC_ROOT_FINALIZER = 2,  
    COR_PRF_GC_ROOT_HANDLE = 3,  
    COR_PRF_GC_ROOT_OTHER = 0  
} COR_PRF_GC_ROOT_KIND;  
```  
  
## <a name="members"></a><span data-ttu-id="71dfa-105">Membres</span><span class="sxs-lookup"><span data-stu-id="71dfa-105">Members</span></span>  
  
|<span data-ttu-id="71dfa-106">Membre</span><span class="sxs-lookup"><span data-stu-id="71dfa-106">Member</span></span>|<span data-ttu-id="71dfa-107">Description</span><span class="sxs-lookup"><span data-stu-id="71dfa-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_GC_ROOT_STACK`|<span data-ttu-id="71dfa-108">La racine est une variable sur la pile.</span><span class="sxs-lookup"><span data-stu-id="71dfa-108">The root is a variable on the stack.</span></span>|  
|`COR_PRF_GC_ROOT_FINALIZER`|<span data-ttu-id="71dfa-109">La racine est une entrée dans la file d’attente du finaliseur.</span><span class="sxs-lookup"><span data-stu-id="71dfa-109">The root is an entry in the finalizer queue.</span></span>|  
|`COR_PRF_GC_ROOT_HANDLE`|<span data-ttu-id="71dfa-110">La racine est un handle de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="71dfa-110">The root is a garbage collection handle.</span></span>|  
|`COR_PRF_GC_ROOT_OTHER`|<span data-ttu-id="71dfa-111">Le type de racine n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="71dfa-111">The kind of root is unspecified.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="71dfa-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71dfa-112">Requirements</span></span>  
 <span data-ttu-id="71dfa-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="71dfa-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="71dfa-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="71dfa-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="71dfa-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="71dfa-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="71dfa-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="71dfa-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71dfa-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71dfa-117">See also</span></span>

- [<span data-ttu-id="71dfa-118">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="71dfa-118">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
