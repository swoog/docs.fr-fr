---
title: GetAppIdAuthority, fonction
ms.date: 03/30/2017
api_name:
- GetAppIdAuthority
api_location:
- fusion.dll
- clr.dll
api_type:
- COM
f1_keywords:
- GetAppIdAuthority
helpviewer_keywords:
- GetAppIdAuthority function [.NET Framework fusion]
ms.assetid: 9f968dad-0d09-47fb-bebc-94c39a0d16ad
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c45da047d384e56440ca5f883a4cfd755a7d0299
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54719710"
---
# <a name="getappidauthority-function"></a><span data-ttu-id="ab5d5-102">GetAppIdAuthority, fonction</span><span class="sxs-lookup"><span data-stu-id="ab5d5-102">GetAppIdAuthority Function</span></span>
<span data-ttu-id="ab5d5-103">Obtient un pointeur vers un [IAppIdAuthority](../../../../docs/framework/unmanaged-api/fusion/iappidauthority-interface.md) instance qui gère des clés pour les identités d’application et les références.</span><span class="sxs-lookup"><span data-stu-id="ab5d5-103">Gets a pointer to an [IAppIdAuthority](../../../../docs/framework/unmanaged-api/fusion/iappidauthority-interface.md) instance that manages keys for application identities and references.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab5d5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab5d5-104">Syntax</span></span>  
  
```  
HRESULT GetAppIdAuthority (  
    [out] IAppIdAuthority **ppIAppIdAuthority  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ab5d5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab5d5-105">Parameters</span></span>  
 `ppIAppIdAuthority`  
 <span data-ttu-id="ab5d5-106">[out] Retourné `IAppIdAuthority` pointeur.</span><span class="sxs-lookup"><span data-stu-id="ab5d5-106">[out] The returned `IAppIdAuthority` pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ab5d5-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ab5d5-107">Requirements</span></span>  
 <span data-ttu-id="ab5d5-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ab5d5-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab5d5-109">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="ab5d5-109">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="ab5d5-110">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ab5d5-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab5d5-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab5d5-111">See also</span></span>
- [<span data-ttu-id="ab5d5-112">IAppIdAuthority, interface</span><span class="sxs-lookup"><span data-stu-id="ab5d5-112">IAppIdAuthority Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iappidauthority-interface.md)
- [<span data-ttu-id="ab5d5-113">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="ab5d5-113">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
