---
title: ICorDebugModuleEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModuleEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModuleEnum::Next
helpviewer_keywords:
- ICorDebugModuleEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugModuleEnum interface [.NET Framework debugging]
ms.assetid: 9ff3fcd6-38fe-41f8-bfd3-f0ab6c7d77ca
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 027c7b0b9ee7902c81b620549b335cd123d8b277
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57491371"
---
# <a name="icordebugmoduleenumnext-method"></a><span data-ttu-id="0c5cc-102">ICorDebugModuleEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="0c5cc-102">ICorDebugModuleEnum::Next Method</span></span>
<span data-ttu-id="0c5cc-103">Obtient le nombre d’instances de « ICorDebugModule » spécifiée par `celt` à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-103">Gets the number of "ICorDebugModule" instances specified by `celt` from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c5cc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c5cc-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in]  ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugModule *modules[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0c5cc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c5cc-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="0c5cc-106">[in] Le nombre de `ICorDebugModule` instances à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-106">[in] The number of `ICorDebugModule` instances to be retrieved.</span></span>  
  
 `modules`  
 <span data-ttu-id="0c5cc-107">[out] Un tableau de pointeurs, chacun d’eux pointe vers un `ICorDebugModule` objet.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-107">[out] An array of pointers, each of which points to an `ICorDebugModule` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="0c5cc-108">[out] Pointeur vers le nombre de `ICorDebugModule` instances réellement retournés.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-108">[out] Pointer to the number of `ICorDebugModule` instances actually returned.</span></span> <span data-ttu-id="0c5cc-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c5cc-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0c5cc-110">Requirements</span></span>  
 <span data-ttu-id="0c5cc-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0c5cc-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c5cc-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0c5cc-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0c5cc-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0c5cc-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0c5cc-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c5cc-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c5cc-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c5cc-115">See also</span></span>

