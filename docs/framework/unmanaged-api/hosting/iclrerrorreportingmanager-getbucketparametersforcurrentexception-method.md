---
title: ICLRErrorReportingManager::GetBucketParametersForCurrentException, méthode
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager.GetBucketParametersForCurrentException
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager::GetBucketParametersForCurrentException
helpviewer_keywords:
- ICLRErrorReportingManager::GetBucketParametersForCurrentException method [.NET Framework hosting]
- GetBucketParametersForCurrentException method [.NET Framework hosting]
ms.assetid: a13ec8a6-8e18-4acb-8054-77f5b1a0e0b9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f37bbe7d9e76d76bfe4c0f80b6f2343a5598bbfb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431748"
---
# <a name="iclrerrorreportingmanagergetbucketparametersforcurrentexception-method"></a><span data-ttu-id="20976-102">ICLRErrorReportingManager::GetBucketParametersForCurrentException, méthode</span><span class="sxs-lookup"><span data-stu-id="20976-102">ICLRErrorReportingManager::GetBucketParametersForCurrentException Method</span></span>
<span data-ttu-id="20976-103">Obtient le compartiment Watson de l’exception actuelle sur le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="20976-103">Gets the Watson bucket for the current exception on the calling thread.</span></span>  
  
 <span data-ttu-id="20976-104">A *compartiment* est une collection de données qui sont liées à la même erreur de code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="20976-104">A *bucket* is a collection of error data that is related to the same code defect.</span></span> <span data-ttu-id="20976-105">*Watson* fait référence à un ensemble de technologies de collecte et analyse des données qui sont associées à une exception.</span><span class="sxs-lookup"><span data-stu-id="20976-105">*Watson* refers to a set of technologies for collecting and analyzing data that is associated with an exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20976-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20976-106">Syntax</span></span>  
  
```  
HRESULT GetBucketParametersForCurrentException(  
    [out] BucketParameters *pParams  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="20976-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20976-107">Parameters</span></span>  
 `pParams`  
 <span data-ttu-id="20976-108">[out] Un pointeur vers un [BucketParameters](../../../../docs/framework/unmanaged-api/hosting/bucketparameters-structure.md) structure qui contient les données d’erreur pour l’exception.</span><span class="sxs-lookup"><span data-stu-id="20976-108">[out] A pointer to a [BucketParameters](../../../../docs/framework/unmanaged-api/hosting/bucketparameters-structure.md) structure that contains error data for the exception.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="20976-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="20976-109">Requirements</span></span>  
 <span data-ttu-id="20976-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="20976-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20976-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="20976-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="20976-112">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="20976-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="20976-113">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="20976-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20976-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20976-114">See Also</span></span>  
 [<span data-ttu-id="20976-115">ICLRErrorReportingManager, interface</span><span class="sxs-lookup"><span data-stu-id="20976-115">ICLRErrorReportingManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-interface.md)
