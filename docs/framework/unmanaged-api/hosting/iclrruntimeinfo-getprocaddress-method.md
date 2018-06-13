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
ms.openlocfilehash: e8e50a018016b885a3513cbd885b8e5115f18113
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432919"
---
# <a name="iclrruntimeinfogetprocaddress-method"></a><span data-ttu-id="95467-102">ICLRRuntimeInfo::GetProcAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="95467-102">ICLRRuntimeInfo::GetProcAddress Method</span></span>
<span data-ttu-id="95467-103">Obtient l’adresse d’une fonction spécifiée qui a été exportée dans le common language runtime (CLR) associé à cette interface.</span><span class="sxs-lookup"><span data-stu-id="95467-103">Gets the address of a specified function that was exported from the common language runtime (CLR) associated with this interface.</span></span>  
  
 <span data-ttu-id="95467-104">Cette méthode remplace la [GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="95467-104">This method supersedes the [GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95467-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95467-105">Syntax</span></span>  
  
```  
HRESULT GetProcAddress(  
     [in]  LPCSTR pszProcName,  
     [out, retval] LPVOID *ppProc);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="95467-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95467-106">Parameters</span></span>  
 `pszProcName`  
 <span data-ttu-id="95467-107">[in] Le nom de la fonction exportée.</span><span class="sxs-lookup"><span data-stu-id="95467-107">[in] The name of the exported function.</span></span>  
  
 `ppProc`  
 <span data-ttu-id="95467-108">[out] L’adresse de la fonction exportée.</span><span class="sxs-lookup"><span data-stu-id="95467-108">[out] The address of the exported function.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="95467-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="95467-109">Return Value</span></span>  
 <span data-ttu-id="95467-110">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="95467-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="95467-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="95467-111">HRESULT</span></span>|<span data-ttu-id="95467-112">Description</span><span class="sxs-lookup"><span data-stu-id="95467-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="95467-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="95467-113">S_OK</span></span>|<span data-ttu-id="95467-114">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="95467-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="95467-115">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="95467-115">E_POINTER</span></span>|<span data-ttu-id="95467-116">`pszProcName` ou `ppProc` est null.</span><span class="sxs-lookup"><span data-stu-id="95467-116">`pszProcName` or `ppProc` is null.</span></span>|  
|<span data-ttu-id="95467-117">CLR_E_SHIM_RUNTIMEEXPORT</span><span class="sxs-lookup"><span data-stu-id="95467-117">CLR_E_SHIM_RUNTIMEEXPORT</span></span>|<span data-ttu-id="95467-118">La fonction spécifiée n’est pas une fonction exportée.</span><span class="sxs-lookup"><span data-stu-id="95467-118">The specified function is not an exported function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="95467-119">Notes</span><span class="sxs-lookup"><span data-stu-id="95467-119">Remarks</span></span>  
 <span data-ttu-id="95467-120">Cette méthode entraîne le CLR pour être chargé, mais non initialisé.</span><span class="sxs-lookup"><span data-stu-id="95467-120">This method causes the CLR to be loaded but not initialized.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="95467-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="95467-121">Requirements</span></span>  
 <span data-ttu-id="95467-122">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="95467-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="95467-123">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="95467-123">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="95467-124">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="95467-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="95467-125">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="95467-125">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="95467-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95467-126">See Also</span></span>  
 [<span data-ttu-id="95467-127">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="95467-127">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)  
 [<span data-ttu-id="95467-128">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="95467-128">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="95467-129">Hébergement</span><span class="sxs-lookup"><span data-stu-id="95467-129">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
