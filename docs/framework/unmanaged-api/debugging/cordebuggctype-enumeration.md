---
title: CorDebugGCType, énumération
ms.date: 03/30/2017
api_name:
- CorDebugGCType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugGCType
helpviewer_keywords:
- CorDebugGCType enumeration [.NET Framework debugging]
ms.assetid: 880ca92a-42d4-42a5-9b9c-c2848eb39c6a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 315d6dd522f3c6be2d36b1eb411d9f471350df60
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651751"
---
# <a name="cordebuggctype-enumeration"></a><span data-ttu-id="e5767-102">CorDebugGCType, énumération</span><span class="sxs-lookup"><span data-stu-id="e5767-102">CorDebugGCType Enumeration</span></span>
<span data-ttu-id="e5767-103">Indique si le récupérateur de mémoire s'exécute sur une station de travail ou sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="e5767-103">Indicates whether the garbage collector is running on a workstation or a server.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5767-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5767-104">Syntax</span></span>  
  
```  
typedef enum CorDebugGCType {  
    CorDebugWorkstationGC  = 0,  
    CorDebugServerGC       = ( CorDebugWorkstationGC + 1 )  
} CorDebugGCType;  
```  
  
## <a name="parameters"></a><span data-ttu-id="e5767-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5767-105">Parameters</span></span>  
  
## <a name="members"></a><span data-ttu-id="e5767-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e5767-106">Members</span></span>  
  
|<span data-ttu-id="e5767-107">Nom de membre</span><span class="sxs-lookup"><span data-stu-id="e5767-107">Member name</span></span>|<span data-ttu-id="e5767-108">Description</span><span class="sxs-lookup"><span data-stu-id="e5767-108">Description</span></span>|  
|-----------------|-----------------|  
|`CorDebugWorkstationGC`|<span data-ttu-id="e5767-109">Le garbage collector s’exécute sur une station de travail.</span><span class="sxs-lookup"><span data-stu-id="e5767-109">The garbage collector is running on a workstation.</span></span>|  
|`CorDebugServerGC`|<span data-ttu-id="e5767-110">Le garbage collector est en cours d’exécution sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="e5767-110">The garbage collector is running on a server.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e5767-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e5767-111">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5767-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5767-112">Requirements</span></span>  
 <span data-ttu-id="e5767-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e5767-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5767-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e5767-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e5767-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e5767-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e5767-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5767-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5767-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5767-117">See also</span></span>

- [<span data-ttu-id="e5767-118">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="e5767-118">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
