---
title: ICorConfiguration::SetGCHostControl, méthode
ms.date: 03/30/2017
api_name:
- ICorConfiguration.SetGCHostControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetGCHostControl
helpviewer_keywords:
- ICorConfiguration::SetGCHostControl method [.NET Framework hosting]
- SetGCHostControl method [.NET Framework hosting]
ms.assetid: bca6bd79-e288-475a-aa46-6bf81541d966
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 50a92058e8a394b95c690d19f1bafdddbed8246a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59135991"
---
# <a name="icorconfigurationsetgchostcontrol-method"></a><span data-ttu-id="6ce19-102">ICorConfiguration::SetGCHostControl, méthode</span><span class="sxs-lookup"><span data-stu-id="6ce19-102">ICorConfiguration::SetGCHostControl Method</span></span>
<span data-ttu-id="6ce19-103">Définit l’interface de rappel à utiliser par le garbage collector de demander à l’hôte de modifier les limites de mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="6ce19-103">Sets the callback interface to be used by the garbage collector to request the host to change the limits of virtual memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ce19-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ce19-104">Syntax</span></span>  
  
```  
HRESULT SetGCHostControl (  
    [in] IGCHostControl* pGCHostControl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6ce19-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ce19-105">Parameters</span></span>  
 `pGCHostControl`  
 <span data-ttu-id="6ce19-106">[in] Un pointeur vers un [IGCHostControl](../../../../docs/framework/unmanaged-api/hosting/igchostcontrol-interface.md) objet qui permet au garbage collector de demander à l’hôte de modifier les limites de mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="6ce19-106">[in] A pointer to an [IGCHostControl](../../../../docs/framework/unmanaged-api/hosting/igchostcontrol-interface.md) object that allows the garbage collector to request the host to change the limits of virtual memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6ce19-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ce19-107">Requirements</span></span>  
 <span data-ttu-id="6ce19-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6ce19-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6ce19-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6ce19-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6ce19-110">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6ce19-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="6ce19-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="6ce19-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="6ce19-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ce19-112">See also</span></span>

- [<span data-ttu-id="6ce19-113">ICorConfiguration, interface</span><span class="sxs-lookup"><span data-stu-id="6ce19-113">ICorConfiguration Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)
