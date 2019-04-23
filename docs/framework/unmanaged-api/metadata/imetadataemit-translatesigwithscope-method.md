---
title: IMetaDataEmit::TranslateSigWithScope, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.TranslateSigWithScope
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::TranslateSigWithScope
helpviewer_keywords:
- TranslateSigWithScope method [.NET Framework metadata]
- IMetaDataEmit::TranslateSigWithScope method [.NET Framework metadata]
ms.assetid: 47915d33-b7bf-409e-b484-4ee1df15de22
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 71029d6ebfb3248da791d4371dfe3e39589af443
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59207641"
---
# <a name="imetadataemittranslatesigwithscope-method"></a><span data-ttu-id="70834-102">IMetaDataEmit::TranslateSigWithScope, méthode</span><span class="sxs-lookup"><span data-stu-id="70834-102">IMetaDataEmit::TranslateSigWithScope Method</span></span>
<span data-ttu-id="70834-103">Importe un assembly dans la portée actuelle et obtient une nouvelle signature de métadonnées pour la portée fusionnée.</span><span class="sxs-lookup"><span data-stu-id="70834-103">Imports an assembly into the current scope and gets a new metadata signature for the merged scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70834-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70834-104">Syntax</span></span>  
  
```  
HRESULT TranslateSigWithScope (   
    [in]  IMetaDataAssemblyImport   *pAssemImport,   
    [in]  const void                *pbHashValue,   
    [in]  ULONG                     cbHashValue,   
    [in]  IMetaDataImport           *import,   
    [in]  PCCOR_SIGNATURE           pbSigBlob,   
    [in]  ULONG                     cbSigBlob,  
    [in]  IMetaDataAssemblyEmit     *pAssemEmit,   
    [in]  IMetaDataEmit             *emit,   
    [out] PCOR_SIGNATURE            pvTranslatedSig,   
    [in]  ULONG                     cbTranslatedSigMax,   
    [out] ULONG                     *pcbTranslatedSig   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="70834-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70834-105">Parameters</span></span>  
 `pAssemImport`  
 <span data-ttu-id="70834-106">[in] L’interface pour importer l’assembly (où la signature est définie).</span><span class="sxs-lookup"><span data-stu-id="70834-106">[in] The interface for import assembly (where the signature is defined).</span></span>  
  
 `pbHashValue`  
 <span data-ttu-id="70834-107">[in] L’objet blob de hachage pour l’assembly.</span><span class="sxs-lookup"><span data-stu-id="70834-107">[in] The hash blob for the assembly.</span></span>  
  
 `cbHashValue`  
 <span data-ttu-id="70834-108">[in] Le nombre d’octets dans `pbHashValue`.</span><span class="sxs-lookup"><span data-stu-id="70834-108">[in] The count of bytes in `pbHashValue`.</span></span>  
  
 `import`  
 <span data-ttu-id="70834-109">[in] L’interface pour la portée d’importation de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="70834-109">[in] The interface for import metadata scope.</span></span>  
  
 `pbSigBlob`  
 <span data-ttu-id="70834-110">[in] La signature doivent être importées.</span><span class="sxs-lookup"><span data-stu-id="70834-110">[in] The signature to be imported.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="70834-111">[in] La taille, en octets, de `pbSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="70834-111">[in] The size, in bytes, of `pbSigBlob`.</span></span>  
  
 `pAssemEmit`  
 <span data-ttu-id="70834-112">[in] L’interface pour exporter l’assembly.</span><span class="sxs-lookup"><span data-stu-id="70834-112">[in] The interface for export assembly.</span></span>  
  
 `emit`  
 <span data-ttu-id="70834-113">[in] L’interface pour la portée de métadonnées d’exportation.</span><span class="sxs-lookup"><span data-stu-id="70834-113">[in] The interface for export metadata scope.</span></span>  
  
 `pvTranslatedSig`  
 <span data-ttu-id="70834-114">[out] La mémoire tampon pour stocker l’objet blob de signature traduite.</span><span class="sxs-lookup"><span data-stu-id="70834-114">[out] The buffer to hold the translated signature blob.</span></span>  
  
 `cbTranslatedSigMax`  
 <span data-ttu-id="70834-115">[in] La capacité, en octets, de `pvTranslatedSig`.</span><span class="sxs-lookup"><span data-stu-id="70834-115">[in] The capacity, in bytes, of `pvTranslatedSig`.</span></span>  
  
 `pcbTranslatedSig`  
 <span data-ttu-id="70834-116">[out] Le nombre d’octets réels dans la signature traduite.</span><span class="sxs-lookup"><span data-stu-id="70834-116">[out] The number of actual bytes in the translated signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="70834-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70834-117">Requirements</span></span>  
 <span data-ttu-id="70834-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="70834-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="70834-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="70834-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="70834-120">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="70834-120">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="70834-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="70834-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70834-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70834-122">See also</span></span>

- [<span data-ttu-id="70834-123">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="70834-123">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
- [<span data-ttu-id="70834-124">IMetaDataAssemblyImport, interface</span><span class="sxs-lookup"><span data-stu-id="70834-124">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
- [<span data-ttu-id="70834-125">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="70834-125">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="70834-126">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="70834-126">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
- [<span data-ttu-id="70834-127">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="70834-127">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
