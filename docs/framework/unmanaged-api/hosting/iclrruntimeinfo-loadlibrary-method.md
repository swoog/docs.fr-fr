---
title: ICLRRuntimeInfo::LoadLibrary, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.LoadLibrary
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::LoadLibrary
helpviewer_keywords:
- ICLRRuntimeInfo::LoadLibrary method [.NET Framework hosting]
- LoadLibrary method [.NET Framework hosting]
ms.assetid: 4517ada3-4417-4ac5-a150-73da7a87c686
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3fe1f93c621fd567471b9a49e4aa75cb90e6e0e7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59161159"
---
# <a name="iclrruntimeinfoloadlibrary-method"></a><span data-ttu-id="da9c4-102">ICLRRuntimeInfo::LoadLibrary, méthode</span><span class="sxs-lookup"><span data-stu-id="da9c4-102">ICLRRuntimeInfo::LoadLibrary Method</span></span>
<span data-ttu-id="da9c4-103">Charge une bibliothèque .NET Framework à partir de représenté par le common language runtime (CLR) un [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="da9c4-103">Loads a .NET Framework library from the common language runtime (CLR) represented by an [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span></span>  
  
 <span data-ttu-id="da9c4-104">Cette méthode remplace la [LoadLibraryShim](../../../../docs/framework/unmanaged-api/hosting/loadlibraryshim-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="da9c4-104">This method supersedes the [LoadLibraryShim](../../../../docs/framework/unmanaged-api/hosting/loadlibraryshim-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da9c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da9c4-105">Syntax</span></span>  
  
```  
HRESULT LoadLibrary(  
     [in]  LPCWSTR pwzDllName,  
     [out, retval] HMODULE *phndModule);  
```  
  
## <a name="parameters"></a><span data-ttu-id="da9c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da9c4-106">Parameters</span></span>  
 `pwzDllName`  
 <span data-ttu-id="da9c4-107">[in] Le nom de l’assembly à charger.</span><span class="sxs-lookup"><span data-stu-id="da9c4-107">[in] The name of the assembly to be loaded.</span></span>  
  
 `phndModule`  
 <span data-ttu-id="da9c4-108">[out] Handle vers l’assembly chargé.</span><span class="sxs-lookup"><span data-stu-id="da9c4-108">[out] A handle to the loaded assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="da9c4-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="da9c4-109">Return Value</span></span>  
 <span data-ttu-id="da9c4-110">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="da9c4-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="da9c4-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="da9c4-111">HRESULT</span></span>|<span data-ttu-id="da9c4-112">Description</span><span class="sxs-lookup"><span data-stu-id="da9c4-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="da9c4-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="da9c4-113">S_OK</span></span>|<span data-ttu-id="da9c4-114">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="da9c4-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="da9c4-115">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="da9c4-115">E_POINTER</span></span>|`pwzDllName` <span data-ttu-id="da9c4-116">ou `phndModule` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="da9c4-116">or `phndModule` is null.</span></span>|  
|<span data-ttu-id="da9c4-117">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="da9c4-117">E_OUTOFMEMORY</span></span>|<span data-ttu-id="da9c4-118">Pas assez de mémoire est disponible pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="da9c4-118">Not enough memory is available to handle the request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="da9c4-119">Notes</span><span class="sxs-lookup"><span data-stu-id="da9c4-119">Remarks</span></span>  
 <span data-ttu-id="da9c4-120">Cette méthode charge uniquement les DLL incluses dans le package redistribuable .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="da9c4-120">This method only loads DLLs included in the .NET Framework redistributable package.</span></span> <span data-ttu-id="da9c4-121">Il ne peut pas charger des assemblys générés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="da9c4-121">It can not load user-generated assemblies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="da9c4-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da9c4-122">Requirements</span></span>  
 <span data-ttu-id="da9c4-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="da9c4-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="da9c4-124">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="da9c4-124">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="da9c4-125">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="da9c4-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="da9c4-126">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="da9c4-126">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="da9c4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da9c4-127">See also</span></span>

- [<span data-ttu-id="da9c4-128">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="da9c4-128">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)
- [<span data-ttu-id="da9c4-129">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="da9c4-129">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="da9c4-130">Hébergement</span><span class="sxs-lookup"><span data-stu-id="da9c4-130">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
