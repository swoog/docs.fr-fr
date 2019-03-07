---
title: ICorDebugGCReferenceEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugGCReferenceEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGCReferenceEnum::Next
helpviewer_keywords:
- Next method, ICorDebugGCReferenceEnum interface [.NET Framework debugging]
- ICorDebugGCReferenceEnum::Next method [.NET Framework debugging]
ms.assetid: 91b1345c-a94f-4ef8-9696-3823d06c6d05
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9f76b727511ad604c407fb2998a5ecea26f91c49
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57481360"
---
# <a name="icordebuggcreferenceenumnext-method"></a><span data-ttu-id="ff203-102">ICorDebugGCReferenceEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="ff203-102">ICorDebugGCReferenceEnum::Next Method</span></span>
<span data-ttu-id="ff203-103">Obtient le nombre spécifié de [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances qui contiennent des informations sur les objets qui seront le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="ff203-103">Gets the specified number of [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances that contain information about objects that will be garbage-collected.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ff203-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff203-104">Syntax</span></span>  
  
```  
HRESULT Next(  
    [in] ULONG celt,    [out, size_is(celt), length_is(*pceltFetched)] COR_GC_REFERENCE roots[],   
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ff203-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff203-105">Parameters</span></span>  
 <span data-ttu-id="ff203-106">celt</span><span class="sxs-lookup"><span data-stu-id="ff203-106">celt</span></span>  
 <span data-ttu-id="ff203-107">[in] Le nombre de racines à récupérer.</span><span class="sxs-lookup"><span data-stu-id="ff203-107">[in] The number of roots to be retrieved.</span></span>  
  
 <span data-ttu-id="ff203-108">racines</span><span class="sxs-lookup"><span data-stu-id="ff203-108">roots</span></span>  
 <span data-ttu-id="ff203-109">[out] Un tableau de pointeurs, chacun d’eux pointe vers un [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objet qui représente la racine d’un objet pour le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="ff203-109">[out] An array of pointers, each of which points to a [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) object that represents the root of an object to be garbage-collected.</span></span>  
  
 <span data-ttu-id="ff203-110">pceltFetched</span><span class="sxs-lookup"><span data-stu-id="ff203-110">pceltFetched</span></span>  
 <span data-ttu-id="ff203-111">[out] Un pointeur vers le nombre de [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) réellement retournés dans des objets `roots`.</span><span class="sxs-lookup"><span data-stu-id="ff203-111">[out] A pointer to the number of [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objects actually returned in `roots`.</span></span> <span data-ttu-id="ff203-112">Cette valeur peut être `null` si `celt` est égal à 1.</span><span class="sxs-lookup"><span data-stu-id="ff203-112">This value may be `null` if `celt` is 1.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ff203-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ff203-113">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ff203-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ff203-114">Requirements</span></span>  
 <span data-ttu-id="ff203-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ff203-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ff203-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ff203-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ff203-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ff203-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ff203-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ff203-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff203-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff203-119">See also</span></span>
- [<span data-ttu-id="ff203-120">ICorDebugGCReferenceEnum, interface</span><span class="sxs-lookup"><span data-stu-id="ff203-120">ICorDebugGCReferenceEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-interface.md)
- [<span data-ttu-id="ff203-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="ff203-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
