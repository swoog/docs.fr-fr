---
title: ICorPublishAppDomain::GetID, méthode
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomain.GetID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomain::GetID
helpviewer_keywords:
- GetID method, ICorPublishAppDomain interface [.NET Framework debugging]
- ICorPublishAppDomain::GetID method [.NET Framework debugging]
ms.assetid: 229437e3-1465-4bd8-8846-9804b2488133
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6a7541a2093fe877fb84a8a05237f18c4da43c44
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57465983"
---
# <a name="icorpublishappdomaingetid-method"></a><span data-ttu-id="cb740-102">ICorPublishAppDomain::GetID, méthode</span><span class="sxs-lookup"><span data-stu-id="cb740-102">ICorPublishAppDomain::GetID Method</span></span>
<span data-ttu-id="cb740-103">Obtient l’identificateur unique pour ce [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md).</span><span class="sxs-lookup"><span data-stu-id="cb740-103">Gets the unique identifier for this [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cb740-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb740-104">Syntax</span></span>  
  
```  
HRESULT GetID (  
    [out] ULONG32   *puId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cb740-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb740-105">Parameters</span></span>  
 `puId`  
 <span data-ttu-id="cb740-106">[out] Un pointeur vers l’identificateur du domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="cb740-106">[out] A pointer to the identifier of the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cb740-107">Notes</span><span class="sxs-lookup"><span data-stu-id="cb740-107">Remarks</span></span>  
 <span data-ttu-id="cb740-108">L’identificateur est unique seulement dans l’étendue du processus contenant.</span><span class="sxs-lookup"><span data-stu-id="cb740-108">The identifier is unique only in the scope of the containing process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cb740-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cb740-109">Requirements</span></span>  
 <span data-ttu-id="cb740-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cb740-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cb740-111">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="cb740-111">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="cb740-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cb740-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cb740-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cb740-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb740-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb740-114">See also</span></span>
- [<span data-ttu-id="cb740-115">ICorPublishAppDomain, interface</span><span class="sxs-lookup"><span data-stu-id="cb740-115">ICorPublishAppDomain Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md)
