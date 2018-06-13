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
ms.openlocfilehash: 7624a22e5d65ae94797779a0b8cfa70f226450ac
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33418982"
---
# <a name="icordebugmoduleenumnext-method"></a><span data-ttu-id="b1102-102">ICorDebugModuleEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="b1102-102">ICorDebugModuleEnum::Next Method</span></span>
<span data-ttu-id="b1102-103">Obtient le nombre d’instances de « ICorDebugModule » spécifié par `celt` à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="b1102-103">Gets the number of "ICorDebugModule" instances specified by `celt` from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1102-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1102-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in]  ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugModule *modules[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b1102-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1102-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="b1102-106">[in] Le nombre de `ICorDebugModule` instances doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="b1102-106">[in] The number of `ICorDebugModule` instances to be retrieved.</span></span>  
  
 `modules`  
 <span data-ttu-id="b1102-107">[out] Un tableau de pointeurs, chacun pointant vers un `ICorDebugModule` objet.</span><span class="sxs-lookup"><span data-stu-id="b1102-107">[out] An array of pointers, each of which points to an `ICorDebugModule` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="b1102-108">[out] Pointeur vers le nombre de `ICorDebugModule` instances réellement retournées.</span><span class="sxs-lookup"><span data-stu-id="b1102-108">[out] Pointer to the number of `ICorDebugModule` instances actually returned.</span></span> <span data-ttu-id="b1102-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="b1102-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b1102-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b1102-110">Requirements</span></span>  
 <span data-ttu-id="b1102-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b1102-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1102-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b1102-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b1102-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b1102-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b1102-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b1102-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1102-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1102-115">See Also</span></span>  
 
