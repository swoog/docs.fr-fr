---
title: IMetaDataImport::EnumFields, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumFields
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumFields
helpviewer_keywords:
- EnumFields method [.NET Framework metadata]
- IMetaDataImport::EnumFields method [.NET Framework metadata]
ms.assetid: 1d23247e-c58c-45db-afd8-83aa89cde18e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 18cf59553468e2408f3898d8233bd05d453db17b
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471964"
---
# <a name="imetadataimportenumfields-method"></a><span data-ttu-id="253ce-102">IMetaDataImport::EnumFields, méthode</span><span class="sxs-lookup"><span data-stu-id="253ce-102">IMetaDataImport::EnumFields Method</span></span>
<span data-ttu-id="253ce-103">Énumère les jetons FieldDef pour le type référencé par le jeton TypeDef spécifié.</span><span class="sxs-lookup"><span data-stu-id="253ce-103">Enumerates FieldDef tokens for the type referenced by the specified TypeDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="253ce-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="253ce-104">Syntax</span></span>  
  
```  
HRESULT EnumFields (   
   [in, out] HCORENUM    *phEnum,   
   [in]      mdTypeDef   cl,   
   [out]     mdFieldDef  rFields[],   
   [in]      ULONG       cMax,   
   [out]     ULONG       *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="253ce-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="253ce-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="253ce-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="253ce-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `cl`  
 <span data-ttu-id="253ce-107">[in] Le jeton TypeDef de la classe dont les champs doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="253ce-107">[in] The TypeDef token of the class whose fields are to be enumerated.</span></span>  
  
 `rFields`  
 <span data-ttu-id="253ce-108">[out] La liste des jetons FieldDef.</span><span class="sxs-lookup"><span data-stu-id="253ce-108">[out] The list of FieldDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="253ce-109">[in] Taille maximale du tableau `rFields`.</span><span class="sxs-lookup"><span data-stu-id="253ce-109">[in] The maximum size of the `rFields` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="253ce-110">[out] Le nombre réel de jetons FieldDef retournés dans `rFields`.</span><span class="sxs-lookup"><span data-stu-id="253ce-110">[out] The actual number of FieldDef tokens returned in `rFields`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="253ce-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="253ce-111">Return Value</span></span>  
  
|<span data-ttu-id="253ce-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="253ce-112">HRESULT</span></span>|<span data-ttu-id="253ce-113">Description</span><span class="sxs-lookup"><span data-stu-id="253ce-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="253ce-114">`EnumFields` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="253ce-114">`EnumFields` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="253ce-115">Il n’existe pas de champs à énumérer.</span><span class="sxs-lookup"><span data-stu-id="253ce-115">There are no fields to enumerate.</span></span> <span data-ttu-id="253ce-116">Dans ce cas, `pcTokens` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="253ce-116">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="253ce-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="253ce-117">Requirements</span></span>  
 <span data-ttu-id="253ce-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="253ce-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="253ce-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="253ce-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="253ce-120">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="253ce-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="253ce-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="253ce-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="253ce-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="253ce-122">See also</span></span>
- [<span data-ttu-id="253ce-123">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="253ce-123">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="253ce-124">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="253ce-124">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
