---
title: ICorDebugProcessEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcessEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcessEnum::Next
helpviewer_keywords:
- Next method, ICorDebugProcessEnum interface [.NET Framework debugging]
- ICorDebugProcessEnum::Next method [.NET Framework debugging]
ms.assetid: 4ac7077c-8d88-49c4-b360-b3af0c541c63
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6cd5dbc27376f8cd391f9ecc006c04d9a3a1eea8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33419742"
---
# <a name="icordebugprocessenumnext-method"></a><span data-ttu-id="3a08a-102">ICorDebugProcessEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="3a08a-102">ICorDebugProcessEnum::Next Method</span></span>
<span data-ttu-id="3a08a-103">Obtient le nombre spécifié d’instances de ICorDebugProcess à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="3a08a-103">Gets the specified number of ICorDebugProcess instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a08a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a08a-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in]  ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugProcess *processes[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3a08a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a08a-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="3a08a-106">[in] Le nombre de `ICorDebugProcess` instances doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="3a08a-106">[in] The number of `ICorDebugProcess` instances to be retrieved.</span></span>  
  
 `processess`  
 <span data-ttu-id="3a08a-107">[out] Un tableau de pointeurs, chacun pointant vers un `ICorDebugProcess` objet qui représente un processus.</span><span class="sxs-lookup"><span data-stu-id="3a08a-107">[out] An array of pointers, each of which points to an `ICorDebugProcess` object that represents a process.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="3a08a-108">[out] Pointeur vers le nombre de `ICorDebugProcess` instances réellement retournées.</span><span class="sxs-lookup"><span data-stu-id="3a08a-108">[out] Pointer to the number of `ICorDebugProcess` instances actually returned.</span></span> <span data-ttu-id="3a08a-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="3a08a-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a08a-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3a08a-110">Requirements</span></span>  
 <span data-ttu-id="3a08a-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3a08a-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3a08a-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3a08a-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3a08a-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3a08a-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3a08a-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3a08a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
