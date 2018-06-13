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
ms.openlocfilehash: 9fdc37676bfae8ac90fde0a7a5b11037b8357e25
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33403755"
---
# <a name="cordebugcreateprocessflags-enumeration"></a><span data-ttu-id="b35f9-102">CorDebugCreateProcessFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="b35f9-102">CorDebugCreateProcessFlags Enumeration</span></span>
<span data-ttu-id="b35f9-103">Fournit des options de débogage supplémentaires qui peuvent être utilisées dans un appel à la [ICorDebug::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="b35f9-103">Provides additional debugging options that can be used in a call to the [ICorDebug::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b35f9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b35f9-104">Syntax</span></span>  
  
```  
typedef enum CorDebugCreateProcessFlags {  
    DEBUG_NO_SPECIAL_OPTIONS    = 0x0000  
} CorDebugCreateProcessFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="b35f9-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b35f9-105">Members</span></span>  
  
|<span data-ttu-id="b35f9-106">Membre</span><span class="sxs-lookup"><span data-stu-id="b35f9-106">Member</span></span>|<span data-ttu-id="b35f9-107">Description</span><span class="sxs-lookup"><span data-stu-id="b35f9-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_NO_SPECIAL_OPTIONS`|<span data-ttu-id="b35f9-108">Sans options spéciales sont définies.</span><span class="sxs-lookup"><span data-stu-id="b35f9-108">No special options are set.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b35f9-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b35f9-109">Requirements</span></span>  
 <span data-ttu-id="b35f9-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b35f9-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b35f9-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b35f9-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b35f9-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b35f9-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b35f9-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b35f9-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b35f9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b35f9-114">See Also</span></span>  
 [<span data-ttu-id="b35f9-115">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="b35f9-115">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
