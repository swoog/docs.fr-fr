---
title: ICorPublishEnum::GetCount, méthode
ms.date: 03/30/2017
api_name:
- ICorPublishEnum.GetCount
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishEnum::GetCount
helpviewer_keywords:
- GetCount method, ICorPublishEnum interface [.NET Framework debugging]
- ICorPublishEnum::GetCount method [.NET Framework debugging]
ms.assetid: d228f684-2be3-4029-93ae-31fe02213c1f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f191c31ec5333fbea52c298f477c8c624beb92b2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424506"
---
# <a name="icorpublishenumgetcount-method"></a><span data-ttu-id="21010-102">ICorPublishEnum::GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="21010-102">ICorPublishEnum::GetCount Method</span></span>
<span data-ttu-id="21010-103">Obtient le nombre d’éléments dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="21010-103">Gets the number of items in the enumeration.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="21010-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21010-104">Syntax</span></span>  
  
```  
HRESULT GetCount (  
    [out] ULONG   *pcelt  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="21010-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21010-105">Parameters</span></span>  
 `pcelt`  
 <span data-ttu-id="21010-106">[out] Pointeur vers le nombre d’éléments dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="21010-106">[out] A pointer to the number of items in the enumeration.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="21010-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="21010-107">Requirements</span></span>  
 <span data-ttu-id="21010-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="21010-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="21010-109">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="21010-109">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="21010-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="21010-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="21010-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="21010-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="21010-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21010-112">See Also</span></span>  
 [<span data-ttu-id="21010-113">ICorPublishEnum, interface</span><span class="sxs-lookup"><span data-stu-id="21010-113">ICorPublishEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md)
