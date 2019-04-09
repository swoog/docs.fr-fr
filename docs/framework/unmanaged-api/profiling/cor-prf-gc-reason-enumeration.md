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
ms.openlocfilehash: daf97f25b1adc30b173fcd81812a4b197915cdd1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59196942"
---
# <a name="corprfgcreason-enumeration"></a><span data-ttu-id="9be1b-102">COR_PRF_GC_REASON, énumération</span><span class="sxs-lookup"><span data-stu-id="9be1b-102">COR_PRF_GC_REASON Enumeration</span></span>
<span data-ttu-id="9be1b-103">Indique la raison pour laquelle une récupération de mémoire se produit.</span><span class="sxs-lookup"><span data-stu-id="9be1b-103">Indicates the reason that garbage collection is occurring.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9be1b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9be1b-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_GC_INDUCED = 1,  
    COR_PRF_GC_OTHER = 0  
} COR_PRF_GC_REASON;  
```  
  
## <a name="members"></a><span data-ttu-id="9be1b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9be1b-105">Members</span></span>  
  
|<span data-ttu-id="9be1b-106">Membre</span><span class="sxs-lookup"><span data-stu-id="9be1b-106">Member</span></span>|<span data-ttu-id="9be1b-107">Description</span><span class="sxs-lookup"><span data-stu-id="9be1b-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_GC_INDUCED`|<span data-ttu-id="9be1b-108">Le garbage collection a été induit par une <xref:System.GC.Collect%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="9be1b-108">The garbage collection was induced by a <xref:System.GC.Collect%2A> method.</span></span>|  
|`COR_PRF_GC_OTHER`|<span data-ttu-id="9be1b-109">La raison n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9be1b-109">The reason is unspecified.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9be1b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9be1b-110">Requirements</span></span>  
 <span data-ttu-id="9be1b-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9be1b-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9be1b-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="9be1b-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="9be1b-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9be1b-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="9be1b-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="9be1b-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="9be1b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9be1b-115">See also</span></span>

- [<span data-ttu-id="9be1b-116">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="9be1b-116">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
