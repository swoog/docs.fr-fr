---
title: ICorDebugThreadEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThreadEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThreadEnum::Next
helpviewer_keywords:
- ICorDebugThreadEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugThreadEnum interface [.NET Framework debugging]
ms.assetid: f967c93d-9a7f-4aaf-99a1-a1317899ff3f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b80e0cc026ce80950c14436abb2e84548f9adb64
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61903316"
---
# <a name="icordebugthreadenumnext-method"></a><span data-ttu-id="de889-102">ICorDebugThreadEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="de889-102">ICorDebugThreadEnum::Next Method</span></span>
<span data-ttu-id="de889-103">Obtient le nombre d’instances de ICorDebugThread spécifiés à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="de889-103">Gets the number of specified ICorDebugThread instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de889-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de889-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugThread *threads[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="de889-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de889-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="de889-106">[in] Le nombre de `ICorDebugThread` instances à récupérer.</span><span class="sxs-lookup"><span data-stu-id="de889-106">[in] The number of `ICorDebugThread` instances to be retrieved.</span></span>  
  
 `threads`  
 <span data-ttu-id="de889-107">[out] Un tableau de pointeurs, chacun d’eux pointe vers un `ICorDebugThread` objet qui représente un thread.</span><span class="sxs-lookup"><span data-stu-id="de889-107">[out] An array of pointers, each of which points to an `ICorDebugThread` object that represents a thread.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="de889-108">[out] Pointeur vers le nombre de `ICorDebugThread` instances réellement retournés.</span><span class="sxs-lookup"><span data-stu-id="de889-108">[out] Pointer to the number of `ICorDebugThread` instances actually returned.</span></span> <span data-ttu-id="de889-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="de889-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="de889-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de889-110">Requirements</span></span>  
 <span data-ttu-id="de889-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="de889-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="de889-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="de889-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="de889-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="de889-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="de889-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="de889-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
