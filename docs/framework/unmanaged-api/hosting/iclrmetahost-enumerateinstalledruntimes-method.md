---
title: ICLRMetaHost::EnumerateInstalledRuntimes, méthode
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.EnumerateInstalledRuntimes
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::EnumerateInstalledRuntimes
helpviewer_keywords:
- ICLRMetaHost::EnumerateInstalledRuntimes method [.NET Framework hosting]
- EnumerateInstalledRuntimes method [.NET Framework hosting]
ms.assetid: 9e359384-0d3d-451c-807e-5d7fcebf2be7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 900ad908229b7881dfa9ba55732e20926c912d7c
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57469077"
---
# <a name="iclrmetahostenumerateinstalledruntimes-method"></a><span data-ttu-id="efb58-102">ICLRMetaHost::EnumerateInstalledRuntimes, méthode</span><span class="sxs-lookup"><span data-stu-id="efb58-102">ICLRMetaHost::EnumerateInstalledRuntimes Method</span></span>
<span data-ttu-id="efb58-103">Retourne une énumération qui contient un élément valide [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface pour chaque version du common language runtime (CLR) est installé sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="efb58-103">Returns an enumeration that contains a valid [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface for each version of the common language runtime (CLR) that is installed on a computer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="efb58-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efb58-104">Syntax</span></span>  
  
```  
HRESULT EnumerateInstalledRuntimes (  
    [out, retval] IEnumUnknown **ppEnumerator);  
```  
  
## <a name="parameters"></a><span data-ttu-id="efb58-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efb58-105">Parameters</span></span>  
 `ppEnumerator`  
 <span data-ttu-id="efb58-106">[out] Une énumération de [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interfaces correspondant à chaque version du CLR qui est installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="efb58-106">[out] An enumeration of [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interfaces corresponding to each version of the CLR that is installed on the computer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="efb58-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="efb58-107">Return Value</span></span>  
 <span data-ttu-id="efb58-108">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="efb58-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="efb58-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="efb58-109">HRESULT</span></span>|<span data-ttu-id="efb58-110">Description</span><span class="sxs-lookup"><span data-stu-id="efb58-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="efb58-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="efb58-111">S_OK</span></span>|<span data-ttu-id="efb58-112">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="efb58-112">The method completed successfully.</span></span>|  
|<span data-ttu-id="efb58-113">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="efb58-113">E_POINTER</span></span>|<span data-ttu-id="efb58-114">`ppEnumerator` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="efb58-114">`ppEnumerator` is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="efb58-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="efb58-115">Requirements</span></span>  
 <span data-ttu-id="efb58-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="efb58-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="efb58-117">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="efb58-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="efb58-118">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="efb58-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="efb58-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="efb58-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="efb58-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efb58-120">See also</span></span>
- [<span data-ttu-id="efb58-121">ICLRMetaHost, interface</span><span class="sxs-lookup"><span data-stu-id="efb58-121">ICLRMetaHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)
- [<span data-ttu-id="efb58-122">Hébergement</span><span class="sxs-lookup"><span data-stu-id="efb58-122">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
