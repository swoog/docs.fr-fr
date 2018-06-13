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
ms.openlocfilehash: 84b2c0571a7991829e65b45759bd61fa4009aa71
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445875"
---
# <a name="imetadataemitsetpinvokemap-method"></a><span data-ttu-id="9055d-102">IMetaDataEmit::SetPinvokeMap, méthode</span><span class="sxs-lookup"><span data-stu-id="9055d-102">IMetaDataEmit::SetPinvokeMap Method</span></span>
<span data-ttu-id="9055d-103">Définit ou modifie les fonctionnalités de la signature PInvoke d’une méthode définie par un appel antérieur à [IMetaDataEmit::DefinePinvokeMap](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepinvokemap-method.md).</span><span class="sxs-lookup"><span data-stu-id="9055d-103">Sets or changes features of a method's PInvoke signature, as defined by a prior call to [IMetaDataEmit::DefinePinvokeMap](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepinvokemap-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9055d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9055d-104">Syntax</span></span>  
  
```  
HRESULT SetPinvokeMap (   
    [in]  mdToken      tk,   
    [in]  DWORD        dwMappingFlags,  
    [in]  LPCWSTR      szImportName,   
    [in]  mdModuleRef  mrImportDLL   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9055d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9055d-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="9055d-106">[in] Le `mdToken` que le mappage s’applique plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9055d-106">[in] The `mdToken` to which mapping information applies.</span></span>  
  
 `dwMappingFlags`  
 <span data-ttu-id="9055d-107">[in] Indicateurs utilisés par PInvoke pour effectuer le mappage.</span><span class="sxs-lookup"><span data-stu-id="9055d-107">[in] Flags used by PInvoke to do the mapping.</span></span> <span data-ttu-id="9055d-108">Il s’agit d’un masque de bits de `CorPinvokeMap` valeurs.</span><span class="sxs-lookup"><span data-stu-id="9055d-108">This is a bitmask of `CorPinvokeMap` values.</span></span>  
  
 `szImportName`  
 <span data-ttu-id="9055d-109">[in] Le nom de l’exportation de la cible de la DLL native.</span><span class="sxs-lookup"><span data-stu-id="9055d-109">[in] The name of the target export in the native DLL.</span></span>  
  
 `mrImportDLL`  
 <span data-ttu-id="9055d-110">[in] Le `mdModuleRef` jeton pour la cible de DLL non managée.</span><span class="sxs-lookup"><span data-stu-id="9055d-110">[in] The `mdModuleRef` token for the target unmanaged DLL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9055d-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9055d-111">Requirements</span></span>  
 <span data-ttu-id="9055d-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9055d-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9055d-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="9055d-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9055d-114">**Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9055d-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9055d-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9055d-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9055d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9055d-116">See Also</span></span>  
 [<span data-ttu-id="9055d-117">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="9055d-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="9055d-118">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="9055d-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
