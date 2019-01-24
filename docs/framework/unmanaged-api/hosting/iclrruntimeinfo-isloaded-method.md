---
title: ICLRRuntimeInfo::IsLoaded, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.IsLoaded
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::IsLoaded
helpviewer_keywords:
- IsLoaded method [.NET Framework hosting]
- ICLRRuntimeInfo::IsLoaded method [.NET Framework hosting]
ms.assetid: fdc5a3a7-71ff-4025-99a1-59e4ee0bfe1b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 69a3b0921528ed09ee4ab3a1ede6b9efe565e02a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54619223"
---
# <a name="iclrruntimeinfoisloaded-method"></a><span data-ttu-id="7c6a3-102">ICLRRuntimeInfo::IsLoaded, méthode</span><span class="sxs-lookup"><span data-stu-id="7c6a3-102">ICLRRuntimeInfo::IsLoaded Method</span></span>
<span data-ttu-id="7c6a3-103">Indique si le common language runtime (CLR) associé à la [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface est chargée dans un processus.</span><span class="sxs-lookup"><span data-stu-id="7c6a3-103">Indicates whether the common language runtime (CLR) associated with the [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface is loaded into a process.</span></span> <span data-ttu-id="7c6a3-104">Un runtime peut être chargé sans également en cours de démarrage.</span><span class="sxs-lookup"><span data-stu-id="7c6a3-104">A runtime can be loaded without also being started.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7c6a3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c6a3-105">Syntax</span></span>  
  
```  
HRESULT IsLoaded(  
[in]  HANDLE hndProcess,  
[out, retval] BOOL *pbLoaded);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7c6a3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c6a3-106">Parameters</span></span>  
 `hndProcess`  
 <span data-ttu-id="7c6a3-107">[in] Handle vers le processus.</span><span class="sxs-lookup"><span data-stu-id="7c6a3-107">[in] A handle to the process.</span></span>  
  
 `pbLoaded`  
 <span data-ttu-id="7c6a3-108">[out] `true` si le CLR est chargé dans le processus ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="7c6a3-108">[out] `true` if the CLR is loaded into the process; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7c6a3-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7c6a3-109">Return Value</span></span>  
 <span data-ttu-id="7c6a3-110">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="7c6a3-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="7c6a3-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7c6a3-111">HRESULT</span></span>|<span data-ttu-id="7c6a3-112">Description</span><span class="sxs-lookup"><span data-stu-id="7c6a3-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7c6a3-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c6a3-113">S_OK</span></span>|<span data-ttu-id="7c6a3-114">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="7c6a3-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="7c6a3-115">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="7c6a3-115">E_POINTER</span></span>|<span data-ttu-id="7c6a3-116">`pbLoaded` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="7c6a3-116">`pbLoaded` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7c6a3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="7c6a3-117">Remarks</span></span>  
 <span data-ttu-id="7c6a3-118">Cette méthode est à compatibilité descendante avec les fonctions et les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="7c6a3-118">This method is backward-compatible with the following functions and interfaces:</span></span>  
  
-   <span data-ttu-id="7c6a3-119">[ICorRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md) interface (dans l’API d’hébergement .NET Framework version 1).</span><span class="sxs-lookup"><span data-stu-id="7c6a3-119">[ICorRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md) interface (in the .NET Framework version 1 hosting API).</span></span>  
  
-   <span data-ttu-id="7c6a3-120">[ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md) interface (dans l’API d’hébergement .NET Framework 2.0).</span><span class="sxs-lookup"><span data-stu-id="7c6a3-120">[ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md) interface (in the .NET Framework 2.0 hosting API).</span></span>  
  
-   <span data-ttu-id="7c6a3-121">Deprecated `CorBindTo*` fonctions (voir [déconseillée fonctions d’hébergement CLR](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md) dans l’API d’hébergement .NET Framework 2.0).</span><span class="sxs-lookup"><span data-stu-id="7c6a3-121">Deprecated `CorBindTo*` functions (see [Deprecated CLR Hosting Functions](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md) in the .NET Framework 2.0 hosting API).</span></span>  
  
 <span data-ttu-id="7c6a3-122">Un hôte peut appeler une des déconseillées `CorBindTo*` fonctions, telles que la [CorBindToRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md) fonction, pour instancier une version spécifique du CLR.</span><span class="sxs-lookup"><span data-stu-id="7c6a3-122">A host may call one of the deprecated `CorBindTo*` functions, such as the [CorBindToRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md) function, to instantiate a specific version of the CLR.</span></span> <span data-ttu-id="7c6a3-123">L’hôte peut ensuite appeler la [ICLRMetaHost::GetRuntime](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-getruntime-method.md) (méthode) et spécifiez le même numéro de version pour obtenir un [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="7c6a3-123">The host could then call the [ICLRMetaHost::GetRuntime](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-getruntime-method.md) method and specify the same version number to obtain a [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span></span>  
  
 <span data-ttu-id="7c6a3-124">Si l’hôte appelle ensuite la `IsLoaded` méthode sur retourné [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface, `pbLoaded` retourne `true`; sinon, elle retourne `false`.</span><span class="sxs-lookup"><span data-stu-id="7c6a3-124">If the host then calls the `IsLoaded` method on the returned [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface, `pbLoaded` returns `true`; otherwise, it returns `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7c6a3-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7c6a3-125">Requirements</span></span>  
 <span data-ttu-id="7c6a3-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7c6a3-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7c6a3-127">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="7c6a3-127">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="7c6a3-128">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7c6a3-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7c6a3-129">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7c6a3-129">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c6a3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c6a3-130">See also</span></span>
- [<span data-ttu-id="7c6a3-131">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="7c6a3-131">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)
- [<span data-ttu-id="7c6a3-132">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="7c6a3-132">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="7c6a3-133">Hébergement</span><span class="sxs-lookup"><span data-stu-id="7c6a3-133">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
