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
ms.openlocfilehash: 1194ae12710ce9ef6d5f53e584493eec0541f3fd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54569714"
---
# <a name="getidentityauthority-function"></a><span data-ttu-id="3e772-102">GetIdentityAuthority, fonction</span><span class="sxs-lookup"><span data-stu-id="3e772-102">GetIdentityAuthority Function</span></span>
<span data-ttu-id="3e772-103">Obtient un pointeur vers un [IIdentityAuthority](../../../../docs/framework/unmanaged-api/fusion/iidentityauthority-interface.md) instance qui gère des clés pour les objets de code.</span><span class="sxs-lookup"><span data-stu-id="3e772-103">Gets a pointer to an [IIdentityAuthority](../../../../docs/framework/unmanaged-api/fusion/iidentityauthority-interface.md) instance that manages keys for code objects.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e772-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e772-104">Syntax</span></span>  
  
```  
HRESULT GetIdentityAuthority (  
    [out] IIdentityAuthority   **ppIIdentityAuthority  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3e772-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e772-105">Parameters</span></span>  
 `ppIIdentityAuthority`  
 <span data-ttu-id="3e772-106">[out] Retourné `IIdentityAuthority` pointeur.</span><span class="sxs-lookup"><span data-stu-id="3e772-106">[out] The returned `IIdentityAuthority` pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e772-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3e772-107">Requirements</span></span>  
 <span data-ttu-id="3e772-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3e772-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3e772-109">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="3e772-109">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="3e772-110">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3e772-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e772-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e772-111">See also</span></span>
- [<span data-ttu-id="3e772-112">IIdentityAuthority, interface</span><span class="sxs-lookup"><span data-stu-id="3e772-112">IIdentityAuthority Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iidentityauthority-interface.md)
- [<span data-ttu-id="3e772-113">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="3e772-113">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
