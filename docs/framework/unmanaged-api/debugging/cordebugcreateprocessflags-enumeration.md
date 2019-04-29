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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61609111"
---
# <a name="cordebugcreateprocessflags-enumeration"></a><span data-ttu-id="c8d39-102">CorDebugCreateProcessFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="c8d39-102">CorDebugCreateProcessFlags Enumeration</span></span>
<span data-ttu-id="c8d39-103">Fournit des options de débogage supplémentaires qui peuvent être utilisées dans un appel à la [ICorDebug::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="c8d39-103">Provides additional debugging options that can be used in a call to the [ICorDebug::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8d39-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8d39-104">Syntax</span></span>  
  
```  
typedef enum CorDebugCreateProcessFlags {  
    DEBUG_NO_SPECIAL_OPTIONS    = 0x0000  
} CorDebugCreateProcessFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="c8d39-105">Membres</span><span class="sxs-lookup"><span data-stu-id="c8d39-105">Members</span></span>  
  
|<span data-ttu-id="c8d39-106">Membre</span><span class="sxs-lookup"><span data-stu-id="c8d39-106">Member</span></span>|<span data-ttu-id="c8d39-107">Description</span><span class="sxs-lookup"><span data-stu-id="c8d39-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_NO_SPECIAL_OPTIONS`|<span data-ttu-id="c8d39-108">Sans options spéciales sont définies.</span><span class="sxs-lookup"><span data-stu-id="c8d39-108">No special options are set.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c8d39-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8d39-109">Requirements</span></span>  
 <span data-ttu-id="c8d39-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c8d39-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c8d39-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c8d39-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c8d39-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c8d39-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c8d39-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c8d39-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c8d39-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8d39-114">See also</span></span>

- [<span data-ttu-id="c8d39-115">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="c8d39-115">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
