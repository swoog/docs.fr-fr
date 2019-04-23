---
title: ICorPublishProcessEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorPublishProcessEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcessEnum::Next
helpviewer_keywords:
- ICorPublishProcessEnum::Next method [.NET Framework debugging]
- Next method, ICorPublishProcessEnum interface [.NET Framework debugging]
ms.assetid: 6c399f37-1e38-4ca1-b70d-8ae41f7228b7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 169716d1a6d0dd633821cc832de96c9a02958d76
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59183096"
---
# <a name="icorpublishprocessenumnext-method"></a><span data-ttu-id="dedd8-102">ICorPublishProcessEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="dedd8-102">ICorPublishProcessEnum::Next Method</span></span>
<span data-ttu-id="dedd8-103">Obtient le nombre spécifié de processus à partir de la collection, en commençant à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="dedd8-103">Gets the specified number of processes from the collection, starting at the current cursor position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dedd8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dedd8-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorPublishProcess **objects,  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dedd8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dedd8-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="dedd8-106">[in] Le nombre de processus à récupérer.</span><span class="sxs-lookup"><span data-stu-id="dedd8-106">[in] The number of processes to be retrieved.</span></span>  
  
 `objects`  
 <span data-ttu-id="dedd8-107">[out] Extrait un pointeur vers le tableau de [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) objets, chacun d’eux représente un processus.</span><span class="sxs-lookup"><span data-stu-id="dedd8-107">[out] A pointer to the array of retrieved [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) objects, each of which represents a process.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="dedd8-108">[out] Pointeur vers le nombre de processus réellement retournés.</span><span class="sxs-lookup"><span data-stu-id="dedd8-108">[out] Pointer to the number of processes actually returned.</span></span> <span data-ttu-id="dedd8-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="dedd8-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dedd8-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dedd8-110">Requirements</span></span>  
 <span data-ttu-id="dedd8-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dedd8-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dedd8-112">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="dedd8-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="dedd8-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dedd8-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dedd8-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dedd8-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dedd8-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dedd8-115">See also</span></span>

- [<span data-ttu-id="dedd8-116">ICorPublishProcessEnum, interface</span><span class="sxs-lookup"><span data-stu-id="dedd8-116">ICorPublishProcessEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md)
