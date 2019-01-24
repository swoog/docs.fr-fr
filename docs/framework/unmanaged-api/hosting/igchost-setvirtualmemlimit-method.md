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
ms.openlocfilehash: d38b174a7e959647a9c1f5287b8acbbcdaf5ca7b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564277"
---
# <a name="igchostsetvirtualmemlimit-method"></a><span data-ttu-id="cfe40-102">IGCHost::SetVirtualMemLimit, méthode</span><span class="sxs-lookup"><span data-stu-id="cfe40-102">IGCHost::SetVirtualMemLimit Method</span></span>
<span data-ttu-id="cfe40-103">Définit la taille maximale de mémoire virtuelle du runtime.</span><span class="sxs-lookup"><span data-stu-id="cfe40-103">Sets the maximum size of the runtime's virtual memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cfe40-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfe40-104">Syntax</span></span>  
  
```  
HRESULT SetVirtualMemLimit (  
    [in] SIZE_T sztMaxVirtualMemMB  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cfe40-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfe40-105">Parameters</span></span>  
 `sztMaxVirtualMemMB`  
 <span data-ttu-id="cfe40-106">[in] La taille maximale, en mégaoctets, de mémoire virtuelle du runtime.</span><span class="sxs-lookup"><span data-stu-id="cfe40-106">[in] The maximum size, in megabytes, of the runtime's virtual memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cfe40-107">Notes</span><span class="sxs-lookup"><span data-stu-id="cfe40-107">Remarks</span></span>  
 <span data-ttu-id="cfe40-108">La taille maximale de mémoire virtuelle du runtime peut être modifiée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="cfe40-108">The maximum size of the runtime's virtual memory can be changed dynamically.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cfe40-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cfe40-109">Requirements</span></span>  
 <span data-ttu-id="cfe40-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cfe40-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cfe40-111">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="cfe40-111">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="cfe40-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cfe40-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cfe40-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cfe40-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cfe40-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfe40-114">See also</span></span>
- [<span data-ttu-id="cfe40-115">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="cfe40-115">IGCHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)
