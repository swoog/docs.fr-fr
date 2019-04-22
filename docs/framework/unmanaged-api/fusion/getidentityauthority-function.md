---
title: GetIdentityAuthority, fonction
ms.date: 03/30/2017
api_name:
- GetIdentityAuthority
api_location:
- fusion.dll
- clr.dll
api_type:
- COM
f1_keywords:
- GetIdentityAuthority
helpviewer_keywords:
- GetIdentityAuthority function [.NET Framework fusion]
ms.assetid: 843cd5ab-d2b7-4ff6-86bd-e68c7a91c098
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3090887d3c670b2784b7b40c7d63832715596c3b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59141516"
---
# <a name="getidentityauthority-function"></a><span data-ttu-id="f7182-102">GetIdentityAuthority, fonction</span><span class="sxs-lookup"><span data-stu-id="f7182-102">GetIdentityAuthority Function</span></span>
<span data-ttu-id="f7182-103">Obtient un pointeur vers un [IIdentityAuthority](../../../../docs/framework/unmanaged-api/fusion/iidentityauthority-interface.md) instance qui gère des clés pour les objets de code.</span><span class="sxs-lookup"><span data-stu-id="f7182-103">Gets a pointer to an [IIdentityAuthority](../../../../docs/framework/unmanaged-api/fusion/iidentityauthority-interface.md) instance that manages keys for code objects.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f7182-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7182-104">Syntax</span></span>  
  
```  
HRESULT GetIdentityAuthority (  
    [out] IIdentityAuthority   **ppIIdentityAuthority  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="f7182-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7182-105">Parameters</span></span>  
 `ppIIdentityAuthority`  
 <span data-ttu-id="f7182-106">[out] Retourné `IIdentityAuthority` pointeur.</span><span class="sxs-lookup"><span data-stu-id="f7182-106">[out] The returned `IIdentityAuthority` pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f7182-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7182-107">Requirements</span></span>  
 <span data-ttu-id="f7182-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f7182-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f7182-109">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="f7182-109">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="f7182-110">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f7182-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f7182-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7182-111">See also</span></span>

- [<span data-ttu-id="f7182-112">IIdentityAuthority, interface</span><span class="sxs-lookup"><span data-stu-id="f7182-112">IIdentityAuthority Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iidentityauthority-interface.md)
- [<span data-ttu-id="f7182-113">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="f7182-113">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
