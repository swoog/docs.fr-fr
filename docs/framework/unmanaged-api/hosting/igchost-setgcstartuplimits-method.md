---
title: IGCHost::SetGCStartupLimits, méthode
ms.date: 03/30/2017
api_name:
- IGCHost.SetGCStartupLimits
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetGCStartupLimits
helpviewer_keywords:
- SetGCStartupLimits method, IGCHost interface [.NET Framework hosting]
- IGCHost::SetGCStartupLimits method [.NET Framework hosting]
ms.assetid: cae53926-82ac-4d1d-b297-0bde0bd1bebb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 365261883f0b81884bb7cf70614628c05f9067c5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61993263"
---
# <a name="igchostsetgcstartuplimits-method"></a><span data-ttu-id="2ad1d-102">IGCHost::SetGCStartupLimits, méthode</span><span class="sxs-lookup"><span data-stu-id="2ad1d-102">IGCHost::SetGCStartupLimits Method</span></span>
<span data-ttu-id="2ad1d-103">Définit la taille du segment et la taille maximale pour la génération 0.</span><span class="sxs-lookup"><span data-stu-id="2ad1d-103">Sets the segment size and the maximum size for generation 0.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="2ad1d-104">En commençant par le [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)], vous pouvez définir la taille des segments de taille maximale de génération 0 aux valeurs et supérieur à `DWORD` à l’aide de la [IGCHost2::SetGCStartupLimitsEx](../../../../docs/framework/unmanaged-api/hosting/igchost2-setgcstartuplimitsex-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="2ad1d-104">Starting with the [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)], you can set segment size and maximum generation 0 size to values greater than `DWORD` by using the [IGCHost2::SetGCStartupLimitsEx](../../../../docs/framework/unmanaged-api/hosting/igchost2-setgcstartuplimitsex-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2ad1d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ad1d-105">Syntax</span></span>  
  
```  
HRESULT SetGCStartupLimits (  
    [in] DWORD SegmentSize,  
    [in] DWORD MaxGen0Size  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2ad1d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ad1d-106">Parameters</span></span>  
 `SegmentSize`  
 <span data-ttu-id="2ad1d-107">[in] La taille du segment utilisé par le système de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="2ad1d-107">[in] The size of the segment used by the garbage collection system.</span></span>  
  
 `MaxGen0Size`  
 <span data-ttu-id="2ad1d-108">[in] La taille maximale pour la génération 0.</span><span class="sxs-lookup"><span data-stu-id="2ad1d-108">[in] The maximum size for generation 0.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2ad1d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2ad1d-109">Remarks</span></span>  
 <span data-ttu-id="2ad1d-110">Le `SetGCStartupLimits` méthode peut être appelée qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="2ad1d-110">The `SetGCStartupLimits` method may be called only once.</span></span> <span data-ttu-id="2ad1d-111">Ces valeurs ne peuvent pas être modifiées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="2ad1d-111">These values cannot be changed later.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2ad1d-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ad1d-112">Requirements</span></span>  
 <span data-ttu-id="2ad1d-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2ad1d-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2ad1d-114">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="2ad1d-114">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="2ad1d-115">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2ad1d-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2ad1d-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2ad1d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2ad1d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ad1d-117">See also</span></span>

- [<span data-ttu-id="2ad1d-118">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="2ad1d-118">IGCHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)
