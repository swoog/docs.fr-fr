---
title: COR_PRF_GC_REASON, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_GC_REASON
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_GC_REASON
helpviewer_keywords:
- COR_PRF_GC_REASON enumeration [.NET Framework profiling]
ms.assetid: 72822b95-a7fb-485e-9d55-1cb016d9a458
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 13740920e8db5d44b71cd3c324742945c64b3e59
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498958"
---
# <a name="corprfgcreason-enumeration"></a><span data-ttu-id="a1824-102">COR_PRF_GC_REASON, énumération</span><span class="sxs-lookup"><span data-stu-id="a1824-102">COR_PRF_GC_REASON Enumeration</span></span>
<span data-ttu-id="a1824-103">Indique la raison pour laquelle une récupération de mémoire se produit.</span><span class="sxs-lookup"><span data-stu-id="a1824-103">Indicates the reason that garbage collection is occurring.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1824-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1824-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_GC_INDUCED = 1,  
    COR_PRF_GC_OTHER = 0  
} COR_PRF_GC_REASON;  
```  
  
## <a name="members"></a><span data-ttu-id="a1824-105">Membres</span><span class="sxs-lookup"><span data-stu-id="a1824-105">Members</span></span>  
  
|<span data-ttu-id="a1824-106">Membre</span><span class="sxs-lookup"><span data-stu-id="a1824-106">Member</span></span>|<span data-ttu-id="a1824-107">Description</span><span class="sxs-lookup"><span data-stu-id="a1824-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_GC_INDUCED`|<span data-ttu-id="a1824-108">Le garbage collection a été induit par une <xref:System.GC.Collect%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="a1824-108">The garbage collection was induced by a <xref:System.GC.Collect%2A> method.</span></span>|  
|`COR_PRF_GC_OTHER`|<span data-ttu-id="a1824-109">La raison n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a1824-109">The reason is unspecified.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a1824-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a1824-110">Requirements</span></span>  
 <span data-ttu-id="a1824-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a1824-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1824-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a1824-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a1824-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a1824-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a1824-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1824-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1824-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1824-115">See also</span></span>
- [<span data-ttu-id="a1824-116">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="a1824-116">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
