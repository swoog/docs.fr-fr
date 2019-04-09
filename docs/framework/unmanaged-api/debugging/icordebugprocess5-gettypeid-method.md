---
title: ICorDebugProcess5::GetTypeID, méthode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugProcess5.GetTypeID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::GetTypeID
helpviewer_keywords:
- ICorDebugProcess5::GetTypeID method [.NET Framework debugging]
- GetTypeID method, ICorDebugProcess5 interface [.NET Framework debugging]
ms.assetid: 47dbaea4-8857-462e-93ba-fff880fc9e50
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 07c23a32037e83a878bb3136c48176f19249b207
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59173185"
---
# <a name="icordebugprocess5gettypeid-method"></a><span data-ttu-id="d414a-102">ICorDebugProcess5::GetTypeID, méthode</span><span class="sxs-lookup"><span data-stu-id="d414a-102">ICorDebugProcess5::GetTypeID Method</span></span>
<span data-ttu-id="d414a-103">Convertit une adresse de l’objet à un [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) identificateur.</span><span class="sxs-lookup"><span data-stu-id="d414a-103">Converts an object address to a [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d414a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d414a-104">Syntax</span></span>  
  
```cpp
HRESULT GetTypeID(  
    [in] CORDB_ADDRESS obj,  
    [out] COR_TYPEID *pId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d414a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d414a-105">Parameters</span></span>  
 `obj`  
 <span data-ttu-id="d414a-106">[in] L’adresse de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d414a-106">[in] The object address.</span></span>  
  
 `pId`  
 <span data-ttu-id="d414a-107">Un pointeur vers le [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) valeur qui identifie l’objet.</span><span class="sxs-lookup"><span data-stu-id="d414a-107">A pointer to the [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) value that identifies the object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d414a-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d414a-108">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d414a-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d414a-109">Requirements</span></span>  
 <span data-ttu-id="d414a-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d414a-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d414a-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d414a-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d414a-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d414a-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="d414a-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="d414a-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="d414a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d414a-114">See also</span></span>

- [<span data-ttu-id="d414a-115">ICorDebugProcess5, interface</span><span class="sxs-lookup"><span data-stu-id="d414a-115">ICorDebugProcess5 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-interface.md)
- [<span data-ttu-id="d414a-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d414a-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
