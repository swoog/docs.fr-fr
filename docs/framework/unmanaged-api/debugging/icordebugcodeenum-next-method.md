---
title: ICorDebugCodeEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCodeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCodeEnum::Next
helpviewer_keywords:
- ICorDebugCodeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugEnum interface [.NET Framework debugging]
ms.assetid: 644ece86-384d-4c63-9fba-52c789616ff7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5db87cd4ad965654b63a68828cd088b8d2f7d07c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59113046"
---
# <a name="icordebugcodeenumnext-method"></a><span data-ttu-id="e823c-102">ICorDebugCodeEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="e823c-102">ICorDebugCodeEnum::Next Method</span></span>
<span data-ttu-id="e823c-103">Obtient le nombre spécifié d’instances de « ICorDebugCode » à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="e823c-103">Gets the specified number of "ICorDebugCode" instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e823c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e823c-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugCode *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e823c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e823c-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="e823c-106">[in] Le nombre de `ICorDebugCode` instances à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e823c-106">[in] The number of `ICorDebugCode` instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="e823c-107">[out] Un tableau de pointeurs, chacun d’eux pointe vers un `ICorDebugCode` objet.</span><span class="sxs-lookup"><span data-stu-id="e823c-107">[out] An array of pointers, each of which points to an `ICorDebugCode` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="e823c-108">[out] Un pointeur vers le nombre de `ICorDebugCode` instances réellement retournés.</span><span class="sxs-lookup"><span data-stu-id="e823c-108">[out] A pointer to the number of `ICorDebugCode` instances actually returned.</span></span> <span data-ttu-id="e823c-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="e823c-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e823c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e823c-110">Requirements</span></span>  
 <span data-ttu-id="e823c-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e823c-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e823c-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e823c-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e823c-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e823c-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="e823c-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="e823c-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="e823c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e823c-115">See also</span></span>
