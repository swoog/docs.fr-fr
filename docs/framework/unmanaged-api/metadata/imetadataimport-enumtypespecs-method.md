---
title: IMetaDataImport::EnumTypeSpecs, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumTypeSpecs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumTypeSpecs
helpviewer_keywords:
- EnumTypeSpecs method [.NET Framework metadata]
- IMetaDataImport::EnumTypeSpecs method [.NET Framework metadata]
ms.assetid: 75331c7b-988b-436c-9eb9-a270d37b4f06
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 01151dc2fe6aa995285a34076527609816b2f3e8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59205158"
---
# <a name="imetadataimportenumtypespecs-method"></a><span data-ttu-id="a382c-102">IMetaDataImport::EnumTypeSpecs, méthode</span><span class="sxs-lookup"><span data-stu-id="a382c-102">IMetaDataImport::EnumTypeSpecs Method</span></span>
<span data-ttu-id="a382c-103">Énumère les jetons TypeSpec définis dans la portée des métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="a382c-103">Enumerates TypeSpec tokens defined in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a382c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a382c-104">Syntax</span></span>  
  
```  
HRESULT EnumTypeSpecs (  
   [in, out] HCORENUM    *phEnum,  
   [out] mdTypeSpec      rTypeSpecs[],  
   [in]  ULONG           cMax,  
   [out] ULONG           *pcTypeSpecs  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a382c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a382c-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="a382c-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="a382c-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="a382c-107">Cette valeur doit être NULL pour le premier appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a382c-107">This value must be NULL for the first call of this method.</span></span>  
  
 `rTypeSpecs`  
 <span data-ttu-id="a382c-108">[out] Tableau utilisé pour stocker les jetons TypeSpec.</span><span class="sxs-lookup"><span data-stu-id="a382c-108">[out] The array used to store the TypeSpec tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="a382c-109">[in] Taille maximale du tableau `rTypeSpecs`.</span><span class="sxs-lookup"><span data-stu-id="a382c-109">[in] The maximum size of the `rTypeSpecs` array.</span></span>  
  
 `pcTypeSpecs`  
 <span data-ttu-id="a382c-110">[out] Le nombre de jetons TypeSpec retournés dans `rTypeSpecs`.</span><span class="sxs-lookup"><span data-stu-id="a382c-110">[out] The number of TypeSpec tokens returned in `rTypeSpecs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a382c-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a382c-111">Return Value</span></span>  
  
|<span data-ttu-id="a382c-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a382c-112">HRESULT</span></span>|<span data-ttu-id="a382c-113">Description</span><span class="sxs-lookup"><span data-stu-id="a382c-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|`EnumTypeSpecs` <span data-ttu-id="a382c-114">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="a382c-114">returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="a382c-115">Il n’existe pas de jetons à énumérer.</span><span class="sxs-lookup"><span data-stu-id="a382c-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="a382c-116">Dans ce cas, `pcTypeSpecs` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a382c-116">In that case, `pcTypeSpecs` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a382c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a382c-117">Remarks</span></span>  
 <span data-ttu-id="a382c-118">Les jetons TypeSpec sont créés par le [IMetaDataEmit::GetTokenFromTypeSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromtypespec-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="a382c-118">The TypeSpec tokens are created by the [IMetaDataEmit::GetTokenFromTypeSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromtypespec-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a382c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a382c-119">Requirements</span></span>  
 <span data-ttu-id="a382c-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a382c-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a382c-121">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a382c-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a382c-122">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a382c-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="a382c-123">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="a382c-123">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a382c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a382c-124">See also</span></span>

- [<span data-ttu-id="a382c-125">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="a382c-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="a382c-126">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="a382c-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
