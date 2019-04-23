---
title: CorDebugExceptionFlags, énumération
ms.date: 03/30/2017
api_name:
- CorDebugExceptionFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugExceptionFlags
helpviewer_keywords:
- CorDebugExceptionFlags enumeration [.NET Framework debugging]
ms.assetid: b22687a8-e9cf-4e65-a1b0-f92a81bc524e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2c7b9b25673685dde8b75702c80f525515917ae1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59078705"
---
# <a name="cordebugexceptionflags-enumeration"></a><span data-ttu-id="e5d77-102">CorDebugExceptionFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="e5d77-102">CorDebugExceptionFlags Enumeration</span></span>
<span data-ttu-id="e5d77-103">Fournit des informations supplémentaires sur une exception.</span><span class="sxs-lookup"><span data-stu-id="e5d77-103">Provides additional information about an exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5d77-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5d77-104">Syntax</span></span>  
  
```  
typedef enum CorDebugExceptionFlags {  
    DEBUG_EXCEPTION_NONE = 0,  
    DEBUG_EXCEPTION_CAN_BE_INTERCEPTED = 0x0001  
} CorDebugExceptionFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="e5d77-105">Membres</span><span class="sxs-lookup"><span data-stu-id="e5d77-105">Members</span></span>  
  
|<span data-ttu-id="e5d77-106">Membre</span><span class="sxs-lookup"><span data-stu-id="e5d77-106">Member</span></span>|<span data-ttu-id="e5d77-107">Description</span><span class="sxs-lookup"><span data-stu-id="e5d77-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_EXCEPTION_NONE`|<span data-ttu-id="e5d77-108">Il n'existe pas d'exception.</span><span class="sxs-lookup"><span data-stu-id="e5d77-108">There is no exception.</span></span>|  
|`DEBUG_EXCEPTION_CAN_BE_INTERCEPTED`|<span data-ttu-id="e5d77-109">L'exception peut être interceptée.</span><span class="sxs-lookup"><span data-stu-id="e5d77-109">The exception is interceptable.</span></span><br /><br /> <span data-ttu-id="e5d77-110">Le moment où se produit l'exception peut néanmoins être tel que le débogueur ne peut pas l'intercepter.</span><span class="sxs-lookup"><span data-stu-id="e5d77-110">The timing of the exception may still be such that the debugger cannot intercept it.</span></span> <span data-ttu-id="e5d77-111">Par exemple, s'il n'existe pas de code managé en dessous du rappel actif ou si l'événement d'exception provient d'un attachement juste-à-temps, l'exception ne peut pas être interceptée.</span><span class="sxs-lookup"><span data-stu-id="e5d77-111">For example, if there is no managed code below the current callback or the exception event resulted from a just-in-time (JIT) attachment, the exception cannot be intercepted.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e5d77-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e5d77-112">Remarks</span></span>  
 <span data-ttu-id="e5d77-113">De nouvelles valeurs sont susceptibles d'être ajoutées dans les versions ultérieures : il est donc recommandé de préparer du code qui utilise `CorDebugExceptionFlags` pour les valeurs inattendues.</span><span class="sxs-lookup"><span data-stu-id="e5d77-113">New values may be added to this enumeration in later versions, so you should prepare code that uses `CorDebugExceptionFlags` for unexpected values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5d77-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5d77-114">Requirements</span></span>  
 <span data-ttu-id="e5d77-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e5d77-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5d77-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e5d77-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e5d77-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e5d77-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e5d77-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5d77-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5d77-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5d77-119">See also</span></span>

- [<span data-ttu-id="e5d77-120">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="e5d77-120">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
