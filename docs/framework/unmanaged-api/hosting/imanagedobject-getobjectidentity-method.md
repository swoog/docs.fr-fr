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
ms.openlocfilehash: 6d014d2900ea790f84331ed933143513ae9e63f7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59213491"
---
# <a name="imanagedobjectgetobjectidentity-method"></a><span data-ttu-id="6944e-102">IManagedObject::GetObjectIdentity, méthode</span><span class="sxs-lookup"><span data-stu-id="6944e-102">IManagedObject::GetObjectIdentity Method</span></span>
<span data-ttu-id="6944e-103">Obtient l’identité de cet objet managé.</span><span class="sxs-lookup"><span data-stu-id="6944e-103">Gets the identity of this managed object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6944e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6944e-104">Syntax</span></span>  
  
```  
HRESULT GetObjectIdentity (  
    [out] BSTR*   pBSTRGUID,  
    [out] int*    AppDomainID,  
    [out] CCW_PTR pCCW  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6944e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6944e-105">Parameters</span></span>  
 `pBSTRGUID`  
 <span data-ttu-id="6944e-106">[out] Un pointeur vers le GUID du processus dans lequel réside l’objet.</span><span class="sxs-lookup"><span data-stu-id="6944e-106">[out] A pointer to the GUID of the process in which the object resides.</span></span>  
  
 `AppDomainID`  
 <span data-ttu-id="6944e-107">[out] Pointeur vers l’ID de l’objet domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="6944e-107">[out] A pointer to the ID of the object's application domain.</span></span>  
  
 `pCCW`  
 <span data-ttu-id="6944e-108">[out] Pointeur vers l’index de l’objet dans la v-table classique COM.</span><span class="sxs-lookup"><span data-stu-id="6944e-108">[out] A pointer to object's index in the COM classic v-table.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6944e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="6944e-109">Remarks</span></span>  
 <span data-ttu-id="6944e-110">L’identité d’un objet managé inclut les GUID du processus, les ID de domaine d’application et les index de l’objet dans la v-table classique COM.</span><span class="sxs-lookup"><span data-stu-id="6944e-110">The identity of a managed object includes process GUID, application domain ID, and the object's index in the COM classic v-table.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6944e-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6944e-111">Requirements</span></span>  
 <span data-ttu-id="6944e-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6944e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6944e-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6944e-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6944e-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6944e-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="6944e-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="6944e-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="6944e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6944e-116">See also</span></span>

- [<span data-ttu-id="6944e-117">IManagedObject, interface</span><span class="sxs-lookup"><span data-stu-id="6944e-117">IManagedObject Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/imanagedobject-interface.md)
