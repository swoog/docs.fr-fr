---
title: COR_PRF_STATIC_TYPE, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_STATIC_TYPE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_STATIC_TYPE
helpviewer_keywords:
- COR_PRF_STATIC_TYPE enumeration [.NET Framework profiling]
ms.assetid: 441d7809-5b65-41a5-ba64-2910a8008315
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 34a2ca5b505c504115af47402c3d92a05ec0676f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54737631"
---
# <a name="corprfstatictype-enumeration"></a><span data-ttu-id="92b60-102">COR_PRF_STATIC_TYPE, énumération</span><span class="sxs-lookup"><span data-stu-id="92b60-102">COR_PRF_STATIC_TYPE Enumeration</span></span>
<span data-ttu-id="92b60-103">Indique si un champ est statique et si oui, la qualité statique qui s'y applique.</span><span class="sxs-lookup"><span data-stu-id="92b60-103">Indicates whether a field is static and, if so, the static quality that applies to the field.</span></span> <span data-ttu-id="92b60-104">Ces valeurs peuvent être combinées à l’aide de l’opération OR au niveau du bit pour indiquer que le champ a plusieurs qualités statiques différentes.</span><span class="sxs-lookup"><span data-stu-id="92b60-104">These values can be combined using the bitwise OR operation to indicate that the field has multiple, different static qualities.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="92b60-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92b60-105">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_FIELD_NOT_A_STATIC = 0x0,  
    COR_PRF_FIELD_APP_DOMAIN_STATIC = 0x1,  
    COR_PRF_FIELD_THREAD_STATIC = 0x2,  
    COR_PRF_FIELD_CONTEXT_STATIC = 0x4,  
    COR_PRF_FIELD_RVA_STATIC = 0x8  
} COR_PRF_STATIC_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="92b60-106">Membres</span><span class="sxs-lookup"><span data-stu-id="92b60-106">Members</span></span>  
  
|<span data-ttu-id="92b60-107">Membre</span><span class="sxs-lookup"><span data-stu-id="92b60-107">Member</span></span>|<span data-ttu-id="92b60-108">Description</span><span class="sxs-lookup"><span data-stu-id="92b60-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_FIELD_NOT_A_STATIC`|<span data-ttu-id="92b60-109">Le champ n’est pas statique.</span><span class="sxs-lookup"><span data-stu-id="92b60-109">The field is not static.</span></span>|  
|`COR_PRF_FIELD_APP_DOMAIN_STATIC`|<span data-ttu-id="92b60-110">Le champ est statique de domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="92b60-110">The field is application domain-static.</span></span>|  
|`COR_PRF_FIELD_THREAD_STATIC`|<span data-ttu-id="92b60-111">Le champ est thread-static.</span><span class="sxs-lookup"><span data-stu-id="92b60-111">The field is thread-static.</span></span>|  
|`COR_PRF_FIELD_CONTEXT_STATIC`|<span data-ttu-id="92b60-112">Le champ est statique de contexte.</span><span class="sxs-lookup"><span data-stu-id="92b60-112">The field is context-static.</span></span>|  
|`COR_PRF_FIELD_RVA_STATIC`|<span data-ttu-id="92b60-113">Le champ est l’adresse virtuelle relative (RVA)-statique.</span><span class="sxs-lookup"><span data-stu-id="92b60-113">The field is relative virtual address (RVA)-static.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="92b60-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="92b60-114">Requirements</span></span>  
 <span data-ttu-id="92b60-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="92b60-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="92b60-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="92b60-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="92b60-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="92b60-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="92b60-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="92b60-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="92b60-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92b60-119">See also</span></span>
- [<span data-ttu-id="92b60-120">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="92b60-120">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
