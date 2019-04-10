---
title: CorDebugHandleType, énumération
ms.date: 03/30/2017
api_name:
- CorDebugHandleType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugHandleType
helpviewer_keywords:
- CorDebugHandleType enumeration [.NET Framework debugging]
ms.assetid: 84296b55-c2c5-424c-ac9c-8e28e2895945
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 513fc93bdac71e2a3ba59ebb53fdde44f1659af5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59220459"
---
# <a name="cordebughandletype-enumeration"></a><span data-ttu-id="0f512-102">CorDebugHandleType, énumération</span><span class="sxs-lookup"><span data-stu-id="0f512-102">CorDebugHandleType Enumeration</span></span>
<span data-ttu-id="0f512-103">Indique le type de handle.</span><span class="sxs-lookup"><span data-stu-id="0f512-103">Indicates the handle type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f512-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f512-104">Syntax</span></span>  
  
```  
typedef enum CorDebugHandleType {  
    HANDLE_STRONG                  = 1,  
    HANDLE_WEAK_TRACK_RESURRECTION = 2  
} CorDebugHandleType;  
```  
  
## <a name="members"></a><span data-ttu-id="0f512-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0f512-105">Members</span></span>  
  
|<span data-ttu-id="0f512-106">Membre</span><span class="sxs-lookup"><span data-stu-id="0f512-106">Member</span></span>|<span data-ttu-id="0f512-107">Description</span><span class="sxs-lookup"><span data-stu-id="0f512-107">Description</span></span>|  
|------------|-----------------|  
|`HANDLE_STRONG`|<span data-ttu-id="0f512-108">Le handle est fort, ce qui empêche un objet d’être récupéré par le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="0f512-108">The handle is strong, which prevents an object from being reclaimed by garbage collection.</span></span>|  
|`HANDLE_WEAK_TRACK_RESURRECTION`|<span data-ttu-id="0f512-109">Le handle est faible, ce qui n’empêche pas un objet d’être récupéré par le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="0f512-109">The handle is weak, which does not prevent an object from being reclaimed by garbage collection.</span></span><br /><br /> <span data-ttu-id="0f512-110">Le handle n’est plus valide lorsque l’objet est collecté.</span><span class="sxs-lookup"><span data-stu-id="0f512-110">The handle becomes invalid when the object is collected.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0f512-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f512-111">Requirements</span></span>  
 <span data-ttu-id="0f512-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0f512-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f512-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0f512-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0f512-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0f512-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="0f512-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0f512-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0f512-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f512-116">See also</span></span>

- [<span data-ttu-id="0f512-117">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="0f512-117">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
