---
title: IMetaDataImport::GetMemberProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetMemberProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMemberProps
helpviewer_keywords:
- IMetaDataImport::GetMemberProps method [.NET Framework metadata]
- GetMemberProps method [.NET Framework metadata]
ms.assetid: 42790918-4142-4938-b8f4-a56979a55846
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d93763da2afbbdb1e738c802ba172e9f16e5f7af
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33448456"
---
# <a name="imetadataimportgetmemberprops-method"></a><span data-ttu-id="d2a1e-102">IMetaDataImport::GetMemberProps, méthode</span><span class="sxs-lookup"><span data-stu-id="d2a1e-102">IMetaDataImport::GetMemberProps Method</span></span>
<span data-ttu-id="d2a1e-103">Obtient les informations de métadonnées, y compris le nom, le signature binaire et l’adresse virtuelle relative, de la <xref:System.Type> membre référencé par le jeton de métadonnées spécifié.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-103">Gets metadata information, including the name, binary signature, and relative virtual address, of the <xref:System.Type> member referenced by the specified metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d2a1e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2a1e-104">Syntax</span></span>  
  
```  
HRESULT GetMemberProps (  
   [in]  mdToken           mb,   
   [out] mdTypeDef         *pClass,  
   [out] LPWSTR            szMember,   
   [in]  ULONG             cchMember,   
   [out] ULONG             *pchMember,   
   [out] DWORD             *pdwAttr,  
   [out] PCCOR_SIGNATURE   *ppvSigBlob,   
   [out] ULONG             *pcbSigBlob,   
   [out] ULONG             *pulCodeRVA,   
   [out] DWORD             *pdwImplFlags,   
   [out] DWORD             *pdwCPlusTypeFlag,   
   [out] UVCP_CONSTANT     *ppValue,  
   [out] ULONG             *pcchValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d2a1e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2a1e-105">Parameters</span></span>  
 `mb`  
 <span data-ttu-id="d2a1e-106">[in] Jeton qui référence le membre pour obtenir les métadonnées associées.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-106">[in] The token that references the member to get the associated metadata for.</span></span>  
  
 `pClass`  
 <span data-ttu-id="d2a1e-107">[out] Pointeur vers le jeton de métadonnées qui représente la classe du membre.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-107">[out] A pointer to the metadata token that represents the class of the member.</span></span>  
  
 `szMember`  
 <span data-ttu-id="d2a1e-108">[out] Le nom du membre.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-108">[out] The name of the member.</span></span>  
  
 `cchMember`  
 <span data-ttu-id="d2a1e-109">[in] La taille en caractères larges de la `szMember` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-109">[in] The size in wide characters of the `szMember` buffer.</span></span>  
  
 `pchMember`  
 <span data-ttu-id="d2a1e-110">[out] La taille en caractères étendus du nom retourné.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-110">[out] The size in wide characters of the returned name.</span></span>  
  
 `pdwAttr`  
 <span data-ttu-id="d2a1e-111">[out] Toutes les valeurs d’indicateur appliqués au membre.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-111">[out] Any flag values applied to the member.</span></span>  
  
 `ppvSigBlob`  
 <span data-ttu-id="d2a1e-112">[out] Pointeur vers la signature de métadonnées binaires du membre.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-112">[out] A pointer to the binary metadata signature of the member.</span></span>  
  
 `pcbSigBlob`  
 <span data-ttu-id="d2a1e-113">[out] La taille en octets de `ppvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-113">[out] The size in bytes of `ppvSigBlob`.</span></span>  
  
 `pulCodeRVA`  
 <span data-ttu-id="d2a1e-114">[out] Pointeur vers l’adresse virtuelle relative du membre.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-114">[out] A pointer to the relative virtual address of the member.</span></span>  
  
 `pdwImplFlags`  
 <span data-ttu-id="d2a1e-115">[out] Toutes les indicateurs d’implémentation de méthode associées au membre.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-115">[out] Any method implementation flags associated with the member.</span></span>  
  
 `pdwCPlusTypeFlag`  
 <span data-ttu-id="d2a1e-116">[out] Un indicateur qui marque un <xref:System.ValueType>.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-116">[out] A flag that marks a <xref:System.ValueType>.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="d2a1e-117">[out] Une valeur de chaîne constante retournée par ce membre.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-117">[out] A constant string value returned by this member.</span></span>  
  
 `pcchValue`  
 <span data-ttu-id="d2a1e-118">[out] La taille en caractères de `ppValue`, ou zéro si `ppValue` ne contient pas de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d2a1e-118">[out] The size in characters of `ppValue`, or zero if `ppValue` does not hold a string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d2a1e-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d2a1e-119">Requirements</span></span>  
 <span data-ttu-id="d2a1e-120">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d2a1e-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d2a1e-121">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="d2a1e-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d2a1e-122">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d2a1e-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d2a1e-123">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d2a1e-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2a1e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2a1e-124">See Also</span></span>  
 [<span data-ttu-id="d2a1e-125">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="d2a1e-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="d2a1e-126">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="d2a1e-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
