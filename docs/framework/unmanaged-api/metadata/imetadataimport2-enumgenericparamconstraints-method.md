---
title: IMetaDataImport2::EnumGenericParamConstraints, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.EnumGenericParamConstraints
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::EnumGenericParamConstraints
helpviewer_keywords:
- EnumGenericParamConstraints method [.NET Framework metadata]
- IMetaDataImport2::EnumGenericParamConstraints method [.NET Framework metadata]
ms.assetid: 8a7d4e40-28fe-4e14-b801-4049880130e7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fd5d35cb13bb55fc73e160089cbc1050cb3d5c0e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33449216"
---
# <a name="imetadataimport2enumgenericparamconstraints-method"></a><span data-ttu-id="c7342-102">IMetaDataImport2::EnumGenericParamConstraints, méthode</span><span class="sxs-lookup"><span data-stu-id="c7342-102">IMetaDataImport2::EnumGenericParamConstraints Method</span></span>
<span data-ttu-id="c7342-103">Obtient un énumérateur pour un tableau de contraintes de paramètres génériques associé au paramètre générique représenté par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="c7342-103">Gets an enumerator for an array of generic parameter constraints associated with the generic parameter represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7342-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7342-104">Syntax</span></span>  
  
```  
HRESULT EnumGenericParamConstraints (  
    [in, out] HCORENUM                *phEnum,  
    [in]  mdGenericParam              tk,  
    [out] mdGenericParamConstraint    rGenericParamConstraints[],  
    [in]  ULONG                       cMax,  
    [out] ULONG                       *pcGenericParamConstraints  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c7342-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7342-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="c7342-106">[dans, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="c7342-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `tk`  
 <span data-ttu-id="c7342-107">[in]   Jeton qui représente le paramètre générique dont les contraintes doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="c7342-107">[in]   A token that represents the generic parameter whose constraints are to be enumerated.</span></span>  
  
 `rGenericParamConstraints`  
 <span data-ttu-id="c7342-108">[out] Tableau de contraintes de paramètre générique pour les énumérer.</span><span class="sxs-lookup"><span data-stu-id="c7342-108">[out] The array of generic parameter constraints to enumerate.</span></span>  
  
 `cMax`  
 <span data-ttu-id="c7342-109">[in]   Nombre maximal demandé de jetons à placer dans `rGenericParamConstraints`.</span><span class="sxs-lookup"><span data-stu-id="c7342-109">[in]   The requested maximum number of tokens to place in `rGenericParamConstraints`.</span></span>  
  
 `pcGenericParamConstraints`  
 <span data-ttu-id="c7342-110">[out] Un pointeur vers le nombre de jetons placés dans `rGenericParamConstraints`.</span><span class="sxs-lookup"><span data-stu-id="c7342-110">[out] A pointer to the number of tokens placed in `rGenericParamConstraints`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c7342-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c7342-111">Return Value</span></span>  
  
|<span data-ttu-id="c7342-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c7342-112">HRESULT</span></span>|<span data-ttu-id="c7342-113">Description</span><span class="sxs-lookup"><span data-stu-id="c7342-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="c7342-114">`EnumGenericParameterConstraints` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="c7342-114">`EnumGenericParameterConstraints` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="c7342-115">`phEnum` ne contient aucun élément de membre.</span><span class="sxs-lookup"><span data-stu-id="c7342-115">`phEnum` has no member elements.</span></span> <span data-ttu-id="c7342-116">Dans ce cas, `pcGenericParameterConstraints` est définie sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="c7342-116">In this case, `pcGenericParameterConstraints` is set to 0 (zero).</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c7342-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c7342-117">Requirements</span></span>  
 <span data-ttu-id="c7342-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c7342-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7342-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c7342-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c7342-120">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c7342-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c7342-121">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7342-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7342-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7342-122">See Also</span></span>  
 [<span data-ttu-id="c7342-123">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="c7342-123">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)  
 [<span data-ttu-id="c7342-124">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="c7342-124">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
