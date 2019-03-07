---
title: IGCHost::SetVirtualMemLimit, méthode
ms.date: 03/30/2017
api_name:
- IGCHost.SetVirtualMemLimit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetVirtualMemLimit
helpviewer_keywords:
- IGCHost::SetVirtualMemLimit method [.NET Framework hosting]
- SetVirtualMemLimit method [.NET Framework hosting]
ms.assetid: c7e7c2d0-e58c-4650-b40c-47b2be2cda45
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b25e9c738c95a918b79d3fd324787e4aaf3aaa7f
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57502473"
---
# <a name="igchostsetvirtualmemlimit-method"></a><span data-ttu-id="ea6d5-102">IGCHost::SetVirtualMemLimit, méthode</span><span class="sxs-lookup"><span data-stu-id="ea6d5-102">IGCHost::SetVirtualMemLimit Method</span></span>
<span data-ttu-id="ea6d5-103">Définit la taille maximale de mémoire virtuelle du runtime.</span><span class="sxs-lookup"><span data-stu-id="ea6d5-103">Sets the maximum size of the runtime's virtual memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea6d5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea6d5-104">Syntax</span></span>  
  
```  
HRESULT SetVirtualMemLimit (  
    [in] SIZE_T sztMaxVirtualMemMB  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ea6d5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea6d5-105">Parameters</span></span>  
 `sztMaxVirtualMemMB`  
 <span data-ttu-id="ea6d5-106">[in] La taille maximale, en mégaoctets, de mémoire virtuelle du runtime.</span><span class="sxs-lookup"><span data-stu-id="ea6d5-106">[in] The maximum size, in megabytes, of the runtime's virtual memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ea6d5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ea6d5-107">Remarks</span></span>  
 <span data-ttu-id="ea6d5-108">La taille maximale de mémoire virtuelle du runtime peut être modifiée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="ea6d5-108">The maximum size of the runtime's virtual memory can be changed dynamically.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ea6d5-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ea6d5-109">Requirements</span></span>  
 <span data-ttu-id="ea6d5-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ea6d5-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ea6d5-111">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="ea6d5-111">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="ea6d5-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ea6d5-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ea6d5-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ea6d5-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ea6d5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea6d5-114">See also</span></span>
- [<span data-ttu-id="ea6d5-115">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="ea6d5-115">IGCHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)
