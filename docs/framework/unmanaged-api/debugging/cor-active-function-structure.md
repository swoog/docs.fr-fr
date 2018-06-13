---
title: COR_ACTIVE_FUNCTION, structure
ms.date: 03/30/2017
api_name:
- COR_ACTIVE_FUNCTION
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_ACTIVE_FUNCTION
helpviewer_keywords:
- COR_ACTIVE_FUNCTION structure [.NET Framework debugging]
ms.assetid: ed86185f-2152-459c-961f-10c06d62e83f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 86ab3d3a0f460f1ecdf86147b14df205aaf49635
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33404195"
---
# <a name="coractivefunction-structure"></a><span data-ttu-id="ce59b-102">COR_ACTIVE_FUNCTION, structure</span><span class="sxs-lookup"><span data-stu-id="ce59b-102">COR_ACTIVE_FUNCTION Structure</span></span>
<span data-ttu-id="ce59b-103">Contient des informations sur les fonctions qui sont actuellement actives dans les trames d'un thread.</span><span class="sxs-lookup"><span data-stu-id="ce59b-103">Contains information about the functions that are currently active in a thread's frames.</span></span> <span data-ttu-id="ce59b-104">Cette structure est utilisée par le [ICorDebugThread2::GetActiveFunctions](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getactivefunctions-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="ce59b-104">This structure is used by the [ICorDebugThread2::GetActiveFunctions](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getactivefunctions-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce59b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce59b-105">Syntax</span></span>  
  
```  
typedef struct  _COR_ACTIVE_FUNCTION {  
    ICorDebugAppDomain   *pAppDomain;  
    ICorDebugModule      *pModule;  
    ICorDebugFunction2   *pFunction;  
    ULONG32              ilOffset;  
    ULONG32              flags;  
} COR_ACTIVE_FUNCTION;  
```  
  
## <a name="members"></a><span data-ttu-id="ce59b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ce59b-106">Members</span></span>  
  
|<span data-ttu-id="ce59b-107">Membre</span><span class="sxs-lookup"><span data-stu-id="ce59b-107">Member</span></span>|<span data-ttu-id="ce59b-108">Description</span><span class="sxs-lookup"><span data-stu-id="ce59b-108">Description</span></span>|  
|------------|-----------------|  
|`pAppDomain`|<span data-ttu-id="ce59b-109">Pointeur vers le propriétaire du domaine d’application le `ilOffset` champ.</span><span class="sxs-lookup"><span data-stu-id="ce59b-109">Pointer to the application domain owner of the `ilOffset` field.</span></span>|  
|`pModule`|<span data-ttu-id="ce59b-110">Pointeur vers le propriétaire du module du `ilOffset` champ.</span><span class="sxs-lookup"><span data-stu-id="ce59b-110">Pointer to the module owner of the `ilOffset` field.</span></span>|  
|`pFunction`|<span data-ttu-id="ce59b-111">Pointeur vers le propriétaire de la fonction de la `ilOffset` champ.</span><span class="sxs-lookup"><span data-stu-id="ce59b-111">Pointer to the function owner of the `ilOffset` field.</span></span>|  
|`ilOffset`|<span data-ttu-id="ce59b-112">L’offset Microsoft intermediate language (MSIL), de l’image.</span><span class="sxs-lookup"><span data-stu-id="ce59b-112">The Microsoft intermediate language (MSIL) offset of the frame.</span></span>|  
|`flags`|<span data-ttu-id="ce59b-113">Réservé pour une future extensibilité.</span><span class="sxs-lookup"><span data-stu-id="ce59b-113">Reserved for future extensibility.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ce59b-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ce59b-114">Requirements</span></span>  
 <span data-ttu-id="ce59b-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ce59b-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ce59b-116">**En-tête :** CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="ce59b-116">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="ce59b-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ce59b-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ce59b-118">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ce59b-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce59b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce59b-119">See Also</span></span>  
 [<span data-ttu-id="ce59b-120">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="ce59b-120">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)  
 [<span data-ttu-id="ce59b-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="ce59b-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
