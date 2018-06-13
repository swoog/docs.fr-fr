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
ms.openlocfilehash: adc72eb1b50369e5219798cdb99618abc5e08a00
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33440387"
---
# <a name="itypenamefactoryparsetypename-method"></a><span data-ttu-id="62bb9-102">ITypeNameFactory::ParseTypeName, méthode</span><span class="sxs-lookup"><span data-stu-id="62bb9-102">ITypeNameFactory::ParseTypeName Method</span></span>
<span data-ttu-id="62bb9-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="62bb9-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62bb9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62bb9-104">Syntax</span></span>  
  
```  
HRESULT ParseTypeName (  
    [in]  LPCWSTR             szName,  
    [out] DWORD*              pError,  
    [out, retval] ITypeName** ppTypeName  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="62bb9-105">Spécifications</span><span class="sxs-lookup"><span data-stu-id="62bb9-105">Requirements</span></span>  
 <span data-ttu-id="62bb9-106">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="62bb9-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="62bb9-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="62bb9-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="62bb9-108">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="62bb9-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="62bb9-109">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="62bb9-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62bb9-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62bb9-110">See Also</span></span>  
 [<span data-ttu-id="62bb9-111">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="62bb9-111">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
