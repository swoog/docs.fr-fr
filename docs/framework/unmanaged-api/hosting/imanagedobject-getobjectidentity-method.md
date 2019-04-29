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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61943511"
---
# <a name="imanagedobjectgetobjectidentity-method"></a><span data-ttu-id="d4027-102">IManagedObject::GetObjectIdentity, méthode</span><span class="sxs-lookup"><span data-stu-id="d4027-102">IManagedObject::GetObjectIdentity Method</span></span>
<span data-ttu-id="d4027-103">Obtient l’identité de cet objet managé.</span><span class="sxs-lookup"><span data-stu-id="d4027-103">Gets the identity of this managed object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d4027-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4027-104">Syntax</span></span>  
  
```  
HRESULT GetObjectIdentity (  
    [out] BSTR*   pBSTRGUID,  
    [out] int*    AppDomainID,  
    [out] CCW_PTR pCCW  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d4027-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4027-105">Parameters</span></span>  
 `pBSTRGUID`  
 <span data-ttu-id="d4027-106">[out] Un pointeur vers le GUID du processus dans lequel réside l’objet.</span><span class="sxs-lookup"><span data-stu-id="d4027-106">[out] A pointer to the GUID of the process in which the object resides.</span></span>  
  
 `AppDomainID`  
 <span data-ttu-id="d4027-107">[out] Pointeur vers l’ID de l’objet domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="d4027-107">[out] A pointer to the ID of the object's application domain.</span></span>  
  
 `pCCW`  
 <span data-ttu-id="d4027-108">[out] Pointeur vers l’index de l’objet dans la v-table classique COM.</span><span class="sxs-lookup"><span data-stu-id="d4027-108">[out] A pointer to object's index in the COM classic v-table.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d4027-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d4027-109">Remarks</span></span>  
 <span data-ttu-id="d4027-110">L’identité d’un objet managé inclut les GUID du processus, les ID de domaine d’application et les index de l’objet dans la v-table classique COM.</span><span class="sxs-lookup"><span data-stu-id="d4027-110">The identity of a managed object includes process GUID, application domain ID, and the object's index in the COM classic v-table.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d4027-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4027-111">Requirements</span></span>  
 <span data-ttu-id="d4027-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d4027-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d4027-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="d4027-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d4027-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d4027-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d4027-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d4027-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4027-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4027-116">See also</span></span>

- [<span data-ttu-id="d4027-117">IManagedObject, interface</span><span class="sxs-lookup"><span data-stu-id="d4027-117">IManagedObject Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/imanagedobject-interface.md)
