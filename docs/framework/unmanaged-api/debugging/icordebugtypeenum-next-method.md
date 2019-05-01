---
title: ICorDebugTypeEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugTypeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugTypeEnum::Next
helpviewer_keywords:
- ICorDebugTypeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugTypeEnum interface [.NET Framework debugging]
ms.assetid: d0fdeba3-c195-4ece-8caf-79b1f40025d2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d47f14ff2adb37fca16cf6774a2b80cb2e074b17
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61993770"
---
# <a name="icordebugtypeenumnext-method"></a><span data-ttu-id="73223-102">ICorDebugTypeEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="73223-102">ICorDebugTypeEnum::Next Method</span></span>
<span data-ttu-id="73223-103">Obtient le nombre d’instances de « ICorDebugType » spécifiée par `celt` à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="73223-103">Gets the number of "ICorDebugType" instances specified by `celt` from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="73223-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73223-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in]  ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugType *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="73223-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73223-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="73223-106">[in] Le nombre de `ICorDebugType` instances à récupérer.</span><span class="sxs-lookup"><span data-stu-id="73223-106">[in] The number of `ICorDebugType` instances to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="73223-107">[out] Un tableau de pointeurs, chacun d’eux pointe vers un `ICorDebugType` objet.</span><span class="sxs-lookup"><span data-stu-id="73223-107">[out] An array of pointers, each of which points to an `ICorDebugType` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="73223-108">[out] Pointeur vers le nombre de `ICorDebugType` instances réellement retournés.</span><span class="sxs-lookup"><span data-stu-id="73223-108">[out] Pointer to the number of `ICorDebugType` instances actually returned.</span></span> <span data-ttu-id="73223-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="73223-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="73223-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73223-110">Requirements</span></span>  
 <span data-ttu-id="73223-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="73223-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="73223-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="73223-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="73223-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="73223-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="73223-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="73223-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="73223-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73223-115">See also</span></span>
