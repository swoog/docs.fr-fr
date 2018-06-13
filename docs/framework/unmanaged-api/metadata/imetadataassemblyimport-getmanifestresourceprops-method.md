---
title: IMetaDataAssemblyImport::GetManifestResourceProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetManifestResourceProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetManifestResourceProps
helpviewer_keywords:
- GetManifestResourceProps method [.NET Framework metadata]
- IMetaDataAssemblyImport::GetManifestResourceProps method [.NET Framework metadata]
ms.assetid: 00be4789-ac63-4397-b2ec-1629a5c5a585
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 07237794ca45b16b1ae1ca95b1d62889f095350f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33448157"
---
# <a name="imetadataassemblyimportgetmanifestresourceprops-method"></a><span data-ttu-id="b1ceb-102">IMetaDataAssemblyImport::GetManifestResourceProps, méthode</span><span class="sxs-lookup"><span data-stu-id="b1ceb-102">IMetaDataAssemblyImport::GetManifestResourceProps Method</span></span>
<span data-ttu-id="b1ceb-103">Obtient le jeu de propriétés de la ressource de manifeste avec la signature de métadonnées spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b1ceb-103">Gets the set of properties of the manifest resource with the specified metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1ceb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1ceb-104">Syntax</span></span>  
  
```  
HRESULT GetManifestResourceProps (  
    [in]  mdManifestResource   mdmr,   
    [out] LPWSTR               szName,   
    [in]  ULONG                cchName,   
    [out] ULONG                *pchName,   
    [out] mdToken              *ptkImplementation,   
    [out] DWORD                *pdwOffset,   
    [out] DWORD                *pdwResourceFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b1ceb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1ceb-105">Parameters</span></span>  
 `mdmr`  
 <span data-ttu-id="b1ceb-106">[in] Un `mdManifestResource` jeton qui représente la ressource pour laquelle obtenir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="b1ceb-106">[in] An `mdManifestResource` token that represents the resource for which to get the properties.</span></span>  
  
 `szName`  
 <span data-ttu-id="b1ceb-107">[out] Le nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="b1ceb-107">[out] The name of the resource.</span></span>  
  
 `cchName`  
 <span data-ttu-id="b1ceb-108">[in] La taille, en caractères étendus de `szName`.</span><span class="sxs-lookup"><span data-stu-id="b1ceb-108">[in] The size, in wide chars, of `szName`.</span></span>  
  
 `pchName`  
 <span data-ttu-id="b1ceb-109">[out] Un pointeur vers le nombre de caractères étendus réellement retournés dans `szName`.</span><span class="sxs-lookup"><span data-stu-id="b1ceb-109">[out] A pointer to the number of wide chars actually returned in `szName`.</span></span>  
  
 `ptkImplementation`  
 <span data-ttu-id="b1ceb-110">[out] Un pointeur vers un `mdFile` jeton ou un `mdAssemblyRef` jeton qui représente le fichier ou l’assembly, qui contient la ressource.</span><span class="sxs-lookup"><span data-stu-id="b1ceb-110">[out] A pointer to an `mdFile` token or an `mdAssemblyRef` token that represents the file or assembly, respectively, that contains the resource.</span></span>  
  
 `pdwOffset`  
 <span data-ttu-id="b1ceb-111">[out] Pointeur vers une valeur qui spécifie l’offset de début de la ressource dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="b1ceb-111">[out] A pointer to a value that specifies the offset to the beginning of the resource within the file.</span></span>  
  
 `pdwResourceFlags`  
 <span data-ttu-id="b1ceb-112">[out] Pointeur vers les indicateurs qui décrivent les métadonnées appliquées à une ressource.</span><span class="sxs-lookup"><span data-stu-id="b1ceb-112">[out] A pointer to flags that describe the metadata applied to a resource.</span></span> <span data-ttu-id="b1ceb-113">La valeur des indicateurs est une combinaison d’une ou plusieurs [CorManifestResourceFlags](../../../../docs/framework/unmanaged-api/metadata/cormanifestresourceflags-enumeration.md) valeurs.</span><span class="sxs-lookup"><span data-stu-id="b1ceb-113">The flags value is a combination of one or more [CorManifestResourceFlags](../../../../docs/framework/unmanaged-api/metadata/cormanifestresourceflags-enumeration.md) values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b1ceb-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b1ceb-114">Requirements</span></span>  
 <span data-ttu-id="b1ceb-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b1ceb-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1ceb-116">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b1ceb-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b1ceb-117">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b1ceb-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b1ceb-118">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b1ceb-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1ceb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1ceb-119">See Also</span></span>  
 [<span data-ttu-id="b1ceb-120">IMetaDataAssemblyImport, interface</span><span class="sxs-lookup"><span data-stu-id="b1ceb-120">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
