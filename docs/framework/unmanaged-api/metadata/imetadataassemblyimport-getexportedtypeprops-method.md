---
title: IMetaDataAssemblyImport::GetExportedTypeProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetExportedTypeProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetExportedTypeProps
helpviewer_keywords:
- GetExportedTypeProps method [.NET Framework metadata]
- IMetaDataAssemblyImport::GetExportedTypeProps method [.NET Framework metadata]
ms.assetid: 25ca7623-5a55-4f09-b44a-36b03d142278
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c76e46c75680d9fc0ad70e94da288f0c6b5e5ee1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33446318"
---
# <a name="imetadataassemblyimportgetexportedtypeprops-method"></a><span data-ttu-id="86ef5-102">IMetaDataAssemblyImport::GetExportedTypeProps, méthode</span><span class="sxs-lookup"><span data-stu-id="86ef5-102">IMetaDataAssemblyImport::GetExportedTypeProps Method</span></span>
<span data-ttu-id="86ef5-103">Obtient le jeu de propriétés du type exporté avec la signature de métadonnées spécifiée.</span><span class="sxs-lookup"><span data-stu-id="86ef5-103">Gets the set of properties of the exported type with the specified metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86ef5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86ef5-104">Syntax</span></span>  
  
```  
HRESULT GetExportedTypeProps (  
    [in]  mdExportedType    mdct,   
    [out] LPWSTR            szName,   
    [in]  ULONG             cchName,   
    [out] ULONG             *pchName,   
    [out] mdToken           *ptkImplementation,   
    [out] mdTypeDef         *ptkTypeDef,   
    [out] DWORD             *pdwExportedTypeFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="86ef5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86ef5-105">Parameters</span></span>  
 `mdct`  
 <span data-ttu-id="86ef5-106">[in] Un `mdExportedType` jeton de métadonnées qui représente le type exporté.</span><span class="sxs-lookup"><span data-stu-id="86ef5-106">[in] An `mdExportedType` metadata token that represents the exported type.</span></span>  
  
 `szName`  
 <span data-ttu-id="86ef5-107">[out] Le nom du type exporté.</span><span class="sxs-lookup"><span data-stu-id="86ef5-107">[out] The name of the exported type.</span></span>  
  
 `cchName`  
 <span data-ttu-id="86ef5-108">[in] La taille, en caractères larges, de `szName`.</span><span class="sxs-lookup"><span data-stu-id="86ef5-108">[in] The size, in wide characters, of `szName`.</span></span>  
  
 `pchName`  
 <span data-ttu-id="86ef5-109">[out] Le nombre de caractères étendus réellement retournés dans `szName`</span><span class="sxs-lookup"><span data-stu-id="86ef5-109">[out] The number of wide characters actually returned in `szName`</span></span>  
  
 `ptkImplementation`  
 <span data-ttu-id="86ef5-110">[out] Un `mdFile`, `mdAssemblyRef`, ou `mdExportedType` jeton de métadonnées qui contienne ou autorise l’accès aux propriétés du type exporté.</span><span class="sxs-lookup"><span data-stu-id="86ef5-110">[out] An `mdFile`, `mdAssemblyRef`, or `mdExportedType` metadata token that contains or allows access to the properties of the exported type.</span></span>  
  
 `ptkTypeDef`  
 <span data-ttu-id="86ef5-111">[out] Un pointeur vers un `mdTypeDef` jeton qui représente un type dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="86ef5-111">[out] A pointer to an `mdTypeDef` token that represents a type in the file.</span></span>  
  
 `pdwExportedTypeFlags`  
 <span data-ttu-id="86ef5-112">[out] Pointeur vers les indicateurs qui décrivent les métadonnées appliquées au type exporté.</span><span class="sxs-lookup"><span data-stu-id="86ef5-112">[out] A pointer to the flags that describe the metadata applied to the exported type.</span></span> <span data-ttu-id="86ef5-113">La valeur des indicateurs peut être une ou plusieurs [CorTypeAttr](../../../../docs/framework/unmanaged-api/metadata/cortypeattr-enumeration.md) valeurs.</span><span class="sxs-lookup"><span data-stu-id="86ef5-113">The flags value can be one or more [CorTypeAttr](../../../../docs/framework/unmanaged-api/metadata/cortypeattr-enumeration.md) values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86ef5-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="86ef5-114">Requirements</span></span>  
 <span data-ttu-id="86ef5-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="86ef5-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86ef5-116">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="86ef5-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="86ef5-117">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="86ef5-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="86ef5-118">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="86ef5-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86ef5-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86ef5-119">See Also</span></span>  
 [<span data-ttu-id="86ef5-120">IMetaDataAssemblyImport, interface</span><span class="sxs-lookup"><span data-stu-id="86ef5-120">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
