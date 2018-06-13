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
ms.openlocfilehash: 24a386fe82bbd004954924a573c090af7f58824a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431826"
---
# <a name="corgcthreadstats-structure"></a><span data-ttu-id="7d7f7-102">COR_GC_THREAD_STATS, structure</span><span class="sxs-lookup"><span data-stu-id="7d7f7-102">COR_GC_THREAD_STATS Structure</span></span>
<span data-ttu-id="7d7f7-103">Contient des statistiques par thread concernant le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="7d7f7-103">Contains per-thread statistics pertaining to garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d7f7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d7f7-104">Syntax</span></span>  
  
```  
typedef struct _COR_GC_THREAD_STATS {  
    ULONGLONG  PerThreadAllocation;   
    ULONG      Flags;   
} COR_GC_THREAD_STATS;  
```  
  
## <a name="members"></a><span data-ttu-id="7d7f7-105">Membres</span><span class="sxs-lookup"><span data-stu-id="7d7f7-105">Members</span></span>  
  
|<span data-ttu-id="7d7f7-106">Membre</span><span class="sxs-lookup"><span data-stu-id="7d7f7-106">Member</span></span>|<span data-ttu-id="7d7f7-107">Description</span><span class="sxs-lookup"><span data-stu-id="7d7f7-107">Description</span></span>|  
|------------|-----------------|  
|`PerThreadAllocation`|<span data-ttu-id="7d7f7-108">Le nombre d’octets de mémoire alloués sur le thread qui est associé à l’actuel `COR_GC_THREAD_STATS` instance.</span><span class="sxs-lookup"><span data-stu-id="7d7f7-108">The number of bytes of memory allocated on the thread that is associated with the current `COR_GC_THREAD_STATS` instance.</span></span> <span data-ttu-id="7d7f7-109">Ce nombre est remis à zéro chaque fois qu'un nettoyage de la génération zéro se produit.</span><span class="sxs-lookup"><span data-stu-id="7d7f7-109">This number is cleared to zero each time a generation-zero garbage collection occurs.</span></span>|  
|`Flags`|<span data-ttu-id="7d7f7-110">Le nombre d’octets promus à une génération supérieure garbage collection le plus récent.</span><span class="sxs-lookup"><span data-stu-id="7d7f7-110">The number of bytes promoted to a higher generation at the most recent garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7d7f7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7d7f7-111">Remarks</span></span>  
 <span data-ttu-id="7d7f7-112">[ICLRTask::GetMemStats](../../../../docs/framework/unmanaged-api/hosting/iclrtask-getmemstats-method.md) prend un paramètre de sortie de type `COR_GC_THREAD_STATS`.</span><span class="sxs-lookup"><span data-stu-id="7d7f7-112">[ICLRTask::GetMemStats](../../../../docs/framework/unmanaged-api/hosting/iclrtask-getmemstats-method.md) takes an output parameter of type `COR_GC_THREAD_STATS`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7d7f7-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7d7f7-113">Requirements</span></span>  
 <span data-ttu-id="7d7f7-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7d7f7-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7d7f7-115">**En-tête :** GCHost.idl</span><span class="sxs-lookup"><span data-stu-id="7d7f7-115">**Header:** GCHost.idl</span></span>  
  
 <span data-ttu-id="7d7f7-116">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7d7f7-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7d7f7-117">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7d7f7-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d7f7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d7f7-118">See Also</span></span>  
 [<span data-ttu-id="7d7f7-119">Structures d’hébergement</span><span class="sxs-lookup"><span data-stu-id="7d7f7-119">Hosting Structures</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)  
 [<span data-ttu-id="7d7f7-120">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="7d7f7-120">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
