---
title: ITypeName::GetNames, méthode
ms.date: 03/30/2017
api_name:
- ITypeName.GetNames
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetNames
helpviewer_keywords:
- ITypeName::GetNames method [.NET Framework hosting]
- GetNames method [.NET Framework hosting]
ms.assetid: e2a3637b-d1e9-4d93-9e9b-0555fbff793d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 28076a36880febad20d457ff5a6b290de3d6f173
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59121548"
---
# <a name="itypenamegetnames-method"></a><span data-ttu-id="e8625-102">ITypeName::GetNames, méthode</span><span class="sxs-lookup"><span data-stu-id="e8625-102">ITypeName::GetNames Method</span></span>
<span data-ttu-id="e8625-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="e8625-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8625-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8625-104">Syntax</span></span>  
  
```  
HRESULT GetNames (  
    [in] DWORD           count,  
    [out] BSTR*          rgbszNames,  
    [out, retval] DWORD* pCount  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="e8625-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8625-105">Requirements</span></span>  
 <span data-ttu-id="e8625-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e8625-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8625-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e8625-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e8625-108">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e8625-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="e8625-109">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="e8625-109">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="e8625-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8625-110">See also</span></span>

- [<span data-ttu-id="e8625-111">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="e8625-111">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
