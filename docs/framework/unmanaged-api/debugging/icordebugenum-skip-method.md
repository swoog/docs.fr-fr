---
title: ICorDebugEnum::Skip, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEnum.Skip
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEnum::Skip
helpviewer_keywords:
- ICorDebugEnum::Skip method [.NET Framework debugging]
- Skip method, ICorDebugEnum interface [.NET Framework debugging]
ms.assetid: e925d88a-67a5-4f76-88b8-09cedeed0232
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c7d280cd20b8ff76efe977983e3e9f6da32990c8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33413957"
---
# <a name="icordebugenumskip-method"></a><span data-ttu-id="9b6fb-102">ICorDebugEnum::Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="9b6fb-102">ICorDebugEnum::Skip Method</span></span>
<span data-ttu-id="9b6fb-103">Déplace le curseur vers l’avant dans l’énumération par le nombre spécifié d’éléments.</span><span class="sxs-lookup"><span data-stu-id="9b6fb-103">Moves the cursor forward in the enumeration by the specified number of items.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9b6fb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b6fb-104">Syntax</span></span>  
  
```  
HRESULT Skip (  
    [in] ULONG celt  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9b6fb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b6fb-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="9b6fb-106">[in] Le nombre d’éléments permettant de déplacer le curseur vers le bas.</span><span class="sxs-lookup"><span data-stu-id="9b6fb-106">[in] The number of items by which to move the cursor forward.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9b6fb-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9b6fb-107">Requirements</span></span>  
 <span data-ttu-id="9b6fb-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9b6fb-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9b6fb-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9b6fb-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9b6fb-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9b6fb-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9b6fb-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9b6fb-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b6fb-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b6fb-112">See Also</span></span>  
 [<span data-ttu-id="9b6fb-113">ICorDebugEnum, interface1</span><span class="sxs-lookup"><span data-stu-id="9b6fb-113">ICorDebugEnum Interface1</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugenum-interface1.md)
