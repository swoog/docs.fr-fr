---
title: COR_GC_THREAD_STATS, structure
ms.date: 03/30/2017
api_name:
- COR_GC_THREAD_STATS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_GC_THREAD_STATS
helpviewer_keywords:
- COR_GC_THREAD_STATS structure [.NET Framework hosting]
ms.assetid: 01f9a59b-7679-4d42-9ced-4a8981625c3d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f60a4b56270318a05d0e5a480fdb56eb45593d5e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59177734"
---
# <a name="corgcthreadstats-structure"></a><span data-ttu-id="53aa1-102">COR_GC_THREAD_STATS, structure</span><span class="sxs-lookup"><span data-stu-id="53aa1-102">COR_GC_THREAD_STATS Structure</span></span>
<span data-ttu-id="53aa1-103">Contient des statistiques par thread relatives au garbage collection.</span><span class="sxs-lookup"><span data-stu-id="53aa1-103">Contains per-thread statistics pertaining to garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53aa1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53aa1-104">Syntax</span></span>  
  
```  
typedef struct _COR_GC_THREAD_STATS {  
    ULONGLONG  PerThreadAllocation;   
    ULONG      Flags;   
} COR_GC_THREAD_STATS;  
```  
  
## <a name="members"></a><span data-ttu-id="53aa1-105">Membres</span><span class="sxs-lookup"><span data-stu-id="53aa1-105">Members</span></span>  
  
|<span data-ttu-id="53aa1-106">Membre</span><span class="sxs-lookup"><span data-stu-id="53aa1-106">Member</span></span>|<span data-ttu-id="53aa1-107">Description</span><span class="sxs-lookup"><span data-stu-id="53aa1-107">Description</span></span>|  
|------------|-----------------|  
|`PerThreadAllocation`|<span data-ttu-id="53aa1-108">Le nombre d’octets de mémoire allouée sur le thread qui est associé à l’actuel `COR_GC_THREAD_STATS` instance.</span><span class="sxs-lookup"><span data-stu-id="53aa1-108">The number of bytes of memory allocated on the thread that is associated with the current `COR_GC_THREAD_STATS` instance.</span></span> <span data-ttu-id="53aa1-109">Ce nombre est remis à zéro à chaque fois qu'un zéro de la génération de garbage collection se produit.</span><span class="sxs-lookup"><span data-stu-id="53aa1-109">This number is cleared to zero each time a generation-zero garbage collection occurs.</span></span>|  
|`Flags`|<span data-ttu-id="53aa1-110">Le nombre d’octets promus à une génération supérieure garbage collection le plus récent.</span><span class="sxs-lookup"><span data-stu-id="53aa1-110">The number of bytes promoted to a higher generation at the most recent garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="53aa1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="53aa1-111">Remarks</span></span>  
 <span data-ttu-id="53aa1-112">[ICLRTask::GetMemStats](../../../../docs/framework/unmanaged-api/hosting/iclrtask-getmemstats-method.md) prend un paramètre de sortie de type `COR_GC_THREAD_STATS`.</span><span class="sxs-lookup"><span data-stu-id="53aa1-112">[ICLRTask::GetMemStats](../../../../docs/framework/unmanaged-api/hosting/iclrtask-getmemstats-method.md) takes an output parameter of type `COR_GC_THREAD_STATS`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="53aa1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53aa1-113">Requirements</span></span>  
 <span data-ttu-id="53aa1-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="53aa1-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="53aa1-115">**En-tête :** GCHost.idl</span><span class="sxs-lookup"><span data-stu-id="53aa1-115">**Header:** GCHost.idl</span></span>  
  
 <span data-ttu-id="53aa1-116">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="53aa1-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="53aa1-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="53aa1-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="53aa1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53aa1-118">See also</span></span>

- [<span data-ttu-id="53aa1-119">Structures d'hébergement</span><span class="sxs-lookup"><span data-stu-id="53aa1-119">Hosting Structures</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)
- [<span data-ttu-id="53aa1-120">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="53aa1-120">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
