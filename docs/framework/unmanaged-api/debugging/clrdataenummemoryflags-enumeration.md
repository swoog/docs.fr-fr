---
title: CLRDataEnumMemoryFlags, énumération
ms.date: 03/30/2017
api_name:
- CLRDataEnumMemoryFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CLRDataEnumMemoryFlags
helpviewer_keywords:
- CLRDataEnumMemoryFlags enumeration [.NET Framework debugging]
ms.assetid: e249f9fc-e24a-4506-903c-92781f6eab7c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 80ea3afef4aee51760e3a2ce6a2b895bca4a6ec5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59224039"
---
# <a name="clrdataenummemoryflags-enumeration"></a><span data-ttu-id="9feb9-102">CLRDataEnumMemoryFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="9feb9-102">CLRDataEnumMemoryFlags Enumeration</span></span>
<span data-ttu-id="9feb9-103">Indique les régions de mémoire un appel à la [ICLRDataEnumMemoryRegions::EnumMemoryRegions](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregions-enummemoryregions-method.md) méthode doit inclure.</span><span class="sxs-lookup"><span data-stu-id="9feb9-103">Indicates which memory regions a call to the [ICLRDataEnumMemoryRegions::EnumMemoryRegions](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregions-enummemoryregions-method.md) method should include.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9feb9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9feb9-104">Syntax</span></span>  
  
```  
typedef enum CLRDataEnumMemoryFlags {  
    CLRDATA_ENUM_MEM_DEFAULT  = 0x0,  
    CLRDATA_ENUM_MEM_MINI     = CLRDATA_ENUM_MEM_DEFAULT,  
    CLRDATA_ENUM_MEM_HEAP     = 0x1  
} CLRDataEnumMemoryFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="9feb9-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9feb9-105">Members</span></span>  
  
|<span data-ttu-id="9feb9-106">Membre</span><span class="sxs-lookup"><span data-stu-id="9feb9-106">Member</span></span>|<span data-ttu-id="9feb9-107">Description</span><span class="sxs-lookup"><span data-stu-id="9feb9-107">Description</span></span>|  
|------------|-----------------|  
|`CLRDATA_ENUM_MEM_DEFAULT`|<span data-ttu-id="9feb9-108">Un minidump, autrement dit, une image mémoire incomplète.</span><span class="sxs-lookup"><span data-stu-id="9feb9-108">A minidump, that is, a sparse memory dump.</span></span>|  
|`CLRDATA_ENUM_MEM_HEAP`|<span data-ttu-id="9feb9-109">Un vidage de tas complètes.</span><span class="sxs-lookup"><span data-stu-id="9feb9-109">A full heap dump.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9feb9-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9feb9-110">Requirements</span></span>  
 <span data-ttu-id="9feb9-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9feb9-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9feb9-112">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="9feb9-112">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="9feb9-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9feb9-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="9feb9-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="9feb9-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="9feb9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9feb9-115">See also</span></span>

- [<span data-ttu-id="9feb9-116">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="9feb9-116">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
