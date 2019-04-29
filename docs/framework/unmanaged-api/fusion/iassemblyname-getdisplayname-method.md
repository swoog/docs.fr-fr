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
ms.openlocfilehash: 323c883b4010f3ddd4c575e5d5fc40a3419e57c2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697405"
---
# <a name="iassemblynamegetdisplayname-method"></a><span data-ttu-id="86c16-102">IAssemblyName::GetDisplayName, méthode</span><span class="sxs-lookup"><span data-stu-id="86c16-102">IAssemblyName::GetDisplayName Method</span></span>
<span data-ttu-id="86c16-103">Obtient le nom lisible de l’assembly référencé par ce [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="86c16-103">Gets the human-readable name of the assembly referenced by this [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86c16-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86c16-104">Syntax</span></span>  
  
```  
HRESULT GetDisplayName (  
        [out]      LPOLESTR  szDisplayName,  
        [in, out]  LPDWORD   pccDisplayName,  
        [in]       DWORD     dwDisplayFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="86c16-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86c16-105">Parameters</span></span>  
 `szDisplayName`  
 <span data-ttu-id="86c16-106">[out] La mémoire tampon de chaîne qui contient le nom de l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="86c16-106">[out] The string buffer that contains the name of the referenced assembly.</span></span>  
  
 `pccDisplayName`  
 <span data-ttu-id="86c16-107">[in, out] La taille de `szDisplayName` en caractères larges, y compris un caractère de marque de fin null.</span><span class="sxs-lookup"><span data-stu-id="86c16-107">[in, out] The size of `szDisplayName` in wide characters, including a null terminator character.</span></span>  
  
 `dwDisplayFlags`  
 <span data-ttu-id="86c16-108">[in] Une combinaison au niveau du bit de [ASM_DISPLAY_FLAGS pour](../../../../docs/framework/unmanaged-api/fusion/asm-display-flags-enumeration.md) valeurs qui influencent les fonctionnalités de `szDisplayName`.</span><span class="sxs-lookup"><span data-stu-id="86c16-108">[in] A bitwise combination of [ASM_DISPLAY_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-display-flags-enumeration.md) values that influence the features of `szDisplayName`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86c16-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86c16-109">Requirements</span></span>  
 <span data-ttu-id="86c16-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="86c16-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86c16-111">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="86c16-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="86c16-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="86c16-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86c16-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86c16-113">See also</span></span>

- [<span data-ttu-id="86c16-114">IAssemblyName, interface</span><span class="sxs-lookup"><span data-stu-id="86c16-114">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
- [<span data-ttu-id="86c16-115">Énumérations de fusion</span><span class="sxs-lookup"><span data-stu-id="86c16-115">Fusion Enumerations</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-enumerations.md)
