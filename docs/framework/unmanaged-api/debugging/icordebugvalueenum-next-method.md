---
title: ICorDebugValueEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugValueEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValueEnum::Next
helpviewer_keywords:
- ICorDebugValueEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugValueEnum interface [.NET Framework debugging]
ms.assetid: f5ef94dd-dfee-49d3-a398-b110f8906dd8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 433e387365834498203e444ed2f85889f8adde06
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420442"
---
# <a name="icordebugvalueenumnext-method"></a><span data-ttu-id="d94fa-102">ICorDebugValueEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="d94fa-102">ICorDebugValueEnum::Next Method</span></span>
<span data-ttu-id="d94fa-103">Obtient le nombre spécifié d’instances de « ICorDebugValue » à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="d94fa-103">Gets the specified number of "ICorDebugValue" instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d94fa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d94fa-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in]  ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugValue *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d94fa-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d94fa-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="d94fa-106">[in] Le nombre de `ICorDebugValue` instances doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="d94fa-106">[in] The number of `ICorDebugValue` instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="d94fa-107">[out] Un tableau de pointeurs, chacun pointant vers un `ICorDebugValue` objet.</span><span class="sxs-lookup"><span data-stu-id="d94fa-107">[out] An array of pointers, each of which points to an `ICorDebugValue` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="d94fa-108">[out] Pointeur vers le nombre de `ICorDebugValue` instances réellement retournées.</span><span class="sxs-lookup"><span data-stu-id="d94fa-108">[out] Pointer to the number of `ICorDebugValue` instances actually returned.</span></span> <span data-ttu-id="d94fa-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="d94fa-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d94fa-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d94fa-110">Requirements</span></span>  
 <span data-ttu-id="d94fa-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d94fa-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d94fa-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d94fa-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d94fa-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d94fa-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d94fa-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d94fa-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d94fa-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d94fa-115">See Also</span></span>  
    
 
