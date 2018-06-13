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
ms.openlocfilehash: bd8a2d373b801bd8238d50eecb388ef511bc34bc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33446200"
---
# <a name="imetadataimportenumfields-method"></a><span data-ttu-id="369b0-102">IMetaDataImport::EnumFields, méthode</span><span class="sxs-lookup"><span data-stu-id="369b0-102">IMetaDataImport::EnumFields Method</span></span>
<span data-ttu-id="369b0-103">Énumère les jetons FieldDef pour le type référencé par le jeton TypeDef spécifié.</span><span class="sxs-lookup"><span data-stu-id="369b0-103">Enumerates FieldDef tokens for the type referenced by the specified TypeDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="369b0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="369b0-104">Syntax</span></span>  
  
```  
HRESULT EnumFields (   
   [in, out] HCORENUM    *phEnum,   
   [in]      mdTypeDef   cl,   
   [out]     mdFieldDef  rFields[],   
   [in]      ULONG       cMax,   
   [out]     ULONG       *pcTokens  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="369b0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="369b0-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="369b0-106">[dans, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="369b0-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `cl`  
 <span data-ttu-id="369b0-107">[in] Le jeton TypeDef de la classe dont les champs doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="369b0-107">[in] The TypeDef token of the class whose fields are to be enumerated.</span></span>  
  
 `rFields`  
 <span data-ttu-id="369b0-108">[out] La liste des jetons FieldDef.</span><span class="sxs-lookup"><span data-stu-id="369b0-108">[out] The list of FieldDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="369b0-109">[in] Taille maximale du tableau `rFields`.</span><span class="sxs-lookup"><span data-stu-id="369b0-109">[in] The maximum size of the `rFields` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="369b0-110">[out] Le nombre réel de jetons FieldDef retournés dans `rFields`.</span><span class="sxs-lookup"><span data-stu-id="369b0-110">[out] The actual number of FieldDef tokens returned in `rFields`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="369b0-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="369b0-111">Return Value</span></span>  
  
|<span data-ttu-id="369b0-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="369b0-112">HRESULT</span></span>|<span data-ttu-id="369b0-113">Description</span><span class="sxs-lookup"><span data-stu-id="369b0-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="369b0-114">`EnumFields` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="369b0-114">`EnumFields` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="369b0-115">Il n’existe pas de champs à énumérer.</span><span class="sxs-lookup"><span data-stu-id="369b0-115">There are no fields to enumerate.</span></span> <span data-ttu-id="369b0-116">Dans ce cas, `pcTokens` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="369b0-116">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="369b0-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="369b0-117">Requirements</span></span>  
 <span data-ttu-id="369b0-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="369b0-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="369b0-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="369b0-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="369b0-120">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="369b0-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="369b0-121">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="369b0-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="369b0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="369b0-122">See Also</span></span>  
 [<span data-ttu-id="369b0-123">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="369b0-123">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="369b0-124">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="369b0-124">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
