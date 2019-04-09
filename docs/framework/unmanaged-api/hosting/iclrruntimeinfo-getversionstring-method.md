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
ms.openlocfilehash: d6e320936430307dab066eecc835ac5c84bd22bc
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59202324"
---
# <a name="iclrruntimeinfogetversionstring-method"></a><span data-ttu-id="7a384-102">ICLRRuntimeInfo::GetVersionString, méthode</span><span class="sxs-lookup"><span data-stu-id="7a384-102">ICLRRuntimeInfo::GetVersionString Method</span></span>
<span data-ttu-id="7a384-103">Obtient les informations de version du common language runtime (CLR) associées à une donnée [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="7a384-103">Gets common language runtime (CLR) version information associated with a given [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span></span>  
  
 <span data-ttu-id="7a384-104">Cette méthode remplace les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a384-104">This method supersedes the following functions:</span></span>  
  
-   [<span data-ttu-id="7a384-105">GetRequestedRuntimeInfo</span><span class="sxs-lookup"><span data-stu-id="7a384-105">GetRequestedRuntimeInfo</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeinfo-function.md)  
  
-   [<span data-ttu-id="7a384-106">GetRequestedRuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="7a384-106">GetRequestedRuntimeVersion</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeversion-function.md)  
  
## <a name="syntax"></a><span data-ttu-id="7a384-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a384-107">Syntax</span></span>  
  
```  
HRESULT GetVersionString(  
    [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
    [in, out]  DWORD *pcchBuffer);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7a384-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a384-108">Parameters</span></span>  
 `pwzBuffer`  
 <span data-ttu-id="7a384-109">[out] La version de compilation .NET Framework dans le format « v*A*. *B*[. *X*] ».</span><span class="sxs-lookup"><span data-stu-id="7a384-109">[out] The .NET Framework compilation version in the format "v*A*.*B*[.*X*]".</span></span> <span data-ttu-id="7a384-110">*Un*, *B*, et *X* sont des nombres décimaux qui correspondent à la version principale, la version secondaire et le numéro de build.</span><span class="sxs-lookup"><span data-stu-id="7a384-110">*A*, *B*, and *X* are decimal numbers that correspond to the major version, the minor version, and the build number.</span></span> <span data-ttu-id="7a384-111">*X* est facultatif.</span><span class="sxs-lookup"><span data-stu-id="7a384-111">*X* is optional.</span></span> <span data-ttu-id="7a384-112">Si *X* est absent, il n’est pas de point final.</span><span class="sxs-lookup"><span data-stu-id="7a384-112">If *X* is not present, there is no trailing period.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7a384-113">Ce paramètre doit correspondre au nom de répertoire pour la version de .NET Framework, tel qu’il apparaît sous C:\Windows\Microsoft.NET\Framework.</span><span class="sxs-lookup"><span data-stu-id="7a384-113">This parameter must match the directory name for the .NET Framework version, as it appears under C:\Windows\Microsoft.NET\Framework.</span></span>  
  
 <span data-ttu-id="7a384-114">Exemples de valeurs : « v1.0.3705 », « v1.1.4322 », « v2.0.50727 » et « v4.0. *x*», où *x* varie selon le numéro de build installé.</span><span class="sxs-lookup"><span data-stu-id="7a384-114">Example values are "v1.0.3705", "v1.1.4322", "v2.0.50727", and "v4.0.*x*", where *x* depends on the build number installed.</span></span> <span data-ttu-id="7a384-115">Notez que le préfixe « v » est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7a384-115">Note that the "v" prefix is mandatory.</span></span>  
  
 `pchBuffer`  
 <span data-ttu-id="7a384-116">[in, out] Spécifie la taille du `pwzBuffer` pour éviter les dépassements de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7a384-116">[in, out] Specifies the size of `pwzBuffer` to avoid buffer overruns.</span></span> <span data-ttu-id="7a384-117">Si `pwzBuffer` est `null`, `pchBuffer` retourne la taille requise de `pwzBuffer` pour autoriser la pré-allocation.</span><span class="sxs-lookup"><span data-stu-id="7a384-117">If `pwzBuffer` is `null`, `pchBuffer` returns the required size of `pwzBuffer` to allow preallocation.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7a384-118">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7a384-118">Return Value</span></span>  
 <span data-ttu-id="7a384-119">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="7a384-119">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="7a384-120">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7a384-120">HRESULT</span></span>|<span data-ttu-id="7a384-121">Description</span><span class="sxs-lookup"><span data-stu-id="7a384-121">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7a384-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a384-122">S_OK</span></span>|<span data-ttu-id="7a384-123">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="7a384-123">The method completed successfully.</span></span>|  
|<span data-ttu-id="7a384-124">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="7a384-124">E_POINTER</span></span>|`pwzBuffer` <span data-ttu-id="7a384-125">ou `pchBuffer` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="7a384-125">or `pchBuffer` is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7a384-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a384-126">Requirements</span></span>  
 <span data-ttu-id="7a384-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7a384-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a384-128">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="7a384-128">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="7a384-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7a384-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="7a384-130">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="7a384-130">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="7a384-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a384-131">See also</span></span>

- [<span data-ttu-id="7a384-132">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="7a384-132">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)
- [<span data-ttu-id="7a384-133">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="7a384-133">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="7a384-134">Interfaces d'hébergement du CLR ajoutées dans .NET Framework 4 et 4.5</span><span class="sxs-lookup"><span data-stu-id="7a384-134">CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)
- [<span data-ttu-id="7a384-135">Hébergement</span><span class="sxs-lookup"><span data-stu-id="7a384-135">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
