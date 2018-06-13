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
ms.openlocfilehash: 0d9a8f9aa910054a4541e4ff8c1f7cad63077ba8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33439948"
---
# <a name="iobjecthandleunwrap-method"></a><span data-ttu-id="8f100-102">IObjectHandle::Unwrap, méthode</span><span class="sxs-lookup"><span data-stu-id="8f100-102">IObjectHandle::Unwrap Method</span></span>
<span data-ttu-id="8f100-103">Désencapsule un objet marshalé-par-valeur à partir de l’indirection.</span><span class="sxs-lookup"><span data-stu-id="8f100-103">Unwraps a marshal-by-value object from indirection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f100-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f100-104">Syntax</span></span>  
  
```  
HRESULT Unwrap (  
    [out, retval] VARIANT *ppv  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8f100-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f100-105">Parameters</span></span>  
 `ppv`  
 <span data-ttu-id="8f100-106">[out] Pointeur vers l’objet à désencapsuler.</span><span class="sxs-lookup"><span data-stu-id="8f100-106">[out] A pointer to the object to be unwrapped.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8f100-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8f100-107">Requirements</span></span>  
 <span data-ttu-id="8f100-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8f100-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8f100-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8f100-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8f100-110">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8f100-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8f100-111">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8f100-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f100-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f100-112">See Also</span></span>  
 
