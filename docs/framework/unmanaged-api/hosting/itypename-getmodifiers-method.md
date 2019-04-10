---
title: ITypeName::GetModifiers, méthode
ms.date: 03/30/2017
api_name:
- ITypeName.GetModifiers
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetModifiers
helpviewer_keywords:
- ITypeName::GetModifiers method [.NET Framework hosting]
- GetModifiers method [.NET Framework hosting]
ms.assetid: 75508c55-3e09-4135-80da-cc811003fa82
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 78d86aff385bbff479c57d8902fbd0973a6ad1bc
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59226415"
---
# <a name="itypenamegetmodifiers-method"></a><span data-ttu-id="3d253-102">ITypeName::GetModifiers, méthode</span><span class="sxs-lookup"><span data-stu-id="3d253-102">ITypeName::GetModifiers Method</span></span>
<span data-ttu-id="3d253-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="3d253-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3d253-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d253-104">Syntax</span></span>  
  
```  
HRESULT GetModifiers (  
    [in] DWORD           count,  
    [out] DWORD*         rgModifiers,  
    [out, retval] DWORD* pCount  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="3d253-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d253-105">Requirements</span></span>  
 <span data-ttu-id="3d253-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3d253-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3d253-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3d253-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3d253-108">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3d253-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="3d253-109">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="3d253-109">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3d253-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d253-110">See also</span></span>

- [<span data-ttu-id="3d253-111">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="3d253-111">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
