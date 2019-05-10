---
title: IHostSecurityManager, interface
ms.date: 03/30/2017
api_name:
- IHostSecurityManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityManager
helpviewer_keywords:
- IHostSecurityManager interface [.NET Framework hosting]
ms.assetid: c3be2cbd-2d93-438b-9888-9a0251b63c03
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a2c71f32dfd190e188bb28aad5d51c72160eb4bc
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64603233"
---
# <a name="ihostsecuritymanager-interface"></a><span data-ttu-id="3886c-102">IHostSecurityManager, interface</span><span class="sxs-lookup"><span data-stu-id="3886c-102">IHostSecurityManager Interface</span></span>
<span data-ttu-id="3886c-103">Fournit des méthodes qui permettent l’accès et contrôle sur le contexte de sécurité du thread en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3886c-103">Provides methods that allow access to and control over the security context of the currently executing thread.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3886c-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3886c-104">Methods</span></span>  
  
|<span data-ttu-id="3886c-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="3886c-105">Method</span></span>|<span data-ttu-id="3886c-106">Description</span><span class="sxs-lookup"><span data-stu-id="3886c-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3886c-107">GetSecurityContext, méthode</span><span class="sxs-lookup"><span data-stu-id="3886c-107">GetSecurityContext Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md)|<span data-ttu-id="3886c-108">Obtient le texte demandé [IHostSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md) à partir de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="3886c-108">Gets the requested [IHostSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md) from the host.</span></span>|  
|[<span data-ttu-id="3886c-109">ImpersonateLoggedOnUser, méthode</span><span class="sxs-lookup"><span data-stu-id="3886c-109">ImpersonateLoggedOnUser Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-impersonateloggedonuser-method.md)|<span data-ttu-id="3886c-110">Les demandes qui code être exécutée en utilisant les informations d’identification de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="3886c-110">Requests that code be executed using the credentials of the current user identity.</span></span>|  
|[<span data-ttu-id="3886c-111">OpenThreadToken, méthode</span><span class="sxs-lookup"><span data-stu-id="3886c-111">OpenThreadToken Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-openthreadtoken-method.md)|<span data-ttu-id="3886c-112">Ouvre le jeton d’accès discrétionnaire associé au thread actuel.</span><span class="sxs-lookup"><span data-stu-id="3886c-112">Opens the discretionary access token associated with the current thread.</span></span>|  
|[<span data-ttu-id="3886c-113">RevertToSelf, méthode</span><span class="sxs-lookup"><span data-stu-id="3886c-113">RevertToSelf Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-reverttoself-method.md)|<span data-ttu-id="3886c-114">Termine l’emprunt d’identité de l’utilisateur actuel et retourne le jeton de thread d’origine.</span><span class="sxs-lookup"><span data-stu-id="3886c-114">Terminates impersonation of the current user identity and returns the original thread token.</span></span>|  
|[<span data-ttu-id="3886c-115">SetSecurityContext, méthode</span><span class="sxs-lookup"><span data-stu-id="3886c-115">SetSecurityContext Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-setsecuritycontext-method.md)|<span data-ttu-id="3886c-116">Définit le contexte de sécurité pour le thread en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3886c-116">Sets the security context for the currently executing thread.</span></span>|  
|[<span data-ttu-id="3886c-117">SetThreadToken, méthode</span><span class="sxs-lookup"><span data-stu-id="3886c-117">SetThreadToken Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-setthreadtoken-method.md)|<span data-ttu-id="3886c-118">Définit un handle pour le thread en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3886c-118">Sets a handle for the currently executing thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3886c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="3886c-119">Remarks</span></span>  
 <span data-ttu-id="3886c-120">Un hôte peut contrôler tous les accès de code aux jetons de thread par le common language runtime (CLR) et le code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3886c-120">A host can control all code access to thread tokens by both the common language runtime (CLR) and user code.</span></span> <span data-ttu-id="3886c-121">Il peut également garantir que la sécurité complète des informations de contexte sont passées aux opérations asynchrones ou des points de code avec accès restreint au code.</span><span class="sxs-lookup"><span data-stu-id="3886c-121">It can also ensure that complete security context information is passed across asynchronous operations or code points with restricted code access.</span></span> <span data-ttu-id="3886c-122">`IHostSecurityContext` encapsule ces informations de contexte de sécurité, qui sont opaques pour le CLR.</span><span class="sxs-lookup"><span data-stu-id="3886c-122">`IHostSecurityContext` encapsulates this security context information, which is opaque to the CLR.</span></span>  
  
 <span data-ttu-id="3886c-123">Le CLR gère le contexte de thread managé en interne.</span><span class="sxs-lookup"><span data-stu-id="3886c-123">The CLR handles managed thread context internally.</span></span> <span data-ttu-id="3886c-124">Elle interroge les processus spécifiques `IHostSecurityManager` dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3886c-124">It queries the process-specific `IHostSecurityManager` in the following situations:</span></span>  
  
- <span data-ttu-id="3886c-125">Sur le thread finaliseur, pendant l’exécution du finaliseur.</span><span class="sxs-lookup"><span data-stu-id="3886c-125">On the finalizer thread, during finalizer execution.</span></span>  
  
- <span data-ttu-id="3886c-126">Pendant l’exécution de constructeur de classe et le module.</span><span class="sxs-lookup"><span data-stu-id="3886c-126">During class and module constructor execution.</span></span>  
  
- <span data-ttu-id="3886c-127">Aux points asynchrones sur le thread de travail, dans les appels à la [IHostThreadPoolManager::QueueUserWorkItem](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-queueuserworkitem-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="3886c-127">At asynchronous points on the worker thread, in calls to the [IHostThreadPoolManager::QueueUserWorkItem](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-queueuserworkitem-method.md) method.</span></span>  
  
- <span data-ttu-id="3886c-128">Prise en charge des ports de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="3886c-128">In servicing of I/O completion ports.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3886c-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3886c-129">Requirements</span></span>  
 <span data-ttu-id="3886c-130">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3886c-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3886c-131">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3886c-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3886c-132">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3886c-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3886c-133">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3886c-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3886c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3886c-134">See also</span></span>

- [<span data-ttu-id="3886c-135">IHostSecurityContext, interface</span><span class="sxs-lookup"><span data-stu-id="3886c-135">IHostSecurityContext Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md)
- [<span data-ttu-id="3886c-136">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="3886c-136">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
