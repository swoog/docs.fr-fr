---
title: IMetaDataImport::EnumTypeRefs, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumTypeRefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumTypeRefs
helpviewer_keywords:
- EnumTypeRefs method [.NET Framework metadata]
- IMetaDataImport::EnumTypeRefs method [.NET Framework metadata]
ms.assetid: b4896b8f-8e97-469c-8089-e72a025661b5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: de0fe4a51fbb49e80377b6b434bf3b72ddb90f02
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59081618"
---
# <a name="imetadataimportenumtyperefs-method"></a><span data-ttu-id="cc8fa-102">IMetaDataImport::EnumTypeRefs, méthode</span><span class="sxs-lookup"><span data-stu-id="cc8fa-102">IMetaDataImport::EnumTypeRefs Method</span></span>
<span data-ttu-id="cc8fa-103">Énumère les jetons TypeRef définis dans la portée des métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="cc8fa-103">Enumerates TypeRef tokens defined in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc8fa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc8fa-104">Syntax</span></span>  
  
```  
HRESULT EnumTypeRefs (  
   [in, out] HCORENUM    *phEnum,   
   [out] mdTypeRef       rTypeRefs[],  
   [in]  ULONG           cMax,   
   [out] ULONG           *pcTypeRefs  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cc8fa-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc8fa-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="cc8fa-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="cc8fa-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="cc8fa-107">Cela doit être NULL pour le premier appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="cc8fa-107">This must be NULL for the first call of this method.</span></span>  
  
 `rTypeRefs`  
 <span data-ttu-id="cc8fa-108">[out] Tableau utilisé pour stocker les jetons TypeRef.</span><span class="sxs-lookup"><span data-stu-id="cc8fa-108">[out] The array used to store the TypeRef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="cc8fa-109">[in] Taille maximale du tableau `rTypeRefs`.</span><span class="sxs-lookup"><span data-stu-id="cc8fa-109">[in] The maximum size of the `rTypeRefs` array.</span></span>  
  
 `pcTypeRefs`  
 <span data-ttu-id="cc8fa-110">[out] Un pointeur vers le nombre de jetons TypeRef retournés dans `rTypeRefs`.</span><span class="sxs-lookup"><span data-stu-id="cc8fa-110">[out] A pointer to the number of TypeRef tokens returned in `rTypeRefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cc8fa-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cc8fa-111">Return Value</span></span>  
  
|<span data-ttu-id="cc8fa-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="cc8fa-112">HRESULT</span></span>|<span data-ttu-id="cc8fa-113">Description</span><span class="sxs-lookup"><span data-stu-id="cc8fa-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|`EnumTypeRefs` <span data-ttu-id="cc8fa-114">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="cc8fa-114">returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="cc8fa-115">Il n’existe pas de jetons à énumérer.</span><span class="sxs-lookup"><span data-stu-id="cc8fa-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="cc8fa-116">Dans ce cas, `pcTypeRefs` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cc8fa-116">In that case, `pcTypeRefs` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cc8fa-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cc8fa-117">Remarks</span></span>  
 <span data-ttu-id="cc8fa-118">Un jeton TypeRef représente une référence à un type.</span><span class="sxs-lookup"><span data-stu-id="cc8fa-118">A TypeRef token represents a reference to a type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc8fa-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc8fa-119">Requirements</span></span>  
 <span data-ttu-id="cc8fa-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cc8fa-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc8fa-121">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="cc8fa-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="cc8fa-122">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cc8fa-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="cc8fa-123">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="cc8fa-123">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="cc8fa-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc8fa-124">See also</span></span>

- [<span data-ttu-id="cc8fa-125">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="cc8fa-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="cc8fa-126">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="cc8fa-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
