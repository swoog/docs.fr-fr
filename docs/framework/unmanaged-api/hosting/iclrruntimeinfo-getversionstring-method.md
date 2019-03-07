---
title: ICLRRuntimeInfo::GetVersionString, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.GetVersionString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::GetVersionString
helpviewer_keywords:
- ICLRRuntimeInfo::GetVersionString method [.NET Framework hosting]
- GetVersionString method, ICLRRuntimeInfo interface [.NET Framework hosting]
ms.assetid: 98b097ef-2276-4dd9-8551-b03c972e8179
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cbfa25300cbed83d36cc43d9a0dd0beb2520dea1
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57475288"
---
# <a name="iclrruntimeinfogetversionstring-method"></a><span data-ttu-id="e7d85-102">ICLRRuntimeInfo::GetVersionString, méthode</span><span class="sxs-lookup"><span data-stu-id="e7d85-102">ICLRRuntimeInfo::GetVersionString Method</span></span>
<span data-ttu-id="e7d85-103">Obtient les informations de version du common language runtime (CLR) associées à une donnée [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="e7d85-103">Gets common language runtime (CLR) version information associated with a given [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span></span>  
  
 <span data-ttu-id="e7d85-104">Cette méthode remplace les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e7d85-104">This method supersedes the following functions:</span></span>  
  
-   [<span data-ttu-id="e7d85-105">GetRequestedRuntimeInfo</span><span class="sxs-lookup"><span data-stu-id="e7d85-105">GetRequestedRuntimeInfo</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeinfo-function.md)  
  
-   [<span data-ttu-id="e7d85-106">GetRequestedRuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="e7d85-106">GetRequestedRuntimeVersion</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeversion-function.md)  
  
## <a name="syntax"></a><span data-ttu-id="e7d85-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7d85-107">Syntax</span></span>  
  
```  
HRESULT GetVersionString(  
    [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
    [in, out]  DWORD *pcchBuffer);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e7d85-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7d85-108">Parameters</span></span>  
 `pwzBuffer`  
 <span data-ttu-id="e7d85-109">[out] La version de compilation .NET Framework dans le format « v*A*. *B*[. *X*] ».</span><span class="sxs-lookup"><span data-stu-id="e7d85-109">[out] The .NET Framework compilation version in the format "v*A*.*B*[.*X*]".</span></span> <span data-ttu-id="e7d85-110">*Un*, *B*, et *X* sont des nombres décimaux qui correspondent à la version principale, la version secondaire et le numéro de build.</span><span class="sxs-lookup"><span data-stu-id="e7d85-110">*A*, *B*, and *X* are decimal numbers that correspond to the major version, the minor version, and the build number.</span></span> <span data-ttu-id="e7d85-111">*X* est facultatif.</span><span class="sxs-lookup"><span data-stu-id="e7d85-111">*X* is optional.</span></span> <span data-ttu-id="e7d85-112">Si *X* est absent, il n’est pas de point final.</span><span class="sxs-lookup"><span data-stu-id="e7d85-112">If *X* is not present, there is no trailing period.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e7d85-113">Ce paramètre doit correspondre au nom de répertoire pour la version de .NET Framework, tel qu’il apparaît sous C:\Windows\Microsoft.NET\Framework.</span><span class="sxs-lookup"><span data-stu-id="e7d85-113">This parameter must match the directory name for the .NET Framework version, as it appears under C:\Windows\Microsoft.NET\Framework.</span></span>  
  
 <span data-ttu-id="e7d85-114">Exemples de valeurs : « v1.0.3705 », « v1.1.4322 », « v2.0.50727 » et « v4.0. *x*», où *x* varie selon le numéro de build installé.</span><span class="sxs-lookup"><span data-stu-id="e7d85-114">Example values are "v1.0.3705", "v1.1.4322", "v2.0.50727", and "v4.0.*x*", where *x* depends on the build number installed.</span></span> <span data-ttu-id="e7d85-115">Notez que le préfixe « v » est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e7d85-115">Note that the "v" prefix is mandatory.</span></span>  
  
 `pchBuffer`  
 <span data-ttu-id="e7d85-116">[in, out] Spécifie la taille du `pwzBuffer` pour éviter les dépassements de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e7d85-116">[in, out] Specifies the size of `pwzBuffer` to avoid buffer overruns.</span></span> <span data-ttu-id="e7d85-117">Si `pwzBuffer` est `null`, `pchBuffer` retourne la taille requise de `pwzBuffer` pour autoriser la pré-allocation.</span><span class="sxs-lookup"><span data-stu-id="e7d85-117">If `pwzBuffer` is `null`, `pchBuffer` returns the required size of `pwzBuffer` to allow preallocation.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e7d85-118">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e7d85-118">Return Value</span></span>  
 <span data-ttu-id="e7d85-119">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="e7d85-119">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="e7d85-120">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e7d85-120">HRESULT</span></span>|<span data-ttu-id="e7d85-121">Description</span><span class="sxs-lookup"><span data-stu-id="e7d85-121">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e7d85-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7d85-122">S_OK</span></span>|<span data-ttu-id="e7d85-123">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="e7d85-123">The method completed successfully.</span></span>|  
|<span data-ttu-id="e7d85-124">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="e7d85-124">E_POINTER</span></span>|<span data-ttu-id="e7d85-125">`pwzBuffer` ou `pchBuffer` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="e7d85-125">`pwzBuffer` or `pchBuffer` is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e7d85-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e7d85-126">Requirements</span></span>  
 <span data-ttu-id="e7d85-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e7d85-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7d85-128">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="e7d85-128">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="e7d85-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e7d85-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e7d85-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7d85-130">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7d85-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7d85-131">See also</span></span>
- [<span data-ttu-id="e7d85-132">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="e7d85-132">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)
- [<span data-ttu-id="e7d85-133">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="e7d85-133">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="e7d85-134">Interfaces d’hébergement CLR ajoutées dans .NET Framework 4 et 4.5</span><span class="sxs-lookup"><span data-stu-id="e7d85-134">CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)
- [<span data-ttu-id="e7d85-135">Hébergement</span><span class="sxs-lookup"><span data-stu-id="e7d85-135">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
