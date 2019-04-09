---
title: IMetaDataEmit::SetPinvokeMap, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetPinvokeMap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetPinvokeMap
helpviewer_keywords:
- IMetaDataEmit::SetPinvokeMap method [.NET Framework metadata]
- SetPinvokeMap method [.NET Framework metadata]
ms.assetid: c6bfd574-1da3-4ba7-82f2-46ca5efcbaba
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b838a83a160707e546b05ef334eb17d0c6e6cc27
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59133560"
---
# <a name="imetadataemitsetpinvokemap-method"></a><span data-ttu-id="82223-102">IMetaDataEmit::SetPinvokeMap, méthode</span><span class="sxs-lookup"><span data-stu-id="82223-102">IMetaDataEmit::SetPinvokeMap Method</span></span>
<span data-ttu-id="82223-103">Définit ou modifie les fonctionnalités de la signature de PInvoke d’une méthode, comme défini par un appel antérieur à [IMetaDataEmit::DefinePinvokeMap](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepinvokemap-method.md).</span><span class="sxs-lookup"><span data-stu-id="82223-103">Sets or changes features of a method's PInvoke signature, as defined by a prior call to [IMetaDataEmit::DefinePinvokeMap](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepinvokemap-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82223-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82223-104">Syntax</span></span>  
  
```  
HRESULT SetPinvokeMap (   
    [in]  mdToken      tk,   
    [in]  DWORD        dwMappingFlags,  
    [in]  LPCWSTR      szImportName,   
    [in]  mdModuleRef  mrImportDLL   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="82223-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82223-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="82223-106">[in] Le `mdToken` pour que le mappage des informations s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="82223-106">[in] The `mdToken` to which mapping information applies.</span></span>  
  
 `dwMappingFlags`  
 <span data-ttu-id="82223-107">[in] Indicateurs utilisés par PInvoke pour effectuer le mappage.</span><span class="sxs-lookup"><span data-stu-id="82223-107">[in] Flags used by PInvoke to do the mapping.</span></span> <span data-ttu-id="82223-108">Il s’agit d’un masque de bits de `CorPinvokeMap` valeurs.</span><span class="sxs-lookup"><span data-stu-id="82223-108">This is a bitmask of `CorPinvokeMap` values.</span></span>  
  
 `szImportName`  
 <span data-ttu-id="82223-109">[in] Le nom de l’exportation de la cible de la DLL native.</span><span class="sxs-lookup"><span data-stu-id="82223-109">[in] The name of the target export in the native DLL.</span></span>  
  
 `mrImportDLL`  
 <span data-ttu-id="82223-110">[in] Le `mdModuleRef` jeton pour la cible de DLL non managée.</span><span class="sxs-lookup"><span data-stu-id="82223-110">[in] The `mdModuleRef` token for the target unmanaged DLL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="82223-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82223-111">Requirements</span></span>  
 <span data-ttu-id="82223-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="82223-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="82223-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="82223-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="82223-114">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="82223-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="82223-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="82223-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="82223-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82223-116">See also</span></span>

- [<span data-ttu-id="82223-117">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="82223-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="82223-118">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="82223-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
