---
title: ICorPublishProcess::GetProcessID, méthode
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.GetProcessID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::GetProcessID
helpviewer_keywords:
- ICorPublishProcess::GetProcessID method [.NET Framework debugging]
- GetProcessID method [.NET Framework debugging]
ms.assetid: f31185e0-f01d-463a-b392-42163e39bfe9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 91e1697366bd3ee95fd040ee261d68417a8125e3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33423606"
---
# <a name="icorpublishprocessgetprocessid-method"></a><span data-ttu-id="c1336-102">ICorPublishProcess::GetProcessID, méthode</span><span class="sxs-lookup"><span data-stu-id="c1336-102">ICorPublishProcess::GetProcessID Method</span></span>
<span data-ttu-id="c1336-103">Obtient l’identificateur de système d’exploitation de ce processus.</span><span class="sxs-lookup"><span data-stu-id="c1336-103">Gets the operating system identifier for this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c1336-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1336-104">Syntax</span></span>  
  
```  
HRESULT GetProcessID (  
    [out] unsigned   *pid  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c1336-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1336-105">Parameters</span></span>  
 `pid`  
 <span data-ttu-id="c1336-106">[out] Un pointeur vers l’identificateur du processus représenté par ce [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="c1336-106">[out] A pointer to the identifier of the process represented by this [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c1336-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c1336-107">Requirements</span></span>  
 <span data-ttu-id="c1336-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c1336-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c1336-109">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="c1336-109">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="c1336-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c1336-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c1336-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c1336-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1336-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1336-112">See Also</span></span>  
 [<span data-ttu-id="c1336-113">ICorPublishProcess, interface</span><span class="sxs-lookup"><span data-stu-id="c1336-113">ICorPublishProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)
