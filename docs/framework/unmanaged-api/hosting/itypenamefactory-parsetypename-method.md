---
title: ITypeNameFactory::ParseTypeName, méthode
ms.date: 03/30/2017
api_name:
- ITypeNameFactory.ParseTypeName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ParseTypeName
helpviewer_keywords:
- ITypeNameFactory::ParseTypeName method [.NET Framework hosting]
- ParseTypeName method [.NET Framework hosting]
ms.assetid: 13c9f063-371c-4911-a5e7-e1e0b88ae382
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cbe5f634a5d0580c7e58b03f318da98a0112fa6b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59208083"
---
# <a name="itypenamefactoryparsetypename-method"></a><span data-ttu-id="77d1e-102">ITypeNameFactory::ParseTypeName, méthode</span><span class="sxs-lookup"><span data-stu-id="77d1e-102">ITypeNameFactory::ParseTypeName Method</span></span>
<span data-ttu-id="77d1e-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="77d1e-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77d1e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77d1e-104">Syntax</span></span>  
  
```  
HRESULT ParseTypeName (  
    [in]  LPCWSTR             szName,  
    [out] DWORD*              pError,  
    [out, retval] ITypeName** ppTypeName  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="77d1e-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77d1e-105">Requirements</span></span>  
 <span data-ttu-id="77d1e-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="77d1e-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77d1e-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="77d1e-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="77d1e-108">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="77d1e-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="77d1e-109">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="77d1e-109">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="77d1e-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77d1e-110">See also</span></span>

- [<span data-ttu-id="77d1e-111">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="77d1e-111">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
