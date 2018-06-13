---
title: IMetaDataAssemblyEmit::SetManifestResourceProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.SetManifestResourceProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::SetManifestResourceProps
helpviewer_keywords:
- SetManifestResourceProps method [.NET Framework metadata]
- IMetaDataAssemblyEmit::SetManifestResourceProps method [.NET Framework metadata]
ms.assetid: ef77efd1-849c-4e51-ba92-7ee3d2bf0339
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 755c64aa00b82bf2d8213217787f4dc1916c0898
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443298"
---
# <a name="imetadataassemblyemitsetmanifestresourceprops-method"></a><span data-ttu-id="0136d-102">IMetaDataAssemblyEmit::SetManifestResourceProps, méthode</span><span class="sxs-lookup"><span data-stu-id="0136d-102">IMetaDataAssemblyEmit::SetManifestResourceProps Method</span></span>
<span data-ttu-id="0136d-103">Modifie la structure de métadonnées `ManifestResource` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0136d-103">Modifies the specified `ManifestResource` metadata structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0136d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0136d-104">Syntax</span></span>  
  
```  
HRESULT SetManifestResourceProps (  
    [in] mdManifestResource  mr,  
    [in] mdToken             tkImplementation,   
    [in] DWORD               dwOffset,  
    [in] DWORD               dwResourceFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0136d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0136d-105">Parameters</span></span>  
 `mr`  
 <span data-ttu-id="0136d-106">[in] Jeton qui spécifie la `ManifestResource` structure de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="0136d-106">[in] The token that specifies the `ManifestResource` metadata structure to be modified.</span></span>  
  
 `tkImplementation`  
 <span data-ttu-id="0136d-107">[in] Le jeton, de type `File` ou `AssemblyRef`, qui mappe au fournisseur de ressources.</span><span class="sxs-lookup"><span data-stu-id="0136d-107">[in] The token, of type `File` or `AssemblyRef`, that maps to the resource provider.</span></span>  
  
 `dwOffset`  
 <span data-ttu-id="0136d-108">[in] Offset au début de la ressource dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="0136d-108">[in] The offset to the beginning of the resource within the file.</span></span>  
  
 `dwResourceFlags`  
 <span data-ttu-id="0136d-109">[in] Combinaison de bits des valeurs d’indicateurs qui spécifient les attributs de la ressource.</span><span class="sxs-lookup"><span data-stu-id="0136d-109">[in] A bitwise combination of flag values that specify the attributes of the resource.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0136d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0136d-110">Remarks</span></span>  
 <span data-ttu-id="0136d-111">Pour créer un `ManifestResource` structure des métadonnées, utilisez le [IMetaDataAssemblyEmit::DefineManifestResource](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definemanifestresource-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="0136d-111">To create a `ManifestResource` metadata structure, use the [IMetaDataAssemblyEmit::DefineManifestResource](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definemanifestresource-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0136d-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0136d-112">Requirements</span></span>  
 <span data-ttu-id="0136d-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0136d-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0136d-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="0136d-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0136d-115">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0136d-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="0136d-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0136d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0136d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0136d-117">See Also</span></span>  
 [<span data-ttu-id="0136d-118">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="0136d-118">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
