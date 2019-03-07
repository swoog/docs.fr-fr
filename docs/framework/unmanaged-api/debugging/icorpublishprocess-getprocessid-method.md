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
ms.openlocfilehash: 61c67e074fc32098fa0d8326ea2f0ecfb1efa952
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471766"
---
# <a name="icorpublishprocessgetprocessid-method"></a><span data-ttu-id="191dc-102">ICorPublishProcess::GetProcessID, méthode</span><span class="sxs-lookup"><span data-stu-id="191dc-102">ICorPublishProcess::GetProcessID Method</span></span>
<span data-ttu-id="191dc-103">Obtient l’identificateur de système d’exploitation de ce processus.</span><span class="sxs-lookup"><span data-stu-id="191dc-103">Gets the operating system identifier for this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="191dc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="191dc-104">Syntax</span></span>  
  
```  
HRESULT GetProcessID (  
    [out] unsigned   *pid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="191dc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="191dc-105">Parameters</span></span>  
 `pid`  
 <span data-ttu-id="191dc-106">[out] Un pointeur vers l’identificateur du processus représenté par cet [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="191dc-106">[out] A pointer to the identifier of the process represented by this [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="191dc-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="191dc-107">Requirements</span></span>  
 <span data-ttu-id="191dc-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="191dc-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="191dc-109">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="191dc-109">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="191dc-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="191dc-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="191dc-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="191dc-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="191dc-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="191dc-112">See also</span></span>
- [<span data-ttu-id="191dc-113">ICorPublishProcess, interface</span><span class="sxs-lookup"><span data-stu-id="191dc-113">ICorPublishProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)
