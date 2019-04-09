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
ms.openlocfilehash: 66a8ba59d221bb3fa2e815a1cbcfa79c474666cc
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59105467"
---
# <a name="cordebugjitcompilerflags-enumeration"></a><span data-ttu-id="675db-102">CorDebugJITCompilerFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="675db-102">CorDebugJITCompilerFlags Enumeration</span></span>
<span data-ttu-id="675db-103">Contient des valeurs qui influencent le comportement du compilateur juste-à-temps managé.</span><span class="sxs-lookup"><span data-stu-id="675db-103">Contains values that influence the behavior of the managed just-in-time (JIT) compiler.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="675db-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="675db-104">Syntax</span></span>  
  
```  
typedef enum CorDebugJITCompilerFlags {  
  
    CORDEBUG_JIT_DEFAULT = 0x1,  
    CORDEBUG_JIT_DISABLE_OPTIMIZATION = 0x3,  
    CORDEBUG_JIT_ENABLE_ENC = 0x7  
  
} CorDebugJITCompilerFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="675db-105">Membres</span><span class="sxs-lookup"><span data-stu-id="675db-105">Members</span></span>  
  
|<span data-ttu-id="675db-106">Membre</span><span class="sxs-lookup"><span data-stu-id="675db-106">Member</span></span>|<span data-ttu-id="675db-107">Description</span><span class="sxs-lookup"><span data-stu-id="675db-107">Description</span></span>|  
|------------|-----------------|  
|`CORDEBUG_JIT_DEFAULT`|<span data-ttu-id="675db-108">Spécifie que le compilateur doit suivre des données de compilation et permet des optimisations.</span><span class="sxs-lookup"><span data-stu-id="675db-108">Specifies that the compiler should track compilation data, and allows optimizations.</span></span>|  
|`CORDEBUG_JIT_DISABLE_OPTIMIZATION`|<span data-ttu-id="675db-109">Spécifie que le compilateur doit suivre des données de compilation, mais désactive les optimisations.</span><span class="sxs-lookup"><span data-stu-id="675db-109">Specifies that the compiler should track compilation data, but disables optimizations.</span></span>|  
|`CORDEBUG_JIT_ENABLE_ENC`|<span data-ttu-id="675db-110">Spécifie que le compilateur doit suivre des données de compilation, désactive les optimisations, et permet aux technologies Modifier & Continue.</span><span class="sxs-lookup"><span data-stu-id="675db-110">Specifies that the compiler should track compilation data, disables optimizations, and enables Edit and Continue technologies.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="675db-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="675db-111">Requirements</span></span>  
 <span data-ttu-id="675db-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="675db-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="675db-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="675db-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="675db-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="675db-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="675db-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="675db-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="675db-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="675db-116">See also</span></span>

- [<span data-ttu-id="675db-117">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="675db-117">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
