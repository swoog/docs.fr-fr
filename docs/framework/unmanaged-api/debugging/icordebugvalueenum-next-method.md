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
ms.openlocfilehash: b24507c7cb0860fc04fa519c6bd95113483f629d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59174211"
---
# <a name="icordebugvalueenumnext-method"></a><span data-ttu-id="0ac1c-102">ICorDebugValueEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="0ac1c-102">ICorDebugValueEnum::Next Method</span></span>
<span data-ttu-id="0ac1c-103">Obtient le nombre spécifié d’instances de « ICorDebugValue » à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-103">Gets the specified number of "ICorDebugValue" instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ac1c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ac1c-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in]  ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugValue *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0ac1c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ac1c-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="0ac1c-106">[in] Le nombre de `ICorDebugValue` instances à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-106">[in] The number of `ICorDebugValue` instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="0ac1c-107">[out] Un tableau de pointeurs, chacun d’eux pointe vers un `ICorDebugValue` objet.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-107">[out] An array of pointers, each of which points to an `ICorDebugValue` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="0ac1c-108">[out] Pointeur vers le nombre de `ICorDebugValue` instances réellement retournés.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-108">[out] Pointer to the number of `ICorDebugValue` instances actually returned.</span></span> <span data-ttu-id="0ac1c-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0ac1c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ac1c-110">Requirements</span></span>  
 <span data-ttu-id="0ac1c-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0ac1c-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0ac1c-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0ac1c-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0ac1c-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0ac1c-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0ac1c-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0ac1c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ac1c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ac1c-115">See also</span></span>
