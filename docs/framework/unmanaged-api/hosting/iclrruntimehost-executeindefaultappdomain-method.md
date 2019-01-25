---
title: ICLRRuntimeHost::ExecuteInDefaultAppDomain, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.ExecuteInDefaultAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::ExecuteInDefaultAppDomain
helpviewer_keywords:
- ICLRRuntimeHost::ExecuteInDefaultAppDomain method [.NET Framework hosting]
- ExecuteInDefaultAppDomain method [.NET Framework hosting]
ms.assetid: 30b5cf9a-a762-4bd4-be12-d6c1442b78b1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ae7bbc41d0e2cca1cf25a5ec34535b20fc9163d1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498253"
---
# <a name="iclrruntimehostexecuteindefaultappdomain-method"></a><span data-ttu-id="1c742-102">ICLRRuntimeHost::ExecuteInDefaultAppDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="1c742-102">ICLRRuntimeHost::ExecuteInDefaultAppDomain Method</span></span>
<span data-ttu-id="1c742-103">Appelle la méthode spécifiée du type spécifié dans l’assembly managé spécifié.</span><span class="sxs-lookup"><span data-stu-id="1c742-103">Calls the specified method of the specified type in the specified managed assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1c742-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c742-104">Syntax</span></span>  
  
```  
HRESULT ExecuteInDefaultAppDomain (  
    [in] LPCWSTR pwzAssemblyPath,  
    [in] LPCWSTR pwzTypeName,   
    [in] LPCWSTR pwzMethodName,  
    [in] LPCWSTR pwzArgument,  
    [out] DWORD *pReturnValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1c742-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c742-105">Parameters</span></span>  
 `pwzAssemblyPath`  
 <span data-ttu-id="1c742-106">[in] Le chemin d’accès à la <xref:System.Reflection.Assembly> qui définit le <xref:System.Type> dont la méthode doit être appelée.</span><span class="sxs-lookup"><span data-stu-id="1c742-106">[in] The path to the <xref:System.Reflection.Assembly> that defines the <xref:System.Type> whose method is to be invoked.</span></span>  
  
 `pwzTypeName`  
 <span data-ttu-id="1c742-107">[in] Le nom de la <xref:System.Type> qui définit la méthode à appeler.</span><span class="sxs-lookup"><span data-stu-id="1c742-107">[in] The name of the <xref:System.Type> that defines the method to invoke.</span></span>  
  
 `pwzMethodName`  
 <span data-ttu-id="1c742-108">[in] Le nom de la méthode à appeler.</span><span class="sxs-lookup"><span data-stu-id="1c742-108">[in] The name of the method to invoke.</span></span>  
  
 `pwzArgument`  
 <span data-ttu-id="1c742-109">[in] Le paramètre de chaîne à passer à la méthode.</span><span class="sxs-lookup"><span data-stu-id="1c742-109">[in] The string parameter to pass to the method.</span></span>  
  
 `pReturnValue`  
 <span data-ttu-id="1c742-110">[out] La valeur entière retournée par la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="1c742-110">[out] The integer value returned by the invoked method.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1c742-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1c742-111">Return Value</span></span>  
  
|<span data-ttu-id="1c742-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1c742-112">HRESULT</span></span>|<span data-ttu-id="1c742-113">Description</span><span class="sxs-lookup"><span data-stu-id="1c742-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1c742-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="1c742-114">S_OK</span></span>|<span data-ttu-id="1c742-115">`ExecuteInDefaultAppDomain` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="1c742-115">`ExecuteInDefaultAppDomain` returned successfully.</span></span>|  
|<span data-ttu-id="1c742-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="1c742-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="1c742-117">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="1c742-117">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="1c742-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="1c742-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="1c742-119">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="1c742-119">The call timed out.</span></span>|  
|<span data-ttu-id="1c742-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="1c742-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="1c742-121">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="1c742-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="1c742-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="1c742-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="1c742-123">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="1c742-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="1c742-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="1c742-124">E_FAIL</span></span>|<span data-ttu-id="1c742-125">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1c742-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="1c742-126">Si une méthode retourne E_FAIL, la liste de révocation n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="1c742-126">If a method returns E_FAIL, the CRL is no longer usable within the process.</span></span> <span data-ttu-id="1c742-127">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="1c742-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1c742-128">Notes</span><span class="sxs-lookup"><span data-stu-id="1c742-128">Remarks</span></span>  
 <span data-ttu-id="1c742-129">La méthode appelée doit avoir la signature suivante :</span><span class="sxs-lookup"><span data-stu-id="1c742-129">The invoked method must have the following signature:</span></span>  
  
```  
static int pwzMethodName (String pwzArgument)  
```  
  
 <span data-ttu-id="1c742-130">où `pwzMethodName` représente le nom de la méthode appelée, et `pwzArgument` représente la valeur de chaîne passée en tant que paramètre à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1c742-130">where `pwzMethodName` represents the name of the invoked method, and `pwzArgument` represents the string value passed as a parameter to that method.</span></span> <span data-ttu-id="1c742-131">Si la valeur HRESULT est définie à S_OK, `pReturnValue` est définie sur la valeur entière retournée par la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="1c742-131">If the HRESULT value is set to S_OK, `pReturnValue` is set to the integer value returned by the invoked method.</span></span> <span data-ttu-id="1c742-132">Sinon, `pReturnValue` n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="1c742-132">Otherwise, `pReturnValue` is not set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1c742-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1c742-133">Requirements</span></span>  
 <span data-ttu-id="1c742-134">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1c742-134">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1c742-135">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1c742-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1c742-136">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1c742-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1c742-137">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1c742-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c742-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c742-138">See also</span></span>
- [<span data-ttu-id="1c742-139">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="1c742-139">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
