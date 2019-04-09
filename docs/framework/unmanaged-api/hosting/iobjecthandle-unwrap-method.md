---
title: IObjectHandle::Unwrap, méthode
ms.date: 03/30/2017
api_name:
- IObjectHandle.Unwrap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- Unwrap
helpviewer_keywords:
- Unwrap method [.NET Framework hosting]
- IObjectHandle::Unwrap method [.NET Framework hosting]
ms.assetid: 794c6f8e-ed58-416b-b756-e864f2c958f7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4c18607d5373b415228846350a3dd0637ade1b45
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59150798"
---
# <a name="iobjecthandleunwrap-method"></a><span data-ttu-id="38822-102">IObjectHandle::Unwrap, méthode</span><span class="sxs-lookup"><span data-stu-id="38822-102">IObjectHandle::Unwrap Method</span></span>
<span data-ttu-id="38822-103">Désencapsule un objet marshalé par valeur à partir de l’indirection.</span><span class="sxs-lookup"><span data-stu-id="38822-103">Unwraps a marshal-by-value object from indirection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38822-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38822-104">Syntax</span></span>  
  
```  
HRESULT Unwrap (  
    [out, retval] VARIANT *ppv  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="38822-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38822-105">Parameters</span></span>  
 `ppv`  
 <span data-ttu-id="38822-106">[out] Pointeur vers l’objet à désencapsuler.</span><span class="sxs-lookup"><span data-stu-id="38822-106">[out] A pointer to the object to be unwrapped.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="38822-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38822-107">Requirements</span></span>  
 <span data-ttu-id="38822-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="38822-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="38822-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="38822-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="38822-110">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="38822-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="38822-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="38822-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
