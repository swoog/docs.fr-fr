---
title: CorDebugJITCompilerFlags, énumération
ms.date: 03/30/2017
api_name:
- CorDebugJITCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugJITCompilerFlags
helpviewer_keywords:
- CorDebugJITCompilerFlags enumeration [.NET Framework debugging]
ms.assetid: c0774f70-5bed-45e8-9922-fdad778c4c33
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 512122d264e0817b89e8a371f57f11d31f7c4380
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54639633"
---
# <a name="cordebugjitcompilerflags-enumeration"></a><span data-ttu-id="b18f1-102">CorDebugJITCompilerFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="b18f1-102">CorDebugJITCompilerFlags Enumeration</span></span>
<span data-ttu-id="b18f1-103">Contient des valeurs qui influencent le comportement du compilateur juste-à-temps managé.</span><span class="sxs-lookup"><span data-stu-id="b18f1-103">Contains values that influence the behavior of the managed just-in-time (JIT) compiler.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b18f1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b18f1-104">Syntax</span></span>  
  
```  
typedef enum CorDebugJITCompilerFlags {  
  
    CORDEBUG_JIT_DEFAULT = 0x1,  
    CORDEBUG_JIT_DISABLE_OPTIMIZATION = 0x3,  
    CORDEBUG_JIT_ENABLE_ENC = 0x7  
  
} CorDebugJITCompilerFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="b18f1-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b18f1-105">Members</span></span>  
  
|<span data-ttu-id="b18f1-106">Membre</span><span class="sxs-lookup"><span data-stu-id="b18f1-106">Member</span></span>|<span data-ttu-id="b18f1-107">Description</span><span class="sxs-lookup"><span data-stu-id="b18f1-107">Description</span></span>|  
|------------|-----------------|  
|`CORDEBUG_JIT_DEFAULT`|<span data-ttu-id="b18f1-108">Spécifie que le compilateur doit suivre des données de compilation et permet des optimisations.</span><span class="sxs-lookup"><span data-stu-id="b18f1-108">Specifies that the compiler should track compilation data, and allows optimizations.</span></span>|  
|`CORDEBUG_JIT_DISABLE_OPTIMIZATION`|<span data-ttu-id="b18f1-109">Spécifie que le compilateur doit suivre des données de compilation, mais désactive les optimisations.</span><span class="sxs-lookup"><span data-stu-id="b18f1-109">Specifies that the compiler should track compilation data, but disables optimizations.</span></span>|  
|`CORDEBUG_JIT_ENABLE_ENC`|<span data-ttu-id="b18f1-110">Spécifie que le compilateur doit suivre des données de compilation, désactive les optimisations, et permet aux technologies Modifier & Continue.</span><span class="sxs-lookup"><span data-stu-id="b18f1-110">Specifies that the compiler should track compilation data, disables optimizations, and enables Edit and Continue technologies.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b18f1-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b18f1-111">Requirements</span></span>  
 <span data-ttu-id="b18f1-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b18f1-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b18f1-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b18f1-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b18f1-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b18f1-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b18f1-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b18f1-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b18f1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b18f1-116">See also</span></span>
- [<span data-ttu-id="b18f1-117">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="b18f1-117">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
