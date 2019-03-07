---
title: IMetaDataImport::EnumParams, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumParams
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumParams
helpviewer_keywords:
- IMetaDataImport::EnumParams method [.NET Framework metadata]
- EnumParams method [.NET Framework metadata]
ms.assetid: 52118dc9-fe6e-4b39-aa48-c3cc3ea4214d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ab5200cbd3a37bba31d52f9934e11aecc88c59c0
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57502408"
---
# <a name="imetadataimportenumparams-method"></a><span data-ttu-id="46311-102">IMetaDataImport::EnumParams, méthode</span><span class="sxs-lookup"><span data-stu-id="46311-102">IMetaDataImport::EnumParams Method</span></span>
<span data-ttu-id="46311-103">Énumère les jetons ParamDef représentant les paramètres de la méthode référencée par le jeton MethodDef spécifié.</span><span class="sxs-lookup"><span data-stu-id="46311-103">Enumerates ParamDef tokens representing the parameters of the method referenced by the specified MethodDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46311-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46311-104">Syntax</span></span>  
  
```  
HRESULT EnumParams (  
   [in, out] HCORENUM    *phEnum,  
   [in]  mdMethodDef     mb,  
   [out] mdParamDef      rParams[],  
   [in]  ULONG           cMax,  
   [out] ULONG          *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="46311-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46311-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="46311-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="46311-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="46311-107">Cela doit être NULL pour le premier appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="46311-107">This must be NULL for the first call of this method.</span></span>  
  
 `mb`  
 <span data-ttu-id="46311-108">[in] Jeton MethodDef représentant la méthode avec les paramètres à énumérer.</span><span class="sxs-lookup"><span data-stu-id="46311-108">[in] A MethodDef token representing the method with the parameters to enumerate.</span></span>  
  
 `rParams`  
 <span data-ttu-id="46311-109">[out] Tableau utilisé pour stocker les jetons ParamDef.</span><span class="sxs-lookup"><span data-stu-id="46311-109">[out] The array used to store the ParamDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="46311-110">[in] Taille maximale du tableau `rParams`.</span><span class="sxs-lookup"><span data-stu-id="46311-110">[in] The maximum size of the `rParams` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="46311-111">[out] Le nombre de jetons ParamDef retournés dans `rParams`.</span><span class="sxs-lookup"><span data-stu-id="46311-111">[out] The number of ParamDef tokens returned in `rParams`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="46311-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="46311-112">Return Value</span></span>  
  
|<span data-ttu-id="46311-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="46311-113">HRESULT</span></span>|<span data-ttu-id="46311-114">Description</span><span class="sxs-lookup"><span data-stu-id="46311-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="46311-115">`EnumParams` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="46311-115">`EnumParams` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="46311-116">Il n’existe pas de jetons à énumérer.</span><span class="sxs-lookup"><span data-stu-id="46311-116">There are no tokens to enumerate.</span></span> <span data-ttu-id="46311-117">Dans ce cas, `pcTokens` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="46311-117">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="46311-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="46311-118">Requirements</span></span>  
 <span data-ttu-id="46311-119">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="46311-119">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46311-120">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="46311-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="46311-121">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="46311-121">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="46311-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46311-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46311-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46311-123">See also</span></span>
- [<span data-ttu-id="46311-124">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="46311-124">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="46311-125">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="46311-125">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
