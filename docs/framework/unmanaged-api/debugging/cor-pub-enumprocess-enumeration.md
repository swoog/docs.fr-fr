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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59089405"
---
# <a name="corpubenumprocess-enumeration"></a><span data-ttu-id="a5fa8-102">COR_PUB_ENUMPROCESS, énumération</span><span class="sxs-lookup"><span data-stu-id="a5fa8-102">COR_PUB_ENUMPROCESS Enumeration</span></span>
<span data-ttu-id="a5fa8-103">Identifie le type de processus à énumérer.</span><span class="sxs-lookup"><span data-stu-id="a5fa8-103">Identifies the type of process to be enumerated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a5fa8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5fa8-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PUB_MANAGEDONLY    = 0x00000001  
} COR_PUB_ENUMPROCESS;  
```  
  
## <a name="members"></a><span data-ttu-id="a5fa8-105">Membres</span><span class="sxs-lookup"><span data-stu-id="a5fa8-105">Members</span></span>  
  
|<span data-ttu-id="a5fa8-106">Nom de membre</span><span class="sxs-lookup"><span data-stu-id="a5fa8-106">Member name</span></span>|<span data-ttu-id="a5fa8-107">Description</span><span class="sxs-lookup"><span data-stu-id="a5fa8-107">Description</span></span>|  
|-----------------|-----------------|  
|`COR_PUB_MANAGEDONLY`|<span data-ttu-id="a5fa8-108">Un processus managé.</span><span class="sxs-lookup"><span data-stu-id="a5fa8-108">A managed process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a5fa8-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a5fa8-109">Remarks</span></span>  
 <span data-ttu-id="a5fa8-110">La version actuelle de l’API de débogage non managé énumère uniquement les processus managés.</span><span class="sxs-lookup"><span data-stu-id="a5fa8-110">The current version of the unmanaged debugging API enumerates only managed processes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a5fa8-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5fa8-111">Requirements</span></span>  
 <span data-ttu-id="a5fa8-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a5fa8-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a5fa8-113">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="a5fa8-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="a5fa8-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a5fa8-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="a5fa8-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="a5fa8-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a5fa8-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5fa8-116">See also</span></span>

- [<span data-ttu-id="a5fa8-117">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="a5fa8-117">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
