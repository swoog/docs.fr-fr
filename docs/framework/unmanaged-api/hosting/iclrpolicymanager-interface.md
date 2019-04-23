---
title: ICLRPolicyManager, interface
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager
helpviewer_keywords:
- ICLRPolicyManager interface [.NET Framework hosting]
ms.assetid: 5c834aa1-f2db-408a-b230-c7bec093d364
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2eeccc4dfd7a7147fe791444eeeca2bd3a844305
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59211040"
---
# <a name="iclrpolicymanager-interface"></a><span data-ttu-id="bcd6d-102">ICLRPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="bcd6d-102">ICLRPolicyManager Interface</span></span>
<span data-ttu-id="bcd6d-103">Fournit des méthodes qui permettent à l’hôte spécifier les actions à entreprendre en cas de défaillances et des délais d’expiration de stratégie.</span><span class="sxs-lookup"><span data-stu-id="bcd6d-103">Provides methods that allow the host to specify policy actions to be taken in the event of failures and timeouts.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="bcd6d-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bcd6d-104">Methods</span></span>  
  
|<span data-ttu-id="bcd6d-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="bcd6d-105">Method</span></span>|<span data-ttu-id="bcd6d-106">Description</span><span class="sxs-lookup"><span data-stu-id="bcd6d-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="bcd6d-107">SetActionOnFailure, méthode</span><span class="sxs-lookup"><span data-stu-id="bcd6d-107">SetActionOnFailure Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactiononfailure-method.md)|<span data-ttu-id="bcd6d-108">Spécifie l’action de stratégie que le common language runtime (CLR) doit prendre en cas d’échec spécifié.</span><span class="sxs-lookup"><span data-stu-id="bcd6d-108">Specifies the policy action the common language runtime (CLR) should take when the specified failure occurs.</span></span>|  
|[<span data-ttu-id="bcd6d-109">SetActionOnTimeout, méthode</span><span class="sxs-lookup"><span data-stu-id="bcd6d-109">SetActionOnTimeout Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactionontimeout-method.md)|<span data-ttu-id="bcd6d-110">Spécifie l’action de stratégie que le CLR doit prendre lorsque l’opération spécifiée arrive à expiration.</span><span class="sxs-lookup"><span data-stu-id="bcd6d-110">Specifies the policy action the CLR should take when the specified operation times out.</span></span>|  
|[<span data-ttu-id="bcd6d-111">SetDefaultAction, méthode</span><span class="sxs-lookup"><span data-stu-id="bcd6d-111">SetDefaultAction Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setdefaultaction-method.md)|<span data-ttu-id="bcd6d-112">Spécifie l’action de stratégie que le CLR doit prendre lorsque l’opération spécifiée se produit.</span><span class="sxs-lookup"><span data-stu-id="bcd6d-112">Specifies the policy action the CLR should take when the specified operation occurs.</span></span>|  
|[<span data-ttu-id="bcd6d-113">SetTimeout, méthode</span><span class="sxs-lookup"><span data-stu-id="bcd6d-113">SetTimeout Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-settimeout-method.md)|<span data-ttu-id="bcd6d-114">Définit une valeur de délai d’attente pour l’opération spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcd6d-114">Sets a timeout value for the specified operation.</span></span>|  
|[<span data-ttu-id="bcd6d-115">SetTimeoutAndAction, méthode</span><span class="sxs-lookup"><span data-stu-id="bcd6d-115">SetTimeoutAndAction Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-settimeoutandaction-method.md)|<span data-ttu-id="bcd6d-116">Définit une valeur de délai d’attente pour l’opération spécifiée et spécifie l’action de stratégie que le CLR doit prendre lorsque l’opération se produit.</span><span class="sxs-lookup"><span data-stu-id="bcd6d-116">Sets a timeout value for the specified operation, and specifies the policy action the CLR should take when the operation occurs.</span></span>|  
|[<span data-ttu-id="bcd6d-117">SetUnhandledExceptionPolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="bcd6d-117">SetUnhandledExceptionPolicy Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setunhandledexceptionpolicy-method.md)|<span data-ttu-id="bcd6d-118">Spécifie le comportement du CLR lorsqu’une exception non gérée se produit.</span><span class="sxs-lookup"><span data-stu-id="bcd6d-118">Specifies the behavior of the CLR when an unhandled exception occurs.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="bcd6d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcd6d-119">Requirements</span></span>  
 <span data-ttu-id="bcd6d-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bcd6d-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bcd6d-121">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="bcd6d-121">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bcd6d-122">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bcd6d-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bcd6d-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bcd6d-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bcd6d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcd6d-124">See also</span></span>

- [<span data-ttu-id="bcd6d-125">EClrFailure, énumération</span><span class="sxs-lookup"><span data-stu-id="bcd6d-125">EClrFailure Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)
- [<span data-ttu-id="bcd6d-126">EClrOperation, énumération</span><span class="sxs-lookup"><span data-stu-id="bcd6d-126">EClrOperation Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)
- [<span data-ttu-id="bcd6d-127">EPolicyAction, énumération</span><span class="sxs-lookup"><span data-stu-id="bcd6d-127">EPolicyAction Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)
- [<span data-ttu-id="bcd6d-128">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="bcd6d-128">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
