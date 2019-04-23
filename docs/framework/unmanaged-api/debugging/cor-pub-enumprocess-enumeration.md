---
title: COR_PUB_ENUMPROCESS, énumération
ms.date: 03/30/2017
api_name:
- COR_PUB_ENUMPROCESS
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_PUB_ENUMPROCESS
helpviewer_keywords:
- COR_PUB_ENUMPROCESS enumeration [.NET Framework debugging]
ms.assetid: 5d3ada6e-feea-47da-a7ed-b664107c137f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 02ff60852a85d003deb68cae96a184ac8d61c65f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59089405"
---
# <a name="corpubenumprocess-enumeration"></a><span data-ttu-id="c17d3-102">COR_PUB_ENUMPROCESS, énumération</span><span class="sxs-lookup"><span data-stu-id="c17d3-102">COR_PUB_ENUMPROCESS Enumeration</span></span>
<span data-ttu-id="c17d3-103">Identifie le type de processus à énumérer.</span><span class="sxs-lookup"><span data-stu-id="c17d3-103">Identifies the type of process to be enumerated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c17d3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c17d3-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PUB_MANAGEDONLY    = 0x00000001  
} COR_PUB_ENUMPROCESS;  
```  
  
## <a name="members"></a><span data-ttu-id="c17d3-105">Membres</span><span class="sxs-lookup"><span data-stu-id="c17d3-105">Members</span></span>  
  
|<span data-ttu-id="c17d3-106">Nom de membre</span><span class="sxs-lookup"><span data-stu-id="c17d3-106">Member name</span></span>|<span data-ttu-id="c17d3-107">Description</span><span class="sxs-lookup"><span data-stu-id="c17d3-107">Description</span></span>|  
|-----------------|-----------------|  
|`COR_PUB_MANAGEDONLY`|<span data-ttu-id="c17d3-108">Un processus managé.</span><span class="sxs-lookup"><span data-stu-id="c17d3-108">A managed process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c17d3-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c17d3-109">Remarks</span></span>  
 <span data-ttu-id="c17d3-110">La version actuelle de l’API de débogage non managé énumère uniquement les processus managés.</span><span class="sxs-lookup"><span data-stu-id="c17d3-110">The current version of the unmanaged debugging API enumerates only managed processes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c17d3-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c17d3-111">Requirements</span></span>  
 <span data-ttu-id="c17d3-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c17d3-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c17d3-113">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="c17d3-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="c17d3-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c17d3-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c17d3-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c17d3-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c17d3-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c17d3-116">See also</span></span>

- [<span data-ttu-id="c17d3-117">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="c17d3-117">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
