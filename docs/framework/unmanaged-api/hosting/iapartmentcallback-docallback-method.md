---
title: IApartmentCallback::DoCallback, méthode
ms.date: 03/30/2017
api_name:
- IApartmentCallback.DoCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- DoCallback
helpviewer_keywords:
- IApartmentCallback::DoCallback method [.NET Framework hosting]
- DoCallback method [.NET Framework hosting]
ms.assetid: 8edad30c-30ff-4bee-813c-75525a82fc93
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ba1dc2a1ec8b0b3b5ec25036cab6362237efe98f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33430754"
---
# <a name="iapartmentcallbackdocallback-method"></a><span data-ttu-id="eb3bf-102">IApartmentCallback::DoCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="eb3bf-102">IApartmentCallback::DoCallback Method</span></span>
<span data-ttu-id="eb3bf-103">Exécute la fonction spécifiée dans un thread cloisonné.</span><span class="sxs-lookup"><span data-stu-id="eb3bf-103">Executes the specified function within an apartment.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb3bf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb3bf-104">Syntax</span></span>  
  
```  
HRESULT _stdcall DoCallback(  
    [in] SIZE_T pFunc,  
    [in] SIZE_T pData  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="eb3bf-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb3bf-105">Parameters</span></span>  
 `pFunc`  
 <span data-ttu-id="eb3bf-106">[in] Pointeur vers la fonction à exécuter dans le cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="eb3bf-106">[in] A pointer to the function to be executed within the apartment.</span></span>  
  
 `pData`  
 <span data-ttu-id="eb3bf-107">[in] Pointeur vers l’argument de la fonction.</span><span class="sxs-lookup"><span data-stu-id="eb3bf-107">[in] A pointer to the function's argument.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eb3bf-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="eb3bf-108">Requirements</span></span>  
 <span data-ttu-id="eb3bf-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eb3bf-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eb3bf-110">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="eb3bf-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="eb3bf-111">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="eb3bf-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="eb3bf-112">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eb3bf-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb3bf-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb3bf-113">See Also</span></span>  
 [<span data-ttu-id="eb3bf-114">IApartmentCallback, interface</span><span class="sxs-lookup"><span data-stu-id="eb3bf-114">IApartmentCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iapartmentcallback-interface.md)
