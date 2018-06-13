---
title: ICorDebugObjectEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugObjectEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectEnum::Next
helpviewer_keywords:
- Next method, ICorDebugObjectEnum interface [.NET Framework debugging]
- ICorDebugObjectEnum::Next method [.NET Framework debugging]
ms.assetid: 10093e3d-26b6-4ad7-8ef3-bbf66243fc02
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 59b37c30df6467439d04e367e13b0fc4ffff0ec6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33422944"
---
# <a name="icordebugobjectenumnext-method"></a><span data-ttu-id="e94b8-102">ICorDebugObjectEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="e94b8-102">ICorDebugObjectEnum::Next Method</span></span>
<span data-ttu-id="e94b8-103">Obtient les adresses virtuelles relatives (RVA) du nombre spécifié d’objets à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="e94b8-103">Gets the relative virtual addresses (RVAs) of the specified number of objects from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e94b8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e94b8-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]    
        CORDB_ADDRESS objects[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e94b8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e94b8-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="e94b8-106">[in] Nombre d'objets à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e94b8-106">[in] The number of objects to be retrieved.</span></span>  
  
 `objects`  
 <span data-ttu-id="e94b8-107">[out] Tableau de pointeurs, chacun pointant vers un objet CORDB_ADDRESS.</span><span class="sxs-lookup"><span data-stu-id="e94b8-107">[out] An array of pointers, each of which points to a CORDB_ADDRESS object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="e94b8-108">[out] Pointeur vers le nombre d’objets retournés.</span><span class="sxs-lookup"><span data-stu-id="e94b8-108">[out] Pointer to the number of objects actually returned.</span></span> <span data-ttu-id="e94b8-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="e94b8-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e94b8-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e94b8-110">Requirements</span></span>  
 <span data-ttu-id="e94b8-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e94b8-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e94b8-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e94b8-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e94b8-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e94b8-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e94b8-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e94b8-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e94b8-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e94b8-115">See Also</span></span>  
 
