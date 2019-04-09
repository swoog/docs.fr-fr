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
ms.openlocfilehash: 1e2d7a344cabb1ab816e4fe696ebb47276397ec3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59095033"
---
# <a name="icordebugenumskip-method"></a><span data-ttu-id="74c6f-102">ICorDebugEnum::Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="74c6f-102">ICorDebugEnum::Skip Method</span></span>
<span data-ttu-id="74c6f-103">Déplace le curseur vers l’avant dans l’énumération par le nombre spécifié d’éléments.</span><span class="sxs-lookup"><span data-stu-id="74c6f-103">Moves the cursor forward in the enumeration by the specified number of items.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="74c6f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74c6f-104">Syntax</span></span>  
  
```  
HRESULT Skip (  
    [in] ULONG celt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="74c6f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74c6f-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="74c6f-106">[in] Le nombre d’éléments par lequel déplacer le curseur vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="74c6f-106">[in] The number of items by which to move the cursor forward.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="74c6f-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74c6f-107">Requirements</span></span>  
 <span data-ttu-id="74c6f-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="74c6f-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="74c6f-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="74c6f-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="74c6f-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="74c6f-110">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="74c6f-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="74c6f-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="74c6f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74c6f-112">See also</span></span>

- [<span data-ttu-id="74c6f-113">ICorDebugEnum, interface</span><span class="sxs-lookup"><span data-stu-id="74c6f-113">ICorDebugEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugenum-interface1.md)
