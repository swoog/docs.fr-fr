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
ms.openlocfilehash: d79a8b0c3c56ffe2b8f57ec26f5942ee0d681194
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59187588"
---
# <a name="icordebugmoduleisinmemory-method"></a><span data-ttu-id="e748d-102">ICorDebugModule::IsInMemory, méthode</span><span class="sxs-lookup"><span data-stu-id="e748d-102">ICorDebugModule::IsInMemory Method</span></span>
<span data-ttu-id="e748d-103">Obtient une valeur qui indique si ce module existe uniquement en mémoire.</span><span class="sxs-lookup"><span data-stu-id="e748d-103">Gets a value that indicates whether this module exists only in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e748d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e748d-104">Syntax</span></span>  
  
```  
HRESULT IsInMemory(  
    [out] BOOL *pInMemory  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e748d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e748d-105">Parameters</span></span>  
 `pInMemory`  
 <span data-ttu-id="e748d-106">[out] `true` si ce module existe uniquement en mémoire ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="e748d-106">[out] `true` if this module exists only in memory; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e748d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e748d-107">Remarks</span></span>  
 <span data-ttu-id="e748d-108">Le common language runtime (CLR) prend en charge le chargement des modules à partir de flux bruts d’octets.</span><span class="sxs-lookup"><span data-stu-id="e748d-108">The common language runtime (CLR) supports the loading of modules from raw streams of bytes.</span></span> <span data-ttu-id="e748d-109">Ces modules sont appelés *en mémoire modules* et n’existent pas sur le disque.</span><span class="sxs-lookup"><span data-stu-id="e748d-109">Such modules are called *in-memory modules* and do not exist on disk.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e748d-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e748d-110">Requirements</span></span>  
 <span data-ttu-id="e748d-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e748d-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e748d-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e748d-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e748d-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e748d-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e748d-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e748d-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e748d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e748d-115">See also</span></span>
