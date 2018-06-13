---
title: ICLRMetaHost::EnumerateLoadedRuntimes, méthode
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.EnumerateLoadedRuntimes
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::EnumerateLoadedRuntimes
helpviewer_keywords:
- EnumerateLoadedRuntimes method [.NET Framework hosting]
- ICLRMetaHost::EnumerateLoadedRuntimes method [.NET Framework hosting]
ms.assetid: 22fc0a3f-dce4-4766-9a3c-9fab15f4b4ca
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8342b18d0fb4163112aafd483bc452a3538aa5c2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433781"
---
# <a name="iclrmetahostenumerateloadedruntimes-method"></a><span data-ttu-id="b3664-102">ICLRMetaHost::EnumerateLoadedRuntimes, méthode</span><span class="sxs-lookup"><span data-stu-id="b3664-102">ICLRMetaHost::EnumerateLoadedRuntimes Method</span></span>
<span data-ttu-id="b3664-103">Retourne une énumération qui contient un élément valide [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) pointeur d’interface pour chaque version du common language runtime (CLR) qui est chargé dans un processus donné.</span><span class="sxs-lookup"><span data-stu-id="b3664-103">Returns an enumeration that includes a valid [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface pointer for each version of the common language runtime (CLR) that is loaded in a given process.</span></span> <span data-ttu-id="b3664-104">Cette méthode remplace la [GetVersionFromProcess](../../../../docs/framework/unmanaged-api/hosting/getversionfromprocess-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="b3664-104">This method supersedes the [GetVersionFromProcess](../../../../docs/framework/unmanaged-api/hosting/getversionfromprocess-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b3664-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3664-105">Syntax</span></span>  
  
```  
HRESULT EnumerateLoadedRuntimes (  
    [in] HANDLE hndProcess,  
    [out, retval] IEnumUnknown **ppEnumerator  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b3664-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3664-106">Parameters</span></span>  
 `hndProcess`  
 <span data-ttu-id="b3664-107">[in] Le handle du processus à inspecter pour les runtimes chargés.</span><span class="sxs-lookup"><span data-stu-id="b3664-107">[in] The handle of the process to inspect for loaded runtimes.</span></span>  
  
 `ppEnumerator`  
 <span data-ttu-id="b3664-108">[out] Un <!--zz <xref:Microsoft.VisualStudio.OLE.Interop.IEnumUnknown>--> `Microsoft.VisualStudio.OLE.Interop.IEnumUnknown` énumération de [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interfaces correspondant à chaque CLR qui est chargé par le processus.</span><span class="sxs-lookup"><span data-stu-id="b3664-108">[out] An <!--zz <xref:Microsoft.VisualStudio.OLE.Interop.IEnumUnknown>--> `Microsoft.VisualStudio.OLE.Interop.IEnumUnknown` enumeration of [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interfaces corresponding to each CLR that is loaded by the process.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b3664-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b3664-109">Return Value</span></span>  
 <span data-ttu-id="b3664-110">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="b3664-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="b3664-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b3664-111">HRESULT</span></span>|<span data-ttu-id="b3664-112">Description</span><span class="sxs-lookup"><span data-stu-id="b3664-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b3664-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="b3664-113">S_OK</span></span>|<span data-ttu-id="b3664-114">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="b3664-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="b3664-115">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="b3664-115">E_POINTER</span></span>|<span data-ttu-id="b3664-116">`ppEnumerator` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="b3664-116">`ppEnumerator` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b3664-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b3664-117">Remarks</span></span>  
 <span data-ttu-id="b3664-118">Cette méthode est répertorie toutes les exécutions chargées, même si elles ont été chargées avec les fonctions déconseillées comme [CorBindToRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md).</span><span class="sxs-lookup"><span data-stu-id="b3664-118">This method is lists all loaded runtimes, even if they were loaded with deprecated functions such as [CorBindToRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b3664-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b3664-119">Requirements</span></span>  
 <span data-ttu-id="b3664-120">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b3664-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b3664-121">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="b3664-121">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="b3664-122">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b3664-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b3664-123">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b3664-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3664-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3664-124">See Also</span></span>  
 [<span data-ttu-id="b3664-125">ICLRMetaHost, interface</span><span class="sxs-lookup"><span data-stu-id="b3664-125">ICLRMetaHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)  
 [<span data-ttu-id="b3664-126">Hébergement</span><span class="sxs-lookup"><span data-stu-id="b3664-126">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
