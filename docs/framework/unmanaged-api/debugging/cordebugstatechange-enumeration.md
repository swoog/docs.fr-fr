---
title: CorDebugStateChange, énumération
ms.date: 02/07/2019
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
ms.openlocfilehash: 05a29022d3ebad37322aef9826f10689d2b5b06b
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221132"
---
# <a name="cordebugstatechange-enumeration"></a><span data-ttu-id="e44a2-102">CorDebugStateChange, énumération</span><span class="sxs-lookup"><span data-stu-id="e44a2-102">CorDebugStateChange Enumeration</span></span>

<span data-ttu-id="e44a2-103">Représente la quantité de données mises en cache à ignorer sur la base des modifications apportées au processus.</span><span class="sxs-lookup"><span data-stu-id="e44a2-103">Describes the amount of cached data that must be discarded based on changes to the process.</span></span>

## <a name="syntax"></a><span data-ttu-id="e44a2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e44a2-104">Syntax</span></span>

```
typedef enum CorDebugStateChange
{
    PROCESS_RUNNING = 0x0000001,
    FLUSH_ALL       = 0x0000002,
} CorDebugStateChange;
```

## <a name="members"></a><span data-ttu-id="e44a2-105">Membres</span><span class="sxs-lookup"><span data-stu-id="e44a2-105">Members</span></span>

| <span data-ttu-id="e44a2-106">Membre</span><span class="sxs-lookup"><span data-stu-id="e44a2-106">Member</span></span>            | <span data-ttu-id="e44a2-107">Description</span><span class="sxs-lookup"><span data-stu-id="e44a2-107">Description</span></span>                                                              |
| ----------------- | ------------------------------------------------------------------------ |
| `PROCESS_RUNNING` | <span data-ttu-id="e44a2-108">Le processus a atteint un nouvel état de mémoire via l'exécution en avant.</span><span class="sxs-lookup"><span data-stu-id="e44a2-108">The process reached a new memory state via forward execution.</span></span>            |
| `FLUSH_ALL`       | <span data-ttu-id="e44a2-109">La mémoire du processus peut être arbitrairement différente de ce qu'elle était précédemment.</span><span class="sxs-lookup"><span data-stu-id="e44a2-109">The process' memory may be arbitrarily different than it was previously.</span></span> |

## <a name="remarks"></a><span data-ttu-id="e44a2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e44a2-110">Remarks</span></span>

 <span data-ttu-id="e44a2-111">Un membre de la `CorDebugStateChange` énumération est fournie en tant qu’argument lorsque le débogueur appelle la `ProcessStateChanged` méthode avec [ICorDebugProcess4::ProcessStateChanged](icordebugprocess4-processstatechanged-method.md) ou [ICorDebugProcess6 :: ProcessStateChanged](icordebugprocess6-processstatechanged-method.md)</span><span class="sxs-lookup"><span data-stu-id="e44a2-111">A member of the `CorDebugStateChange` enumeration is provided as an argument when the debugger calls the `ProcessStateChanged` method either with [ICorDebugProcess4::ProcessStateChanged](icordebugprocess4-processstatechanged-method.md) or [ICorDebugProcess6::ProcessStateChanged](icordebugprocess6-processstatechanged-method.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="e44a2-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e44a2-112">Requirements</span></span>

 <span data-ttu-id="e44a2-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e44a2-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

 <span data-ttu-id="e44a2-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e44a2-114">**Header:** CorDebug.idl, CorDebug.h</span></span>

 <span data-ttu-id="e44a2-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e44a2-115">**Library:** CorGuids.lib</span></span>

 <span data-ttu-id="e44a2-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e44a2-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="e44a2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e44a2-117">See also</span></span>

- [<span data-ttu-id="e44a2-118">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="e44a2-118">Debugging Enumerations</span></span>](debugging-enumerations.md)
- [<span data-ttu-id="e44a2-119">Débogage</span><span class="sxs-lookup"><span data-stu-id="e44a2-119">Debugging</span></span>](index.md)
