---
title: IMetaDataImport::GetMemberRefProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetMemberRefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMemberRefProps
helpviewer_keywords:
- GetMemberRefProps method [.NET Framework metadata]
- IMetaDataImport::GetMemberRefProps method [.NET Framework metadata]
ms.assetid: 0ea73055-ece0-4151-a094-414c88ef8941
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0d62b9be1bef16014e2870c15a232bb46d4daf10
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33448746"
---
# <a name="imetadataimportgetmemberrefprops-method"></a><span data-ttu-id="d70f1-102">IMetaDataImport::GetMemberRefProps, méthode</span><span class="sxs-lookup"><span data-stu-id="d70f1-102">IMetaDataImport::GetMemberRefProps Method</span></span>
<span data-ttu-id="d70f1-103">Obtient les métadonnées associées au membre référencé par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="d70f1-103">Gets metadata associated with the member referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d70f1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d70f1-104">Syntax</span></span>  
  
```  
HRESULT GetMemberRefProps (  
   [in]  mdMemberRef       mr,   
   [out] mdToken           *ptk,   
   [out] LPWSTR            szMember,   
   [in]  ULONG             cchMember,   
   [out] ULONG             *pchMember,   
   [out] PCCOR_SIGNATURE   *ppvSigBlob,   
   [out] ULONG             *pbSig   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d70f1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d70f1-105">Parameters</span></span>  
 `mr`  
 <span data-ttu-id="d70f1-106">[in] Jeton MemberRef pour retourner les métadonnées associées.</span><span class="sxs-lookup"><span data-stu-id="d70f1-106">[in] The MemberRef token to return associated metadata for.</span></span>  
  
 `ptk`  
 <span data-ttu-id="d70f1-107">[out] Un jeton TypeDef ou TypeRef ou TypeSpec qui représente la classe qui déclare le membre, ou un jeton ModuleRef qui représente la classe de module qui déclare le membre, ou MethodDef qui représente le membre.</span><span class="sxs-lookup"><span data-stu-id="d70f1-107">[out] A TypeDef or TypeRef, or TypeSpec token that represents the class that declares the member, or a ModuleRef token that represents the module class that declares the member, or a MethodDef that represents the member.</span></span>  
  
 `szMember`  
 <span data-ttu-id="d70f1-108">[out] Un tampon pour chaîne pour le nom du membre.</span><span class="sxs-lookup"><span data-stu-id="d70f1-108">[out] A string buffer for the member's name.</span></span>  
  
 `cchMember`  
 <span data-ttu-id="d70f1-109">[in] La taille demandée en caractères larges de `szMember`.</span><span class="sxs-lookup"><span data-stu-id="d70f1-109">[in] The requested size in wide characters of `szMember`.</span></span>  
  
 `pchMember`  
 <span data-ttu-id="d70f1-110">[out] La taille retournée en caractères larges de `szMember`.</span><span class="sxs-lookup"><span data-stu-id="d70f1-110">[out] The returned size in wide characters of `szMember`.</span></span>  
  
 `ppvSibBlob`  
 <span data-ttu-id="d70f1-111">[out] Pointeur vers la signature de métadonnées binaires pour le membre.</span><span class="sxs-lookup"><span data-stu-id="d70f1-111">[out] A pointer to the binary metadata signature for the member.</span></span>  
  
 `pbSig`  
 <span data-ttu-id="d70f1-112">[out] La taille en octets de `ppvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="d70f1-112">[out] The size in bytes of `ppvSigBlob`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d70f1-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d70f1-113">Requirements</span></span>  
 <span data-ttu-id="d70f1-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d70f1-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d70f1-115">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="d70f1-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d70f1-116">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d70f1-116">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d70f1-117">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d70f1-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d70f1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d70f1-118">See Also</span></span>  
 [<span data-ttu-id="d70f1-119">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="d70f1-119">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="d70f1-120">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="d70f1-120">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
