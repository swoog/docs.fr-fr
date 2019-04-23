---
title: CorDebugJITCompilerFlagsDeprecated, énumération
ms.date: 03/30/2017
api_name:
- CorDebugJITCompilerFlagsDeprecated
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugJITCompilerFlagsDeprecated
helpviewer_keywords:
- CorDebugJITCompilerFlagsDeprecated enumeration [.NET Framework debugging]
ms.assetid: af15e2ca-6be1-472b-bd36-03644a1e3ddd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7f15a4557be0dc633fb9ecda5916896e340f00da
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59136888"
---
# <a name="cordebugjitcompilerflagsdeprecated-enumeration"></a><span data-ttu-id="84a56-102">CorDebugJITCompilerFlagsDeprecated, énumération</span><span class="sxs-lookup"><span data-stu-id="84a56-102">CorDebugJITCompilerFlagsDeprecated Enumeration</span></span>
<span data-ttu-id="84a56-103">Cette énumération est obsolète.</span><span class="sxs-lookup"><span data-stu-id="84a56-103">This enumeration is obsolete.</span></span> <span data-ttu-id="84a56-104">Utilisez le `CORDEBUG_JIT_DEFAULT` membre de la [CorDebugJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md) énumération à la place.</span><span class="sxs-lookup"><span data-stu-id="84a56-104">Use the `CORDEBUG_JIT_DEFAULT` member of the [CorDebugJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md) enumeration instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84a56-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84a56-105">Syntax</span></span>  
  
```  
typedef enum CorDebugJITCompilerFlagsDeprecated {  
    CORDEBUG_JIT_TRACK_DEBUG_INFO  = 0x1  
} CorDebugJITCompilerFlagsDeprecated;  
```  
  
## <a name="members"></a><span data-ttu-id="84a56-106">Membres</span><span class="sxs-lookup"><span data-stu-id="84a56-106">Members</span></span>  
  
|<span data-ttu-id="84a56-107">Membre</span><span class="sxs-lookup"><span data-stu-id="84a56-107">Member</span></span>|<span data-ttu-id="84a56-108">Description</span><span class="sxs-lookup"><span data-stu-id="84a56-108">Description</span></span>|  
|------------|-----------------|  
|`CORDEBUG_JIT_TRACK_DEBUG_INFO`|<span data-ttu-id="84a56-109">Utilisez plutôt `CORDEBUG_JIT_DEFAULT`.</span><span class="sxs-lookup"><span data-stu-id="84a56-109">Use `CORDEBUG_JIT_DEFAULT` instead.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="84a56-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84a56-110">Requirements</span></span>  
 <span data-ttu-id="84a56-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="84a56-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="84a56-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="84a56-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="84a56-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="84a56-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="84a56-114">**Versions du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="84a56-114">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84a56-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84a56-115">See also</span></span>

- [<span data-ttu-id="84a56-116">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="84a56-116">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
