---
title: ICLRRuntimeInfo::LoadErrorString, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.LoadErrorString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::LoadErrorString
helpviewer_keywords:
- ICLRRuntimeInfo::LoadErrorString method [.NET Framework hosting]
- LoadErrorString method [.NET Framework hosting]
ms.assetid: 52c543ab-9ef5-4ee7-b836-c0ffc35cd45b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 43a00d687c6a9ec42cb8573e70d181b4dc2c7d0e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433215"
---
# <a name="iclrruntimeinfoloaderrorstring-method"></a><span data-ttu-id="22e28-102">ICLRRuntimeInfo::LoadErrorString, méthode</span><span class="sxs-lookup"><span data-stu-id="22e28-102">ICLRRuntimeInfo::LoadErrorString Method</span></span>
<span data-ttu-id="22e28-103">Traduit une valeur HRESULT dans un message d’erreur approprié pour la culture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="22e28-103">Translates an HRESULT value into an appropriate error message for the specified culture.</span></span>  
  
 <span data-ttu-id="22e28-104">Cette méthode remplace les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="22e28-104">This method supersedes the following functions:</span></span>  
  
-   [<span data-ttu-id="22e28-105">LoadStringRC</span><span class="sxs-lookup"><span data-stu-id="22e28-105">LoadStringRC</span></span>](../../../../docs/framework/unmanaged-api/hosting/loadstringrc-function.md)  
  
-   [<span data-ttu-id="22e28-106">LoadStringRCEx</span><span class="sxs-lookup"><span data-stu-id="22e28-106">LoadStringRCEx</span></span>](../../../../docs/framework/unmanaged-api/hosting/loadstringrcex-function.md)  
  
## <a name="syntax"></a><span data-ttu-id="22e28-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22e28-107">Syntax</span></span>  
  
```  
HRESULT LoadErrorString(  
     [in] UINT iResourceID,  
     [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
     [in, out]  DWORD *pcchBuffer,  
     [in, lcid] LONG iLocaleID);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="22e28-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22e28-108">Parameters</span></span>  
 `iResourceID`  
 <span data-ttu-id="22e28-109">[in] HRESULT à convertir.</span><span class="sxs-lookup"><span data-stu-id="22e28-109">[in] The HRESULT to translate.</span></span>  
  
 `pwzBuffer`  
 <span data-ttu-id="22e28-110">[out] La chaîne de message associée au HRESULT donné.</span><span class="sxs-lookup"><span data-stu-id="22e28-110">[out] The message string associated with the given HRESULT.</span></span>  
  
 `pcchBuffer`  
 <span data-ttu-id="22e28-111">[dans, out] La taille de `pwzbuffer` pour éviter les dépassements de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="22e28-111">[in, out] The size of `pwzbuffer` to avoid buffer overruns.</span></span> <span data-ttu-id="22e28-112">Si `pwzbuffer` a la valeur null, `pcchBuffer` fournit la taille attendue de `pwzbuffer` pour autoriser la pré-allocation.</span><span class="sxs-lookup"><span data-stu-id="22e28-112">If `pwzbuffer` is null, `pcchBuffer` provides the expected size of `pwzbuffer` to allow preallocation.</span></span>  
  
 `iLocaleID`  
 <span data-ttu-id="22e28-113">[in] L’identificateur de culture.</span><span class="sxs-lookup"><span data-stu-id="22e28-113">[in] The culture identifier.</span></span> <span data-ttu-id="22e28-114">Pour utiliser la culture par défaut, vous devez spécifier -1.</span><span class="sxs-lookup"><span data-stu-id="22e28-114">To use the default culture, you must specify -1.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="22e28-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="22e28-115">Return Value</span></span>  
 <span data-ttu-id="22e28-116">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="22e28-116">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="22e28-117">HRESULT</span><span class="sxs-lookup"><span data-stu-id="22e28-117">HRESULT</span></span>|<span data-ttu-id="22e28-118">Description</span><span class="sxs-lookup"><span data-stu-id="22e28-118">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="22e28-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="22e28-119">S_OK</span></span>|<span data-ttu-id="22e28-120">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="22e28-120">The method completed successfully.</span></span>|  
|<span data-ttu-id="22e28-121">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="22e28-121">E_POINTER</span></span>|<span data-ttu-id="22e28-122">`pcchBuffer` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="22e28-122">`pcchBuffer` is null.</span></span>|  
|<span data-ttu-id="22e28-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="22e28-123">E_INVALIDARG</span></span>|<span data-ttu-id="22e28-124">`pwzBuffer` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="22e28-124">`pwzBuffer` is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="22e28-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="22e28-125">Requirements</span></span>  
 <span data-ttu-id="22e28-126">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="22e28-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22e28-127">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="22e28-127">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="22e28-128">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="22e28-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="22e28-129">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22e28-129">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22e28-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22e28-130">See Also</span></span>  
 [<span data-ttu-id="22e28-131">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="22e28-131">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)  
 [<span data-ttu-id="22e28-132">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="22e28-132">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="22e28-133">Hébergement</span><span class="sxs-lookup"><span data-stu-id="22e28-133">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
