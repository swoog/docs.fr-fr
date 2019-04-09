---
title: IGCHostControl::RequestVirtualMemLimit, méthode
ms.date: 03/30/2017
api_name:
- IGCHostControl.RequestVirtualMemLimit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- RequestVirtualMemLimit
helpviewer_keywords:
- IGCHostControl::RequestVirtualMemLimit method [.NET Framework hosting]
- RequestVirtualMemLimit method [.NET Framework hosting]
ms.assetid: f4984a8c-4c0e-4460-9aa1-d022b3621228
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 948b18832ccfc5e0fc2e42ee58e6444a581de260
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59209686"
---
# <a name="igchostcontrolrequestvirtualmemlimit-method"></a><span data-ttu-id="5629d-102">IGCHostControl::RequestVirtualMemLimit, méthode</span><span class="sxs-lookup"><span data-stu-id="5629d-102">IGCHostControl::RequestVirtualMemLimit Method</span></span>
<span data-ttu-id="5629d-103">Demande à l’hôte de modifier les limites de mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5629d-103">Requests the host to change the limits of virtual memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5629d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5629d-104">Syntax</span></span>  
  
```  
HRESULT RequestVirtualMemLimit (  
    [in] SIZE_T       sztMaxVirtualMemMB,  
    [in, out] SIZE_T* psztNewMaxVirtualMemMB  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5629d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5629d-105">Parameters</span></span>  
 `sztMaxVirtualMemMB`  
 <span data-ttu-id="5629d-106">[in] La taille de la mémoire à allouer.</span><span class="sxs-lookup"><span data-stu-id="5629d-106">[in] The requested size of memory to be allocated.</span></span>  
  
 `psztNewMaxVirtualMemMB`  
 <span data-ttu-id="5629d-107">[in, out] Pointeur vers la taille réelle de mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="5629d-107">[in, out] A pointer to the actual size of memory allocated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5629d-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5629d-108">Requirements</span></span>  
 <span data-ttu-id="5629d-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5629d-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5629d-110">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="5629d-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5629d-111">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5629d-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="5629d-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="5629d-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="5629d-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5629d-113">See also</span></span>

- [<span data-ttu-id="5629d-114">IGCHostControl, interface</span><span class="sxs-lookup"><span data-stu-id="5629d-114">IGCHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchostcontrol-interface.md)
