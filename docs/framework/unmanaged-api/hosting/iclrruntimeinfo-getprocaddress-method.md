---
title: ICLRRuntimeInfo::GetProcAddress, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.GetProcAddress
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::GetProcAddress
helpviewer_keywords:
- GetProcAddress method [.NET Framework hosting]
- ICLRRuntimeInfo::GetProcAddress method [.NET Framework hosting]
ms.assetid: a7732bfc-689a-4926-88fd-4f81e6f9ed78
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a95b6b7e20bbcd86dedf187c932f2cf74d37cdab
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59199178"
---
# <a name="iclrruntimeinfogetprocaddress-method"></a><span data-ttu-id="5ca52-102">ICLRRuntimeInfo::GetProcAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="5ca52-102">ICLRRuntimeInfo::GetProcAddress Method</span></span>
<span data-ttu-id="5ca52-103">Obtient l’adresse d’une fonction spécifiée qui a été exportée dans le common language runtime (CLR) associé à cette interface.</span><span class="sxs-lookup"><span data-stu-id="5ca52-103">Gets the address of a specified function that was exported from the common language runtime (CLR) associated with this interface.</span></span>  
  
 <span data-ttu-id="5ca52-104">Cette méthode remplace la [GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="5ca52-104">This method supersedes the [GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5ca52-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ca52-105">Syntax</span></span>  
  
```  
HRESULT GetProcAddress(  
     [in]  LPCSTR pszProcName,  
     [out, retval] LPVOID *ppProc);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5ca52-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ca52-106">Parameters</span></span>  
 `pszProcName`  
 <span data-ttu-id="5ca52-107">[in] Le nom de la fonction exportée.</span><span class="sxs-lookup"><span data-stu-id="5ca52-107">[in] The name of the exported function.</span></span>  
  
 `ppProc`  
 <span data-ttu-id="5ca52-108">[out] L’adresse de la fonction exportée.</span><span class="sxs-lookup"><span data-stu-id="5ca52-108">[out] The address of the exported function.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5ca52-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5ca52-109">Return Value</span></span>  
 <span data-ttu-id="5ca52-110">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="5ca52-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="5ca52-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="5ca52-111">HRESULT</span></span>|<span data-ttu-id="5ca52-112">Description</span><span class="sxs-lookup"><span data-stu-id="5ca52-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="5ca52-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ca52-113">S_OK</span></span>|<span data-ttu-id="5ca52-114">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="5ca52-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="5ca52-115">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="5ca52-115">E_POINTER</span></span>|`pszProcName` <span data-ttu-id="5ca52-116">ou `ppProc` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="5ca52-116">or `ppProc` is null.</span></span>|  
|<span data-ttu-id="5ca52-117">CLR_E_SHIM_RUNTIMEEXPORT</span><span class="sxs-lookup"><span data-stu-id="5ca52-117">CLR_E_SHIM_RUNTIMEEXPORT</span></span>|<span data-ttu-id="5ca52-118">La fonction spécifiée n’est pas une fonction exportée.</span><span class="sxs-lookup"><span data-stu-id="5ca52-118">The specified function is not an exported function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5ca52-119">Notes</span><span class="sxs-lookup"><span data-stu-id="5ca52-119">Remarks</span></span>  
 <span data-ttu-id="5ca52-120">Cette méthode provoque le CLR être chargé, mais non initialisé.</span><span class="sxs-lookup"><span data-stu-id="5ca52-120">This method causes the CLR to be loaded but not initialized.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5ca52-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ca52-121">Requirements</span></span>  
 <span data-ttu-id="5ca52-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5ca52-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5ca52-123">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="5ca52-123">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="5ca52-124">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5ca52-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="5ca52-125">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="5ca52-125">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="5ca52-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ca52-126">See also</span></span>

- [<span data-ttu-id="5ca52-127">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="5ca52-127">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)
- [<span data-ttu-id="5ca52-128">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="5ca52-128">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="5ca52-129">Hébergement</span><span class="sxs-lookup"><span data-stu-id="5ca52-129">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
