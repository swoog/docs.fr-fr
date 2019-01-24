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
ms.openlocfilehash: bfc576e1b4f0bf1666dcd585a24dbfa398e9abde
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715853"
---
# <a name="corpubenumprocess-enumeration"></a><span data-ttu-id="36416-102">COR_PUB_ENUMPROCESS, énumération</span><span class="sxs-lookup"><span data-stu-id="36416-102">COR_PUB_ENUMPROCESS Enumeration</span></span>
<span data-ttu-id="36416-103">Identifie le type de processus à énumérer.</span><span class="sxs-lookup"><span data-stu-id="36416-103">Identifies the type of process to be enumerated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="36416-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36416-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PUB_MANAGEDONLY    = 0x00000001  
} COR_PUB_ENUMPROCESS;  
```  
  
## <a name="members"></a><span data-ttu-id="36416-105">Membres</span><span class="sxs-lookup"><span data-stu-id="36416-105">Members</span></span>  
  
|<span data-ttu-id="36416-106">Nom de membre</span><span class="sxs-lookup"><span data-stu-id="36416-106">Member name</span></span>|<span data-ttu-id="36416-107">Description</span><span class="sxs-lookup"><span data-stu-id="36416-107">Description</span></span>|  
|-----------------|-----------------|  
|`COR_PUB_MANAGEDONLY`|<span data-ttu-id="36416-108">Un processus managé.</span><span class="sxs-lookup"><span data-stu-id="36416-108">A managed process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="36416-109">Notes</span><span class="sxs-lookup"><span data-stu-id="36416-109">Remarks</span></span>  
 <span data-ttu-id="36416-110">La version actuelle de l’API de débogage non managé énumère uniquement les processus managés.</span><span class="sxs-lookup"><span data-stu-id="36416-110">The current version of the unmanaged debugging API enumerates only managed processes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="36416-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="36416-111">Requirements</span></span>  
 <span data-ttu-id="36416-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="36416-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="36416-113">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="36416-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="36416-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="36416-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="36416-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="36416-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="36416-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36416-116">See also</span></span>
- [<span data-ttu-id="36416-117">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="36416-117">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
