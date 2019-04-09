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
ms.openlocfilehash: 33ad221f2a05357484d0877b6306d78e3864eff6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59120170"
---
# <a name="icordebuggcreferenceenumnext-method"></a><span data-ttu-id="6c70b-102">ICorDebugGCReferenceEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="6c70b-102">ICorDebugGCReferenceEnum::Next Method</span></span>
<span data-ttu-id="6c70b-103">Obtient le nombre spécifié de [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances qui contiennent des informations sur les objets qui seront le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="6c70b-103">Gets the specified number of [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances that contain information about objects that will be garbage-collected.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c70b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c70b-104">Syntax</span></span>  
  
```  
HRESULT Next(  
    [in] ULONG celt,    [out, size_is(celt), length_is(*pceltFetched)] COR_GC_REFERENCE roots[],   
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6c70b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c70b-105">Parameters</span></span>  
 <span data-ttu-id="6c70b-106">celt</span><span class="sxs-lookup"><span data-stu-id="6c70b-106">celt</span></span>  
 <span data-ttu-id="6c70b-107">[in] Le nombre de racines à récupérer.</span><span class="sxs-lookup"><span data-stu-id="6c70b-107">[in] The number of roots to be retrieved.</span></span>  
  
 <span data-ttu-id="6c70b-108">racines</span><span class="sxs-lookup"><span data-stu-id="6c70b-108">roots</span></span>  
 <span data-ttu-id="6c70b-109">[out] Un tableau de pointeurs, chacun d’eux pointe vers un [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objet qui représente la racine d’un objet pour le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="6c70b-109">[out] An array of pointers, each of which points to a [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) object that represents the root of an object to be garbage-collected.</span></span>  
  
 <span data-ttu-id="6c70b-110">pceltFetched</span><span class="sxs-lookup"><span data-stu-id="6c70b-110">pceltFetched</span></span>  
 <span data-ttu-id="6c70b-111">[out] Un pointeur vers le nombre de [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) réellement retournés dans des objets `roots`.</span><span class="sxs-lookup"><span data-stu-id="6c70b-111">[out] A pointer to the number of [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objects actually returned in `roots`.</span></span> <span data-ttu-id="6c70b-112">Cette valeur peut être `null` si `celt` est égal à 1.</span><span class="sxs-lookup"><span data-stu-id="6c70b-112">This value may be `null` if `celt` is 1.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6c70b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6c70b-113">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6c70b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c70b-114">Requirements</span></span>  
 <span data-ttu-id="6c70b-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6c70b-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c70b-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6c70b-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6c70b-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6c70b-117">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="6c70b-118">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="6c70b-118">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="6c70b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c70b-119">See also</span></span>

- [<span data-ttu-id="6c70b-120">ICorDebugGCReferenceEnum, interface</span><span class="sxs-lookup"><span data-stu-id="6c70b-120">ICorDebugGCReferenceEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-interface.md)
- [<span data-ttu-id="6c70b-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="6c70b-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
