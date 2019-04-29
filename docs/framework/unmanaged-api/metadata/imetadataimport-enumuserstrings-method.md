---
title: IMetaDataImport::EnumUserStrings, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumUserStrings
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumUserStrings
helpviewer_keywords:
- IMetaDataImport::EnumUserStrings method [.NET Framework metadata]
- EnumUserStrings method [.NET Framework metadata]
ms.assetid: 2b1f1418-4be8-4cdb-b418-b3abccc527a7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f4be12e46851b11a5e6db60c351094a356fa61f2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61777921"
---
# <a name="imetadataimportenumuserstrings-method"></a><span data-ttu-id="706ef-102">IMetaDataImport::EnumUserStrings, méthode</span><span class="sxs-lookup"><span data-stu-id="706ef-102">IMetaDataImport::EnumUserStrings Method</span></span>
<span data-ttu-id="706ef-103">Énumère les jetons String représentant des chaînes codées en dur dans la portée des métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="706ef-103">Enumerates String tokens representing hard-coded strings in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="706ef-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="706ef-104">Syntax</span></span>  
  
```  
HRESULT EnumUserStrings (  
   [in, out]  HCORENUM    *phEnum,  
   [out]  mdString        rStrings[],  
   [in]   ULONG           cMax,  
   [out]  ULONG           *pcStrings  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="706ef-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="706ef-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="706ef-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="706ef-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="706ef-107">Cela doit être NULL pour le premier appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="706ef-107">This must be NULL for the first call of this method.</span></span>  
  
 `rStrings`  
 <span data-ttu-id="706ef-108">[out] Tableau utilisé pour stocker les jetons de chaîne.</span><span class="sxs-lookup"><span data-stu-id="706ef-108">[out] The array used to store the String tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="706ef-109">[in] Taille maximale du tableau `rStrings`.</span><span class="sxs-lookup"><span data-stu-id="706ef-109">[in] The maximum size of the `rStrings` array.</span></span>  
  
 `pcStrings`  
 <span data-ttu-id="706ef-110">[out] Le nombre de jetons de chaîne retournée dans `rStrings`.</span><span class="sxs-lookup"><span data-stu-id="706ef-110">[out] The number of String tokens returned in `rStrings`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="706ef-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="706ef-111">Return Value</span></span>  
  
|<span data-ttu-id="706ef-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="706ef-112">HRESULT</span></span>|<span data-ttu-id="706ef-113">Description</span><span class="sxs-lookup"><span data-stu-id="706ef-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="706ef-114">`EnumUserStrings` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="706ef-114">`EnumUserStrings` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="706ef-115">Il n’existe pas de jetons à énumérer.</span><span class="sxs-lookup"><span data-stu-id="706ef-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="706ef-116">Dans ce cas, `pcStrings` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="706ef-116">In that case, `pcStrings` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="706ef-117">Notes</span><span class="sxs-lookup"><span data-stu-id="706ef-117">Remarks</span></span>  
 <span data-ttu-id="706ef-118">Les jetons de chaîne sont créés par le [IMetaDataEmit::DefineUserString](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineuserstring-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="706ef-118">The String tokens are created by the [IMetaDataEmit::DefineUserString](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineuserstring-method.md) method.</span></span> <span data-ttu-id="706ef-119">Cette méthode est conçue pour être utilisée par un navigateur de métadonnées plutôt que par un compilateur.</span><span class="sxs-lookup"><span data-stu-id="706ef-119">This method is designed to be used by a metadata browser rather than by a compiler.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="706ef-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="706ef-120">Requirements</span></span>  
 <span data-ttu-id="706ef-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="706ef-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="706ef-122">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="706ef-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="706ef-123">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="706ef-123">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="706ef-124">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="706ef-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="706ef-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="706ef-125">See also</span></span>

- [<span data-ttu-id="706ef-126">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="706ef-126">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="706ef-127">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="706ef-127">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
