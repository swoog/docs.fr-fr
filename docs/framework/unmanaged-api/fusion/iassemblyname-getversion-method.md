---
title: IAssemblyName::GetVersion, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetVersion
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetVersion
helpviewer_keywords:
- IAssemblyName::GetVersion method [.NET Framework fusion]
- GetVersion method, IAssemblyName interface [.NET Framework fusion]
ms.assetid: 42230928-2c33-41fd-9519-d96efef6c7af
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7479e8d1eee0c44544b5923d4de66153cb2c3a19
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57490331"
---
# <a name="iassemblynamegetversion-method"></a><span data-ttu-id="1d74e-102">IAssemblyName::GetVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="1d74e-102">IAssemblyName::GetVersion Method</span></span>
<span data-ttu-id="1d74e-103">Obtient les informations de version pour l’assembly référencé par ce [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="1d74e-103">Gets the version information for the assembly referenced by this [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1d74e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d74e-104">Syntax</span></span>  
  
```  
HRESULT GetVersion (  
    [out] LPDWORD pdwVersionHi,  
    [out] LPDWORD pdwVersionLow  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1d74e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d74e-105">Parameters</span></span>  
 `pdwVersionHi`  
 <span data-ttu-id="1d74e-106">[out] 32 bits de poids fort de la version.</span><span class="sxs-lookup"><span data-stu-id="1d74e-106">[out] The high 32 bits of the version.</span></span>  
  
 `pdwVersionLow`  
 <span data-ttu-id="1d74e-107">[out] 32 bits de poids faibles de la version.</span><span class="sxs-lookup"><span data-stu-id="1d74e-107">[out] The low 32 bits of the version.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1d74e-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1d74e-108">Requirements</span></span>  
 <span data-ttu-id="1d74e-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1d74e-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1d74e-110">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="1d74e-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="1d74e-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1d74e-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d74e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d74e-112">See also</span></span>
- [<span data-ttu-id="1d74e-113">IAssemblyName, interface</span><span class="sxs-lookup"><span data-stu-id="1d74e-113">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
