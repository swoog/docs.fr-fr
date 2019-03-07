---
title: IManagedObject::GetObjectIdentity, méthode
ms.date: 03/30/2017
api_name:
- IManagedObject.GetObjectIdentity
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetObjectIdentity
helpviewer_keywords:
- GetObjectIdentity method [.NET Framework hosting]
- IManagedObject::GetObjectIdentity method [.NET Framework hosting]
ms.assetid: b862ff3e-e480-4cdf-84e2-e1013334a467
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4d825a0c67f88e1f37023feb96a217b115653056
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57496935"
---
# <a name="imanagedobjectgetobjectidentity-method"></a><span data-ttu-id="abbf4-102">IManagedObject::GetObjectIdentity, méthode</span><span class="sxs-lookup"><span data-stu-id="abbf4-102">IManagedObject::GetObjectIdentity Method</span></span>
<span data-ttu-id="abbf4-103">Obtient l’identité de cet objet managé.</span><span class="sxs-lookup"><span data-stu-id="abbf4-103">Gets the identity of this managed object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="abbf4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abbf4-104">Syntax</span></span>  
  
```  
HRESULT GetObjectIdentity (  
    [out] BSTR*   pBSTRGUID,  
    [out] int*    AppDomainID,  
    [out] CCW_PTR pCCW  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="abbf4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abbf4-105">Parameters</span></span>  
 `pBSTRGUID`  
 <span data-ttu-id="abbf4-106">[out] Un pointeur vers le GUID du processus dans lequel réside l’objet.</span><span class="sxs-lookup"><span data-stu-id="abbf4-106">[out] A pointer to the GUID of the process in which the object resides.</span></span>  
  
 `AppDomainID`  
 <span data-ttu-id="abbf4-107">[out] Pointeur vers l’ID de l’objet domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="abbf4-107">[out] A pointer to the ID of the object's application domain.</span></span>  
  
 `pCCW`  
 <span data-ttu-id="abbf4-108">[out] Pointeur vers l’index de l’objet dans la v-table classique COM.</span><span class="sxs-lookup"><span data-stu-id="abbf4-108">[out] A pointer to object's index in the COM classic v-table.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="abbf4-109">Notes</span><span class="sxs-lookup"><span data-stu-id="abbf4-109">Remarks</span></span>  
 <span data-ttu-id="abbf4-110">L’identité d’un objet managé inclut les GUID du processus, les ID de domaine d’application et les index de l’objet dans la v-table classique COM.</span><span class="sxs-lookup"><span data-stu-id="abbf4-110">The identity of a managed object includes process GUID, application domain ID, and the object's index in the COM classic v-table.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="abbf4-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="abbf4-111">Requirements</span></span>  
 <span data-ttu-id="abbf4-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="abbf4-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="abbf4-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="abbf4-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="abbf4-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="abbf4-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="abbf4-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="abbf4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="abbf4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abbf4-116">See also</span></span>
- [<span data-ttu-id="abbf4-117">IManagedObject, interface</span><span class="sxs-lookup"><span data-stu-id="abbf4-117">IManagedObject Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/imanagedobject-interface.md)
