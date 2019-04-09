---
title: ICLRMetaHost::GetRuntime, méthode
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.GetRuntime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::GetRuntime
helpviewer_keywords:
- GetRuntime method [.NET Framework hosting]
- ICLRMetaHost::GetRuntime method [.NET Framework hosting]
ms.assetid: a10749f1-ab91-47cf-982f-d8ccd2e81bd2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8b71d0f29d770b2722b0dfaabc8b9667e524c99e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59207602"
---
# <a name="iclrmetahostgetruntime-method"></a><span data-ttu-id="86cd0-102">ICLRMetaHost::GetRuntime, méthode</span><span class="sxs-lookup"><span data-stu-id="86cd0-102">ICLRMetaHost::GetRuntime Method</span></span>
<span data-ttu-id="86cd0-103">Obtient le [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface qui correspond à une version particulière du common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="86cd0-103">Gets the [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface that corresponds to a particular version of the common language runtime (CLR).</span></span> <span data-ttu-id="86cd0-104">Cette méthode remplace la [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) fonction utilisée avec le [STARTUP_LOADER_SAFEMODE](../../../../docs/framework/unmanaged-api/hosting/startup-flags-enumeration.md) indicateur.</span><span class="sxs-lookup"><span data-stu-id="86cd0-104">This method supersedes the [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) function used with the [STARTUP_LOADER_SAFEMODE](../../../../docs/framework/unmanaged-api/hosting/startup-flags-enumeration.md) flag.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86cd0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86cd0-105">Syntax</span></span>  
  
```  
HRESULT GetRuntime (  
    [in] LPCWSTR pwzVersion,  
    [in, REFIID riid,  
    [out,iid_is(riid), retval] LPVOID *ppRuntime  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="86cd0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86cd0-106">Parameters</span></span>  
 `pwzVersion`  
 <span data-ttu-id="86cd0-107">[in] La version de compilation .NET Framework stockée dans les métadonnées, au format « v*A*. *B*[. *X*] ».</span><span class="sxs-lookup"><span data-stu-id="86cd0-107">[in] The .NET Framework compilation version stored in the metadata, in the format "v*A*.*B*[.*X*]".</span></span> <span data-ttu-id="86cd0-108">*Un*, *B*, et *X* sont des nombres décimaux qui correspondent à la version principale, la version secondaire et le numéro de build.</span><span class="sxs-lookup"><span data-stu-id="86cd0-108">*A*, *B*, and *X* are decimal numbers that correspond to the major version, the minor version, and the build number.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="86cd0-109">Ce paramètre doit correspondre au nom de répertoire pour la version de .NET Framework, tel qu’il apparaît sous C:\Windows\Microsoft.NET\Framework ou C:\Windows\Microsoft.NET\Framework64.</span><span class="sxs-lookup"><span data-stu-id="86cd0-109">This parameter must match the directory name for the .NET Framework version, as it appears under C:\Windows\Microsoft.NET\Framework or C:\Windows\Microsoft.NET\Framework64.</span></span>  
  
 <span data-ttu-id="86cd0-110">Exemples de valeurs : « v1.0.3705 », « v1.1.4322 », « v2.0.50727 » et « v4.0. *X*», où *X* varie selon le numéro de build installé.</span><span class="sxs-lookup"><span data-stu-id="86cd0-110">Example values are "v1.0.3705", "v1.1.4322", "v2.0.50727", and "v4.0.*X*", where *X* depends on the build number installed.</span></span> <span data-ttu-id="86cd0-111">Le préfixe « v » est requis.</span><span class="sxs-lookup"><span data-stu-id="86cd0-111">The "v" prefix is required.</span></span>  
  
 `riid`  
 <span data-ttu-id="86cd0-112">[in] L’identificateur de l’interface souhaitée.</span><span class="sxs-lookup"><span data-stu-id="86cd0-112">[in] The identifier for the desired interface.</span></span> <span data-ttu-id="86cd0-113">Actuellement, la seule valeur valide pour ce paramètre est IID_ICLRRuntimeInfo.</span><span class="sxs-lookup"><span data-stu-id="86cd0-113">Currently, the only valid value for this parameter is IID_ICLRRuntimeInfo.</span></span>  
  
 `ppRuntime`  
 <span data-ttu-id="86cd0-114">[out] Un pointeur vers le [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface qui correspond au runtime demandé.</span><span class="sxs-lookup"><span data-stu-id="86cd0-114">[out] A pointer to the [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface that corresponds to the requested runtime.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="86cd0-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="86cd0-115">Return Value</span></span>  
 <span data-ttu-id="86cd0-116">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="86cd0-116">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="86cd0-117">HRESULT</span><span class="sxs-lookup"><span data-stu-id="86cd0-117">HRESULT</span></span>|<span data-ttu-id="86cd0-118">Description</span><span class="sxs-lookup"><span data-stu-id="86cd0-118">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="86cd0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="86cd0-119">S_OK</span></span>|<span data-ttu-id="86cd0-120">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="86cd0-120">The method completed successfully.</span></span>|  
|<span data-ttu-id="86cd0-121">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="86cd0-121">E_POINTER</span></span>|`pwzVersion` <span data-ttu-id="86cd0-122">ou `ppRuntime` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="86cd0-122">or `ppRuntime` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="86cd0-123">Notes</span><span class="sxs-lookup"><span data-stu-id="86cd0-123">Remarks</span></span>  
 <span data-ttu-id="86cd0-124">Cette méthode interagit régulièrement avec les interfaces héritées telles que la [ICorRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md) interface et les fonctions héritées comme déconseillées `CorBindTo*` fonctions (voir [déconseillée hébergeant des fonctions CLR](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md) dans l’API d’hébergement .NET Framework 2.0).</span><span class="sxs-lookup"><span data-stu-id="86cd0-124">This method interacts consistently with legacy interfaces such as the [ICorRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md) interface and legacy functions such as the deprecated `CorBindTo*` functions (see [Deprecated CLR Hosting Functions](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md) in the .NET Framework 2.0 hosting API).</span></span> <span data-ttu-id="86cd0-125">Autrement dit, les runtimes chargés avec l’API héritée sont visibles à la nouvelle API, et les runtimes chargés avec la nouvelle API sont visibles à l’API héritée.</span><span class="sxs-lookup"><span data-stu-id="86cd0-125">That is, runtimes that are loaded with the legacy API are visible to the new API, and runtimes that are loaded with the new API are visible to the legacy API.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86cd0-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86cd0-126">Requirements</span></span>  
 <span data-ttu-id="86cd0-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="86cd0-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86cd0-128">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="86cd0-128">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="86cd0-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="86cd0-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="86cd0-130">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="86cd0-130">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="86cd0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86cd0-131">See also</span></span>

- [<span data-ttu-id="86cd0-132">ICLRMetaHost, interface</span><span class="sxs-lookup"><span data-stu-id="86cd0-132">ICLRMetaHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)
- [<span data-ttu-id="86cd0-133">Interfaces d'hébergement du CLR et coclasses déconseillées</span><span class="sxs-lookup"><span data-stu-id="86cd0-133">Deprecated CLR Hosting Interfaces and Coclasses</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-interfaces-and-coclasses.md)
- [<span data-ttu-id="86cd0-134">Interfaces d'hébergement du CLR</span><span class="sxs-lookup"><span data-stu-id="86cd0-134">CLR Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces.md)
- [<span data-ttu-id="86cd0-135">Fonction d'hébergement du CLR déconseillées</span><span class="sxs-lookup"><span data-stu-id="86cd0-135">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
- [<span data-ttu-id="86cd0-136">Hébergement</span><span class="sxs-lookup"><span data-stu-id="86cd0-136">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
