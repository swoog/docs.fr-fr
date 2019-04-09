---
title: CorDebugCreateProcessFlags, énumération
ms.date: 03/30/2017
api_name:
- CorDebugCreateProcessFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugCreateProcessFlags
helpviewer_keywords:
- CorDebugCreateProcessFlags enumeration [.NET Framework debugging]
ms.assetid: e709acce-6a17-4346-b38a-467dba567358
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ae3ba480e208762f5a80f9f1b78dd008f02b6df4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59089376"
---
# <a name="cordebugcreateprocessflags-enumeration"></a><span data-ttu-id="9a4dc-102">CorDebugCreateProcessFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="9a4dc-102">CorDebugCreateProcessFlags Enumeration</span></span>
<span data-ttu-id="9a4dc-103">Fournit des options de débogage supplémentaires qui peuvent être utilisées dans un appel à la [ICorDebug::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="9a4dc-103">Provides additional debugging options that can be used in a call to the [ICorDebug::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a4dc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a4dc-104">Syntax</span></span>  
  
```  
typedef enum CorDebugCreateProcessFlags {  
    DEBUG_NO_SPECIAL_OPTIONS    = 0x0000  
} CorDebugCreateProcessFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="9a4dc-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9a4dc-105">Members</span></span>  
  
|<span data-ttu-id="9a4dc-106">Membre</span><span class="sxs-lookup"><span data-stu-id="9a4dc-106">Member</span></span>|<span data-ttu-id="9a4dc-107">Description</span><span class="sxs-lookup"><span data-stu-id="9a4dc-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_NO_SPECIAL_OPTIONS`|<span data-ttu-id="9a4dc-108">Sans options spéciales sont définies.</span><span class="sxs-lookup"><span data-stu-id="9a4dc-108">No special options are set.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9a4dc-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a4dc-109">Requirements</span></span>  
 <span data-ttu-id="9a4dc-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9a4dc-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9a4dc-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9a4dc-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9a4dc-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9a4dc-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="9a4dc-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="9a4dc-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="9a4dc-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a4dc-114">See also</span></span>

- [<span data-ttu-id="9a4dc-115">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="9a4dc-115">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
