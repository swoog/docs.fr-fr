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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049995"
---
# <a name="imetadataemitsetpinvokemap-method"></a><span data-ttu-id="e9f40-102">IMetaDataEmit::SetPinvokeMap, méthode</span><span class="sxs-lookup"><span data-stu-id="e9f40-102">IMetaDataEmit::SetPinvokeMap Method</span></span>
<span data-ttu-id="e9f40-103">Définit ou modifie les fonctionnalités de la signature de PInvoke d’une méthode, comme défini par un appel antérieur à [IMetaDataEmit::DefinePinvokeMap](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepinvokemap-method.md).</span><span class="sxs-lookup"><span data-stu-id="e9f40-103">Sets or changes features of a method's PInvoke signature, as defined by a prior call to [IMetaDataEmit::DefinePinvokeMap](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepinvokemap-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e9f40-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9f40-104">Syntax</span></span>  
  
```  
HRESULT SetPinvokeMap (   
    [in]  mdToken      tk,   
    [in]  DWORD        dwMappingFlags,  
    [in]  LPCWSTR      szImportName,   
    [in]  mdModuleRef  mrImportDLL   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e9f40-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9f40-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="e9f40-106">[in] Le `mdToken` pour que le mappage des informations s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="e9f40-106">[in] The `mdToken` to which mapping information applies.</span></span>  
  
 `dwMappingFlags`  
 <span data-ttu-id="e9f40-107">[in] Indicateurs utilisés par PInvoke pour effectuer le mappage.</span><span class="sxs-lookup"><span data-stu-id="e9f40-107">[in] Flags used by PInvoke to do the mapping.</span></span> <span data-ttu-id="e9f40-108">Il s’agit d’un masque de bits de `CorPinvokeMap` valeurs.</span><span class="sxs-lookup"><span data-stu-id="e9f40-108">This is a bitmask of `CorPinvokeMap` values.</span></span>  
  
 `szImportName`  
 <span data-ttu-id="e9f40-109">[in] Le nom de l’exportation de la cible de la DLL native.</span><span class="sxs-lookup"><span data-stu-id="e9f40-109">[in] The name of the target export in the native DLL.</span></span>  
  
 `mrImportDLL`  
 <span data-ttu-id="e9f40-110">[in] Le `mdModuleRef` jeton pour la cible de DLL non managée.</span><span class="sxs-lookup"><span data-stu-id="e9f40-110">[in] The `mdModuleRef` token for the target unmanaged DLL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e9f40-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9f40-111">Requirements</span></span>  
 <span data-ttu-id="e9f40-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e9f40-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e9f40-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e9f40-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e9f40-114">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e9f40-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e9f40-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e9f40-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e9f40-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9f40-116">See also</span></span>

- [<span data-ttu-id="e9f40-117">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="e9f40-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="e9f40-118">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="e9f40-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
