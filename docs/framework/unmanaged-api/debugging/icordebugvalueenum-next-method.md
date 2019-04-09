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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59174211"
---
# <a name="icordebugvalueenumnext-method"></a><span data-ttu-id="35ec0-102">ICorDebugValueEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="35ec0-102">ICorDebugValueEnum::Next Method</span></span>
<span data-ttu-id="35ec0-103">Obtient le nombre spécifié d’instances de « ICorDebugValue » à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="35ec0-103">Gets the specified number of "ICorDebugValue" instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35ec0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35ec0-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in]  ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugValue *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="35ec0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35ec0-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="35ec0-106">[in] Le nombre de `ICorDebugValue` instances à récupérer.</span><span class="sxs-lookup"><span data-stu-id="35ec0-106">[in] The number of `ICorDebugValue` instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="35ec0-107">[out] Un tableau de pointeurs, chacun d’eux pointe vers un `ICorDebugValue` objet.</span><span class="sxs-lookup"><span data-stu-id="35ec0-107">[out] An array of pointers, each of which points to an `ICorDebugValue` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="35ec0-108">[out] Pointeur vers le nombre de `ICorDebugValue` instances réellement retournés.</span><span class="sxs-lookup"><span data-stu-id="35ec0-108">[out] Pointer to the number of `ICorDebugValue` instances actually returned.</span></span> <span data-ttu-id="35ec0-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="35ec0-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="35ec0-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35ec0-110">Requirements</span></span>  
 <span data-ttu-id="35ec0-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="35ec0-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="35ec0-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="35ec0-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="35ec0-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="35ec0-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="35ec0-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="35ec0-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="35ec0-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35ec0-115">See also</span></span>
