---
title: COR_GC_THREAD_STATS_TYPES (énumération)
ms.date: 03/30/2017
api_name:
- COR_GC_THREAD_STATS_TYPES
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_GC_THREAD_STATS_TYPES
helpviewer_keywords:
- COR_GC_THREAD_STATS_TYPES enumeration [.NET Framework hosting]
ms.assetid: aa227704-0ab1-4b08-aee2-1f439762162e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c631a0a3abb3cb2a342dfd44fdffb147b742ae3c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59212464"
---
# <a name="corgcthreadstatstypes-enumeration"></a><span data-ttu-id="01411-102">COR_GC_THREAD_STATS_TYPES (énumération)</span><span class="sxs-lookup"><span data-stu-id="01411-102">COR_GC_THREAD_STATS_TYPES Enumeration</span></span>
<span data-ttu-id="01411-103">Indique les statistiques de garbage collection pour un thread.</span><span class="sxs-lookup"><span data-stu-id="01411-103">Indicates the garbage collection statistics for a thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="01411-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01411-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_GC_THREAD_HAS_PROMOTED_BYTES  = 0x00000001  
} COR_GC_THREAD_STATS_TYPES;  
```  
  
## <a name="members"></a><span data-ttu-id="01411-105">Membres</span><span class="sxs-lookup"><span data-stu-id="01411-105">Members</span></span>  
  
|<span data-ttu-id="01411-106">Membre</span><span class="sxs-lookup"><span data-stu-id="01411-106">Member</span></span>|<span data-ttu-id="01411-107">Description</span><span class="sxs-lookup"><span data-stu-id="01411-107">Description</span></span>|  
|------------|-----------------|  
|`COR_GC_THREAD_HAS_PROMOTED_BYTES`|<span data-ttu-id="01411-108">Le thread a octets qui ont été promus dans le garbage collection le plus récent.</span><span class="sxs-lookup"><span data-stu-id="01411-108">The thread has bytes that were promoted in the most recent garbage collection.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="01411-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01411-109">Requirements</span></span>  
 <span data-ttu-id="01411-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="01411-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="01411-111">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="01411-111">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 **<span data-ttu-id="01411-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="01411-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="01411-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01411-113">See also</span></span>

- [<span data-ttu-id="01411-114">Énumérations d'hébergement</span><span class="sxs-lookup"><span data-stu-id="01411-114">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
