---
title: ICorDebugModule::IsInMemory, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.IsInMemory
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::IsInMemory
helpviewer_keywords:
- IsInMemory method [.NET Framework debugging]
- ICorDebugModule::IsInMemory method [.NET Framework debugging]
ms.assetid: 89940711-98e7-4aa6-bffc-5e39e91e1b7d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0f057896d9dd65a850c0b07e4084bc263e804d20
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57497364"
---
# <a name="icordebugmoduleisinmemory-method"></a><span data-ttu-id="3d8e0-102">ICorDebugModule::IsInMemory, méthode</span><span class="sxs-lookup"><span data-stu-id="3d8e0-102">ICorDebugModule::IsInMemory Method</span></span>
<span data-ttu-id="3d8e0-103">Obtient une valeur qui indique si ce module existe uniquement en mémoire.</span><span class="sxs-lookup"><span data-stu-id="3d8e0-103">Gets a value that indicates whether this module exists only in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3d8e0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d8e0-104">Syntax</span></span>  
  
```  
HRESULT IsInMemory(  
    [out] BOOL *pInMemory  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3d8e0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d8e0-105">Parameters</span></span>  
 `pInMemory`  
 <span data-ttu-id="3d8e0-106">[out] `true` si ce module existe uniquement en mémoire ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="3d8e0-106">[out] `true` if this module exists only in memory; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3d8e0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3d8e0-107">Remarks</span></span>  
 <span data-ttu-id="3d8e0-108">Le common language runtime (CLR) prend en charge le chargement des modules à partir de flux bruts d’octets.</span><span class="sxs-lookup"><span data-stu-id="3d8e0-108">The common language runtime (CLR) supports the loading of modules from raw streams of bytes.</span></span> <span data-ttu-id="3d8e0-109">Ces modules sont appelés *en mémoire modules* et n’existent pas sur le disque.</span><span class="sxs-lookup"><span data-stu-id="3d8e0-109">Such modules are called *in-memory modules* and do not exist on disk.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3d8e0-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3d8e0-110">Requirements</span></span>  
 <span data-ttu-id="3d8e0-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3d8e0-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3d8e0-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3d8e0-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3d8e0-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3d8e0-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3d8e0-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3d8e0-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3d8e0-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d8e0-115">See also</span></span>


