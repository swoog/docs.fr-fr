---
title: IMetaDataImport::EnumFieldsWithName, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumFieldsWithName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumFieldsWithName
helpviewer_keywords:
- IMetaDataImport::EnumFieldsWithName method [.NET Framework metadata]
- EnumFieldsWithName method [.NET Framework metadata]
ms.assetid: 42145e8d-000f-4d0b-ae43-c08201190fa2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6ed8bbbd9699fe707d638bb8d07064e508b6f2fb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447770"
---
# <a name="imetadataimportenumfieldswithname-method"></a><span data-ttu-id="82c80-102">IMetaDataImport::EnumFieldsWithName, méthode</span><span class="sxs-lookup"><span data-stu-id="82c80-102">IMetaDataImport::EnumFieldsWithName Method</span></span>
<span data-ttu-id="82c80-103">Énumère les jetons FieldDef du type spécifié avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="82c80-103">Enumerates FieldDef tokens of the specified type with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82c80-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82c80-104">Syntax</span></span>  
  
```  
HRESULT EnumFieldsWithName (  
   [in, out] HCORENUM    *phEnum,   
   [in]  mdTypeDef       cl,   
   [in]  LPCWSTR         szName,   
   [out] mdFieldDef      rFields[],   
   [in]  ULONG           cMax,   
   [out] ULONG           *pcTokens   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="82c80-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82c80-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="82c80-106">[dans, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="82c80-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `cl`  
 <span data-ttu-id="82c80-107">[in] Le jeton du type dont les champs doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="82c80-107">[in] The token of the type whose fields are to be enumerated.</span></span>  
  
 `szName`  
 <span data-ttu-id="82c80-108">[in] Le nom du champ qui limite la portée de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="82c80-108">[in] The field name that limits the scope of the enumeration.</span></span>  
  
 `rFields`  
 <span data-ttu-id="82c80-109">[out] Tableau utilisé pour stocker les jetons FieldDef.</span><span class="sxs-lookup"><span data-stu-id="82c80-109">[out] Array used to store the FieldDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="82c80-110">[in] Taille maximale du tableau `rFields`.</span><span class="sxs-lookup"><span data-stu-id="82c80-110">[in] The maximum size of the `rFields` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="82c80-111">[out] Le nombre réel de jetons FieldDef retournés dans `rFields`.</span><span class="sxs-lookup"><span data-stu-id="82c80-111">[out] The actual number of FieldDef tokens returned in `rFields`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="82c80-112">Notes</span><span class="sxs-lookup"><span data-stu-id="82c80-112">Remarks</span></span>  
 <span data-ttu-id="82c80-113">Contrairement aux [IMetaDataImport::EnumFields](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enumfields-method.md), `EnumFieldsWithName` ignore tous les jetons de champ qui n’ont pas le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="82c80-113">Unlike [IMetaDataImport::EnumFields](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enumfields-method.md), `EnumFieldsWithName` discards all field tokens that do not have the specified name.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="82c80-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="82c80-114">Return Value</span></span>  
  
|<span data-ttu-id="82c80-115">HRESULT</span><span class="sxs-lookup"><span data-stu-id="82c80-115">HRESULT</span></span>|<span data-ttu-id="82c80-116">Description</span><span class="sxs-lookup"><span data-stu-id="82c80-116">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="82c80-117">`EnumFieldsWithName` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="82c80-117">`EnumFieldsWithName` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="82c80-118">Il n’existe pas de champs à énumérer.</span><span class="sxs-lookup"><span data-stu-id="82c80-118">There are no fields to enumerate.</span></span> <span data-ttu-id="82c80-119">Dans ce cas, `pcTokens` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="82c80-119">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="82c80-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="82c80-120">Requirements</span></span>  
 <span data-ttu-id="82c80-121">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="82c80-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="82c80-122">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="82c80-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="82c80-123">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="82c80-123">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="82c80-124">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="82c80-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="82c80-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82c80-125">See Also</span></span>  
 [<span data-ttu-id="82c80-126">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="82c80-126">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="82c80-127">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="82c80-127">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
