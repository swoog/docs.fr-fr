---
title: CorDebugExceptionUnwindCallbackType, énumération
ms.date: 03/30/2017
api_name:
- CorDebugExceptionUnwindCallbackType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugExceptionUnwindCallbackType
helpviewer_keywords:
- CorDebugExceptionUnwindCallbackType enumeration [.NET Framework debugging]
ms.assetid: 783dce92-8a98-43db-8f78-888d943dd5b2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 408e72eeaa1dac83c45488d186425f30c6043280
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59155621"
---
# <a name="cordebugexceptionunwindcallbacktype-enumeration"></a><span data-ttu-id="9ee1a-102">CorDebugExceptionUnwindCallbackType, énumération</span><span class="sxs-lookup"><span data-stu-id="9ee1a-102">CorDebugExceptionUnwindCallbackType Enumeration</span></span>
<span data-ttu-id="9ee1a-103">Indique l'événement qui est signalé par le rappel lors de la phase de déroulement.</span><span class="sxs-lookup"><span data-stu-id="9ee1a-103">Indicates the event that is being signaled by the callback during the unwind phase.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ee1a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ee1a-104">Syntax</span></span>  
  
```  
typedef enum CorDebugExceptionUnwindCallbackType {  
    DEBUG_EXCEPTION_UNWIND_BEGIN = 1,  
    DEBUG_EXCEPTION_INTERCEPTED  = 2  
} CorDebugExceptionUnwindCallbackType;  
```  
  
## <a name="members"></a><span data-ttu-id="9ee1a-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9ee1a-105">Members</span></span>  
  
|<span data-ttu-id="9ee1a-106">Membre</span><span class="sxs-lookup"><span data-stu-id="9ee1a-106">Member</span></span>|<span data-ttu-id="9ee1a-107">Description</span><span class="sxs-lookup"><span data-stu-id="9ee1a-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_EXCEPTION_UNWIND_BEGIN`|<span data-ttu-id="9ee1a-108">Début du processus de déroulement.</span><span class="sxs-lookup"><span data-stu-id="9ee1a-108">The beginning of the unwind process.</span></span>|  
|`DEBUG_EXCEPTION_INTERCEPTED`|<span data-ttu-id="9ee1a-109">L’exception a été interceptée.</span><span class="sxs-lookup"><span data-stu-id="9ee1a-109">The exception was intercepted.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9ee1a-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ee1a-110">Requirements</span></span>  
 <span data-ttu-id="9ee1a-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9ee1a-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ee1a-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9ee1a-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9ee1a-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9ee1a-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9ee1a-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ee1a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ee1a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ee1a-115">See also</span></span>

- [<span data-ttu-id="9ee1a-116">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="9ee1a-116">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
