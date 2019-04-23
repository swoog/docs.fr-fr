---
title: IMetaDataImport::GetMethodProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetMethodProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMethodProps
helpviewer_keywords:
- GetMethodProps method [.NET Framework metadata]
- IMetaDataImport::GetMethodProps method [.NET Framework metadata]
ms.assetid: e0667ef7-1d31-4c89-a2d3-d426f023f8d2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c61931f5f6a4bbbf66446d68b0d1b2d1df958a66
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59137916"
---
# <a name="imetadataimportgetmethodprops-method"></a><span data-ttu-id="53023-102">IMetaDataImport::GetMethodProps, méthode</span><span class="sxs-lookup"><span data-stu-id="53023-102">IMetaDataImport::GetMethodProps Method</span></span>
<span data-ttu-id="53023-103">Obtient les métadonnées associées à la méthode référencée par le jeton MethodDef spécifié.</span><span class="sxs-lookup"><span data-stu-id="53023-103">Gets the metadata associated with the method referenced by the specified MethodDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53023-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53023-104">Syntax</span></span>  
  
```  
HRESULT GetMethodProps (  
    [in]  mdMethodDef         mb,  
    [out] mdTypeDef           *pClass,  
    [out] LPWSTR              szMethod,  
    [in]  ULONG               cchMethod,  
    [out] ULONG               *pchMethod,  
    [out] DWORD               *pdwAttr,  
    [out] PCCOR_SIGNATURE     *ppvSigBlob,  
    [out] ULONG               *pcbSigBlob,  
    [out] ULONG               *pulCodeRVA,  
    [out] DWORD               *pdwImplFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="53023-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53023-105">Parameters</span></span>  
 `mb`  
 <span data-ttu-id="53023-106">[in] Le jeton MethodDef qui représente la méthode pour retourner les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="53023-106">[in] The MethodDef token that represents the method to return metadata for.</span></span>  
  
 `pClass`  
 <span data-ttu-id="53023-107">[out] Pointeur vers un jeton TypeDef qui représente le type qui implémente la méthode.</span><span class="sxs-lookup"><span data-stu-id="53023-107">[out] A Pointer to a TypeDef token that represents the type that implements the method.</span></span>  
  
 `szMethod`  
 <span data-ttu-id="53023-108">[out] Pointeur vers une mémoire tampon qui a le nom de méthode.</span><span class="sxs-lookup"><span data-stu-id="53023-108">[out] A Pointer to a buffer that has the method's name.</span></span>  
  
 `cchMethod`  
 <span data-ttu-id="53023-109">[in] La taille demandée de `szMethod`.</span><span class="sxs-lookup"><span data-stu-id="53023-109">[in] The requested size of `szMethod`.</span></span>  
  
 `pchMethod`  
 <span data-ttu-id="53023-110">[out] Un pointeur vers la taille en caractères larges de `szMethod`, ou dans le cas de troncation, le nombre réel de caractères étendus dans le nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="53023-110">[out] A Pointer to the size in wide characters of `szMethod`, or in the case of truncation, the actual number of wide characters in the method name.</span></span>  
  
 `pdwAttr`  
 <span data-ttu-id="53023-111">[out] Pointeur vers les indicateurs associés à la méthode.</span><span class="sxs-lookup"><span data-stu-id="53023-111">[out] A pointer to any flags associated with the method.</span></span>  
  
 `ppvSigBlob`  
 <span data-ttu-id="53023-112">[out] Pointeur vers la signature de métadonnées binaires de la méthode.</span><span class="sxs-lookup"><span data-stu-id="53023-112">[out] A pointer to the binary metadata signature of the method.</span></span>  
  
 `pcbSigBlob`  
 <span data-ttu-id="53023-113">[out] Un pointeur vers la taille en octets de `ppvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="53023-113">[out] A Pointer to the size in bytes of `ppvSigBlob`.</span></span>  
  
 `pulCodeRVA`  
 <span data-ttu-id="53023-114">[out] Pointeur vers l’adresse virtuelle relative de la méthode.</span><span class="sxs-lookup"><span data-stu-id="53023-114">[out] A pointer to the relative virtual address of the method.</span></span>  
  
 `pdwImplFlags`  
 <span data-ttu-id="53023-115">[out] Pointeur vers les indicateurs d’implémentation de la méthode.</span><span class="sxs-lookup"><span data-stu-id="53023-115">[out] A pointer to any implementation flags for the method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="53023-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53023-116">Requirements</span></span>  
 <span data-ttu-id="53023-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="53023-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="53023-118">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="53023-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="53023-119">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="53023-119">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="53023-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="53023-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53023-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53023-121">See also</span></span>

- [<span data-ttu-id="53023-122">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="53023-122">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="53023-123">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="53023-123">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
