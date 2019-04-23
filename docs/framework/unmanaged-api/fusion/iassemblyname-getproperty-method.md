---
title: IAssemblyName::GetProperty, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetProperty
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetProperty
helpviewer_keywords:
- IAssemblyName::GetProperty method [.NET Framework fusion]
- GetProperty method [.NET Framework fusion]
ms.assetid: e59fda62-77d5-4e37-89cb-ce7ae4627975
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9af0773c2ef066c103f823e4d28c0fd6e9eadc24
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59086557"
---
# <a name="iassemblynamegetproperty-method"></a><span data-ttu-id="81235-102">IAssemblyName::GetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="81235-102">IAssemblyName::GetProperty Method</span></span>
<span data-ttu-id="81235-103">Obtient un pointeur vers la propriété référencée par l’identificateur de propriété spécifié.</span><span class="sxs-lookup"><span data-stu-id="81235-103">Gets a pointer to the property referenced by the specified property identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81235-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81235-104">Syntax</span></span>  
  
```  
HRESULT GetProperty (  
    [in]      DWORD    PropertyId,  
    [out]     LPVOID   pvProperty,  
    [in, out] LPDWORD  pcbProperty  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="81235-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81235-105">Parameters</span></span>  
 `PropertyId`  
 <span data-ttu-id="81235-106">[in] Identificateur unique pour la propriété demandée.</span><span class="sxs-lookup"><span data-stu-id="81235-106">[in] The unique identifier for the requested property.</span></span>  
  
 `pvProperty`  
 <span data-ttu-id="81235-107">[out] Les données de la propriété retournée.</span><span class="sxs-lookup"><span data-stu-id="81235-107">[out] The returned property data.</span></span>  
  
 `pcbProperty`  
 <span data-ttu-id="81235-108">[in, out] La taille, en octets, de `pvProperty`.</span><span class="sxs-lookup"><span data-stu-id="81235-108">[in, out] The size, in bytes, of `pvProperty`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="81235-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81235-109">Requirements</span></span>  
 <span data-ttu-id="81235-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="81235-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="81235-111">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="81235-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="81235-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="81235-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81235-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81235-113">See also</span></span>

- [<span data-ttu-id="81235-114">IAssemblyName, interface</span><span class="sxs-lookup"><span data-stu-id="81235-114">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
