---
title: COR_GC_STAT_TYPES (énumération)
ms.date: 03/30/2017
api_name:
- COR_GC_STAT_TYPES
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_GC_STAT_TYPES
helpviewer_keywords:
- COR_GC_STAT_TYPES enumeration [.NET Framework hosting]
ms.assetid: fc51d6db-f7f8-408b-b93d-c166fc712c99
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4bd12feb47352d9bb78aa8ef056072f9bdc6fba3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710324"
---
# <a name="corgcstattypes-enumeration"></a><span data-ttu-id="16a1f-102">COR_GC_STAT_TYPES (énumération)</span><span class="sxs-lookup"><span data-stu-id="16a1f-102">COR_GC_STAT_TYPES Enumeration</span></span>
<span data-ttu-id="16a1f-103">Spécifie les statistiques à enregistrer pour un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="16a1f-103">Specifies the statistics to be recorded for a garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="16a1f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16a1f-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_GC_COUNTS                 = 0x00000001  
    COR_GC_MEMORYUSAGE            = 0x00000002  
} COR_GC_STAT_TYPES;  
```  
  
## <a name="remarks"></a><span data-ttu-id="16a1f-105">Notes</span><span class="sxs-lookup"><span data-stu-id="16a1f-105">Remarks</span></span>  
 <span data-ttu-id="16a1f-106">Cette énumération spécifie les statistiques de la [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) structure doivent être définis [ICLRGCManager::GetStats](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager-getstats-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="16a1f-106">This enumeration specifies which statistics in the [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) structure are to be set by [ICLRGCManager::GetStats](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager-getstats-method.md) method.</span></span>  
  
## <a name="members"></a><span data-ttu-id="16a1f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="16a1f-107">Members</span></span>  
  
|<span data-ttu-id="16a1f-108">Membre</span><span class="sxs-lookup"><span data-stu-id="16a1f-108">Member</span></span>|<span data-ttu-id="16a1f-109">Description</span><span class="sxs-lookup"><span data-stu-id="16a1f-109">Description</span></span>|  
|------------|-----------------|  
|`COR_GC_COUNTS`|<span data-ttu-id="16a1f-110">Enregistre le nombre de garbage collections effectué pour chaque génération.</span><span class="sxs-lookup"><span data-stu-id="16a1f-110">Records the number of garbage collections performed for each generation.</span></span>|  
|`COR_GC_MEMORYUSAGE`|<span data-ttu-id="16a1f-111">Enregistre l’utilisation et le garbage collection taille statistiques de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="16a1f-111">Records memory usage and garbage collection size statistics.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="16a1f-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="16a1f-112">Requirements</span></span>  
 <span data-ttu-id="16a1f-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="16a1f-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="16a1f-114">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="16a1f-114">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="16a1f-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="16a1f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="16a1f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16a1f-116">See also</span></span>
- [<span data-ttu-id="16a1f-117">COR_GC_STATS, structure</span><span class="sxs-lookup"><span data-stu-id="16a1f-117">COR_GC_STATS Structure</span></span>](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md)
- [<span data-ttu-id="16a1f-118">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="16a1f-118">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
