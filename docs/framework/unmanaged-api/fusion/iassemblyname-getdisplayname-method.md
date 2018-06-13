---
title: IAssemblyName::GetDisplayName, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetDisplayName
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetDisplayName
helpviewer_keywords:
- GetDisplayName method, IAssemblyName interface [.NET Framework fusion]
- IAssemblyName::GetDisplayName method [.NET Framework fusion]
ms.assetid: 9a26547a-9a34-4284-a463-78a7d4b496cf
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 00a95646323a5ee08d6758b0f6a7c493c661705d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431774"
---
# <a name="iassemblynamegetdisplayname-method"></a><span data-ttu-id="8ba4b-102">IAssemblyName::GetDisplayName, méthode</span><span class="sxs-lookup"><span data-stu-id="8ba4b-102">IAssemblyName::GetDisplayName Method</span></span>
<span data-ttu-id="8ba4b-103">Obtient le nom explicite de l’assembly référencé par ce [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="8ba4b-103">Gets the human-readable name of the assembly referenced by this [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ba4b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ba4b-104">Syntax</span></span>  
  
```  
HRESULT GetDisplayName (  
        [out]      LPOLESTR  szDisplayName,  
        [in, out]  LPDWORD   pccDisplayName,  
        [in]       DWORD     dwDisplayFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8ba4b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ba4b-105">Parameters</span></span>  
 `szDisplayName`  
 <span data-ttu-id="8ba4b-106">[out] La mémoire tampon de chaîne qui contient le nom de l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="8ba4b-106">[out] The string buffer that contains the name of the referenced assembly.</span></span>  
  
 `pccDisplayName`  
 <span data-ttu-id="8ba4b-107">[dans, out] La taille de `szDisplayName` en caractères larges, y compris un caractère de marque de fin null.</span><span class="sxs-lookup"><span data-stu-id="8ba4b-107">[in, out] The size of `szDisplayName` in wide characters, including a null terminator character.</span></span>  
  
 `dwDisplayFlags`  
 <span data-ttu-id="8ba4b-108">[in] Une combinaison d’opérations de [ASM_DISPLAY_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-display-flags-enumeration.md) valeurs qui influencent les fonctionnalités de `szDisplayName`.</span><span class="sxs-lookup"><span data-stu-id="8ba4b-108">[in] A bitwise combination of [ASM_DISPLAY_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-display-flags-enumeration.md) values that influence the features of `szDisplayName`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ba4b-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8ba4b-109">Requirements</span></span>  
 <span data-ttu-id="8ba4b-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8ba4b-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ba4b-111">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="8ba4b-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="8ba4b-112">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ba4b-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ba4b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ba4b-113">See Also</span></span>  
 [<span data-ttu-id="8ba4b-114">IAssemblyName, interface</span><span class="sxs-lookup"><span data-stu-id="8ba4b-114">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)  
 [<span data-ttu-id="8ba4b-115">Énumérations de fusion</span><span class="sxs-lookup"><span data-stu-id="8ba4b-115">Fusion Enumerations</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-enumerations.md)
