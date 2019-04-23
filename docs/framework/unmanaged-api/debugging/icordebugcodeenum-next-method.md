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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59113046"
---
# <a name="icordebugcodeenumnext-method"></a><span data-ttu-id="7b46f-102">ICorDebugCodeEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="7b46f-102">ICorDebugCodeEnum::Next Method</span></span>
<span data-ttu-id="7b46f-103">Obtient le nombre spécifié d’instances de « ICorDebugCode » à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="7b46f-103">Gets the specified number of "ICorDebugCode" instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b46f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b46f-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugCode *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7b46f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b46f-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="7b46f-106">[in] Le nombre de `ICorDebugCode` instances à récupérer.</span><span class="sxs-lookup"><span data-stu-id="7b46f-106">[in] The number of `ICorDebugCode` instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="7b46f-107">[out] Un tableau de pointeurs, chacun d’eux pointe vers un `ICorDebugCode` objet.</span><span class="sxs-lookup"><span data-stu-id="7b46f-107">[out] An array of pointers, each of which points to an `ICorDebugCode` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="7b46f-108">[out] Un pointeur vers le nombre de `ICorDebugCode` instances réellement retournés.</span><span class="sxs-lookup"><span data-stu-id="7b46f-108">[out] A pointer to the number of `ICorDebugCode` instances actually returned.</span></span> <span data-ttu-id="7b46f-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="7b46f-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7b46f-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b46f-110">Requirements</span></span>  
 <span data-ttu-id="7b46f-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7b46f-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7b46f-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7b46f-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7b46f-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7b46f-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7b46f-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7b46f-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b46f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b46f-115">See also</span></span>
