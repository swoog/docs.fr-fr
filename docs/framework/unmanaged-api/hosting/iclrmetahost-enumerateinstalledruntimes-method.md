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
ms.openlocfilehash: 09931dce7afdb7944cf9912b5146e44fda131935
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59173405"
---
# <a name="iclrmetahostenumerateinstalledruntimes-method"></a><span data-ttu-id="8b63e-102">ICLRMetaHost::EnumerateInstalledRuntimes, méthode</span><span class="sxs-lookup"><span data-stu-id="8b63e-102">ICLRMetaHost::EnumerateInstalledRuntimes Method</span></span>
<span data-ttu-id="8b63e-103">Retourne une énumération qui contient un élément valide [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface pour chaque version du common language runtime (CLR) est installé sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8b63e-103">Returns an enumeration that contains a valid [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface for each version of the common language runtime (CLR) that is installed on a computer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b63e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b63e-104">Syntax</span></span>  
  
```  
HRESULT EnumerateInstalledRuntimes (  
    [out, retval] IEnumUnknown **ppEnumerator);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8b63e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b63e-105">Parameters</span></span>  
 `ppEnumerator`  
 <span data-ttu-id="8b63e-106">[out] Une énumération de [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interfaces correspondant à chaque version du CLR qui est installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8b63e-106">[out] An enumeration of [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interfaces corresponding to each version of the CLR that is installed on the computer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8b63e-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8b63e-107">Return Value</span></span>  
 <span data-ttu-id="8b63e-108">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="8b63e-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="8b63e-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8b63e-109">HRESULT</span></span>|<span data-ttu-id="8b63e-110">Description</span><span class="sxs-lookup"><span data-stu-id="8b63e-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8b63e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b63e-111">S_OK</span></span>|<span data-ttu-id="8b63e-112">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="8b63e-112">The method completed successfully.</span></span>|  
|<span data-ttu-id="8b63e-113">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="8b63e-113">E_POINTER</span></span>|`ppEnumerator` <span data-ttu-id="8b63e-114">a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="8b63e-114">is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8b63e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b63e-115">Requirements</span></span>  
 <span data-ttu-id="8b63e-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8b63e-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8b63e-117">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="8b63e-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="8b63e-118">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8b63e-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="8b63e-119">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="8b63e-119">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8b63e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b63e-120">See also</span></span>

- [<span data-ttu-id="8b63e-121">ICLRMetaHost, interface</span><span class="sxs-lookup"><span data-stu-id="8b63e-121">ICLRMetaHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)
- [<span data-ttu-id="8b63e-122">Hébergement</span><span class="sxs-lookup"><span data-stu-id="8b63e-122">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
