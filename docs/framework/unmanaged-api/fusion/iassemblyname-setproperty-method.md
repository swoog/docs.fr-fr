---
title: IAssemblyName::SetProperty, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyName.SetProperty
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::SetProperty
helpviewer_keywords:
- IAssemblyName::SetProperty method [.NET Framework fusion]
- SetProperty method [.NET Framework fusion]
ms.assetid: 496c3add-f60b-4073-943f-d1bcf33330cb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ca2d7fe73fc749296f76e18ecce75b7fdd0795d3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54585589"
---
# <a name="iassemblynamesetproperty-method"></a><span data-ttu-id="48c44-102">IAssemblyName::SetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="48c44-102">IAssemblyName::SetProperty Method</span></span>
<span data-ttu-id="48c44-103">Définit la valeur de la propriété référencée par l’identificateur de propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="48c44-103">Sets the value of the property referenced by the specified property identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="48c44-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48c44-104">Syntax</span></span>  
  
```  
HRESULT SetProperty (  
    [in] DWORD  PropertyId,  
    [in] LPVOID pvProperty,  
    [in] DWORD  cbProperty  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="48c44-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48c44-105">Parameters</span></span>  
 `PropertyId`  
 <span data-ttu-id="48c44-106">[in] Identificateur unique de la propriété dont la valeur sera définie.</span><span class="sxs-lookup"><span data-stu-id="48c44-106">[in] The unique identifier of the property whose value will be set.</span></span>  
  
 `pvProperty`  
 <span data-ttu-id="48c44-107">[in] La valeur à laquelle définir la propriété référencée par `PropertyId`.</span><span class="sxs-lookup"><span data-stu-id="48c44-107">[in] The value to which to set the property referenced by `PropertyId`.</span></span>  
  
 `cbProperty`  
 <span data-ttu-id="48c44-108">[in] La taille, en octets, de `pvProperty`.</span><span class="sxs-lookup"><span data-stu-id="48c44-108">[in] The size, in bytes, of `pvProperty`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="48c44-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="48c44-109">Requirements</span></span>  
 <span data-ttu-id="48c44-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="48c44-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="48c44-111">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="48c44-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="48c44-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="48c44-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48c44-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48c44-113">See also</span></span>
- [<span data-ttu-id="48c44-114">IAssemblyName, interface</span><span class="sxs-lookup"><span data-stu-id="48c44-114">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
