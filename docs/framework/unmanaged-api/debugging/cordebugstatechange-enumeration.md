---
title: CorDebugStateChange, énumération
ms.date: 03/30/2017
api_name:
- CorDebugStateChange
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 1d4424ab-5143-4e50-a84a-ceeb4ddf3bba
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0f0f692b692628d50755ce813c66823f940dccb8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54513783"
---
# <a name="cordebugstatechange-enumeration"></a><span data-ttu-id="3f8f1-102">CorDebugStateChange, énumération</span><span class="sxs-lookup"><span data-stu-id="3f8f1-102">CorDebugStateChange Enumeration</span></span>
<span data-ttu-id="3f8f1-103">Représente la quantité de données mises en cache à ignorer sur la base des modifications apportées au processus.</span><span class="sxs-lookup"><span data-stu-id="3f8f1-103">Describes the amount of cached data that must be discarded based on changes to the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f8f1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f8f1-104">Syntax</span></span>  
  
```  
typedef enum CorDebugStateChange  
{  
    PROCESS_RUNNING = 0x0000001,   
    FLUSH_ALL       = 0x0000002,   
} CorDebugStateChange;  
```  
  
## <a name="members"></a><span data-ttu-id="3f8f1-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3f8f1-105">Members</span></span>  
  
|<span data-ttu-id="3f8f1-106">Membre</span><span class="sxs-lookup"><span data-stu-id="3f8f1-106">Member</span></span>|<span data-ttu-id="3f8f1-107">Description</span><span class="sxs-lookup"><span data-stu-id="3f8f1-107">Description</span></span>|  
|------------|-----------------|  
|`PROCESS_RUNNING`|<span data-ttu-id="3f8f1-108">Le processus a atteint un nouvel état de mémoire via l'exécution en avant.</span><span class="sxs-lookup"><span data-stu-id="3f8f1-108">The process reached a new memory state via forward execution.</span></span>|  
|`SET_CONTEXT_FLAG_UNWIND_FRAME`|<span data-ttu-id="3f8f1-109">La mémoire du processus peut être arbitrairement différente de ce qu'elle était précédemment.</span><span class="sxs-lookup"><span data-stu-id="3f8f1-109">The process' memory may be arbitrarily different than it was previously.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3f8f1-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3f8f1-110">Remarks</span></span>  
 <span data-ttu-id="3f8f1-111">Un membre de la `CorDebugStateChange` énumération est fournie en tant qu’argument lorsque le débogueur appelle la [ProcessStateChanged](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md) (méthode)</span><span class="sxs-lookup"><span data-stu-id="3f8f1-111">A member of the `CorDebugStateChange` enumeration is provided as an argument when the debugger calls the [ProcessStateChanged](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md) method</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3f8f1-112">Cette énumération est destinée à une utilisation dans des scénarios de débogage .NET Native uniquement.</span><span class="sxs-lookup"><span data-stu-id="3f8f1-112">This enumeration is intended for use in .NET Native debugging scenarios only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f8f1-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3f8f1-113">Requirements</span></span>  
 <span data-ttu-id="3f8f1-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3f8f1-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3f8f1-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3f8f1-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3f8f1-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3f8f1-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3f8f1-117">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3f8f1-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f8f1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f8f1-118">See also</span></span>
- [<span data-ttu-id="3f8f1-119">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="3f8f1-119">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
- [<span data-ttu-id="3f8f1-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="3f8f1-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
