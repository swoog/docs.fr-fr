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
ms.openlocfilehash: 48c2a394126aca3a10b38ab2ba2df945f53e45d6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33438270"
---
# <a name="icorconfigurationsetgchostcontrol-method"></a><span data-ttu-id="ea61e-102">ICorConfiguration::SetGCHostControl, méthode</span><span class="sxs-lookup"><span data-stu-id="ea61e-102">ICorConfiguration::SetGCHostControl Method</span></span>
<span data-ttu-id="ea61e-103">Définit l’interface de rappel à utiliser par le garbage collector de demander à l’hôte de modifier les limites de mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="ea61e-103">Sets the callback interface to be used by the garbage collector to request the host to change the limits of virtual memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea61e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea61e-104">Syntax</span></span>  
  
```  
HRESULT SetGCHostControl (  
    [in] IGCHostControl* pGCHostControl  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ea61e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea61e-105">Parameters</span></span>  
 `pGCHostControl`  
 <span data-ttu-id="ea61e-106">[in] Un pointeur vers un [IGCHostControl](../../../../docs/framework/unmanaged-api/hosting/igchostcontrol-interface.md) objet qui autorise le garbage collector de demander à l’hôte de modifier les limites de mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="ea61e-106">[in] A pointer to an [IGCHostControl](../../../../docs/framework/unmanaged-api/hosting/igchostcontrol-interface.md) object that allows the garbage collector to request the host to change the limits of virtual memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ea61e-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ea61e-107">Requirements</span></span>  
 <span data-ttu-id="ea61e-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ea61e-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ea61e-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="ea61e-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ea61e-110">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ea61e-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ea61e-111">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ea61e-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ea61e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea61e-112">See Also</span></span>  
 [<span data-ttu-id="ea61e-113">ICorConfiguration, interface</span><span class="sxs-lookup"><span data-stu-id="ea61e-113">ICorConfiguration Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)
