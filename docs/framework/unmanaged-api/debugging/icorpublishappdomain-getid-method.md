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
ms.openlocfilehash: 41b39597a5a438592d2ae07a16510f5406a91a43
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33422830"
---
# <a name="icorpublishappdomaingetid-method"></a><span data-ttu-id="1fdb5-102">ICorPublishAppDomain::GetID, méthode</span><span class="sxs-lookup"><span data-stu-id="1fdb5-102">ICorPublishAppDomain::GetID Method</span></span>
<span data-ttu-id="1fdb5-103">Obtient l’identificateur unique pour ce [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md).</span><span class="sxs-lookup"><span data-stu-id="1fdb5-103">Gets the unique identifier for this [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1fdb5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fdb5-104">Syntax</span></span>  
  
```  
HRESULT GetID (  
    [out] ULONG32   *puId  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1fdb5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fdb5-105">Parameters</span></span>  
 `puId`  
 <span data-ttu-id="1fdb5-106">[out] Pointeur vers l’identificateur du domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="1fdb5-106">[out] A pointer to the identifier of the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1fdb5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1fdb5-107">Remarks</span></span>  
 <span data-ttu-id="1fdb5-108">L’identificateur est unique seulement dans l’étendue du processus contenant.</span><span class="sxs-lookup"><span data-stu-id="1fdb5-108">The identifier is unique only in the scope of the containing process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1fdb5-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1fdb5-109">Requirements</span></span>  
 <span data-ttu-id="1fdb5-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1fdb5-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1fdb5-111">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="1fdb5-111">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="1fdb5-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1fdb5-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1fdb5-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1fdb5-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1fdb5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fdb5-114">See Also</span></span>  
 [<span data-ttu-id="1fdb5-115">ICorPublishAppDomain, interface</span><span class="sxs-lookup"><span data-stu-id="1fdb5-115">ICorPublishAppDomain Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md)
