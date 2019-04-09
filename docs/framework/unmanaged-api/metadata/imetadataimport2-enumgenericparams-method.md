---
title: IMetaDataImport2::EnumGenericParams, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.EnumGenericParams
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::EnumGenericParams
helpviewer_keywords:
- EnumGenericParams method [.NET Framework metadata]
- IMetaDataImport2::EnumGenericParams method [.NET Framework metadata]
ms.assetid: b50488a5-3cf0-483c-82dc-2892a3ec61ac
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7edd2eeafcce6a22c3256d0684a9c4f961b34002
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59157636"
---
# <a name="imetadataimport2enumgenericparams-method"></a><span data-ttu-id="4eb17-102">IMetaDataImport2::EnumGenericParams, méthode</span><span class="sxs-lookup"><span data-stu-id="4eb17-102">IMetaDataImport2::EnumGenericParams Method</span></span>
<span data-ttu-id="4eb17-103">Obtient un énumérateur pour un tableau de jetons de paramètre générique associé au TypeDef spécifié ou le MethodDef jeton.</span><span class="sxs-lookup"><span data-stu-id="4eb17-103">Gets an enumerator for an array of generic parameter tokens associated with the specified TypeDef or MethodDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4eb17-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4eb17-104">Syntax</span></span>  
  
```  
HRESULT EnumGenericParams (  
   [in, out] HCORENUM     *phEnum,   
   [in]  mdToken          tk,  
   [out] mdGenericParam   rGenericParams[],   
   [in]  ULONG            cMax,   
   [out] ULONG            *pcGenericParams  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4eb17-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4eb17-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="4eb17-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="4eb17-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `tk`  
 <span data-ttu-id="4eb17-107">[in] Le jeton TypeDef ou MethodDef dont les paramètres génériques doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="4eb17-107">[in] The TypeDef or MethodDef token whose generic parameters are to be enumerated.</span></span>  
  
 `rGenericParams`  
 <span data-ttu-id="4eb17-108">[out] Le tableau de paramètres génériques à énumérer.</span><span class="sxs-lookup"><span data-stu-id="4eb17-108">[out] The array of generic parameters to enumerate.</span></span>  
  
 `cMax`  
 <span data-ttu-id="4eb17-109">[in] Le nombre maximal demandé de jetons à placer dans `rGenericParams`.</span><span class="sxs-lookup"><span data-stu-id="4eb17-109">[in] The requested maximum number of tokens to place in `rGenericParams`.</span></span>  
  
 `pcGenericParams`  
 <span data-ttu-id="4eb17-110">[out] Le nombre retourné de jetons placés dans `rGenericParams`.</span><span class="sxs-lookup"><span data-stu-id="4eb17-110">[out] The returned number of tokens placed in `rGenericParams`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4eb17-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4eb17-111">Return Value</span></span>  
  
|<span data-ttu-id="4eb17-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4eb17-112">HRESULT</span></span>|<span data-ttu-id="4eb17-113">Description</span><span class="sxs-lookup"><span data-stu-id="4eb17-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|`EnumGenericParams` <span data-ttu-id="4eb17-114">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="4eb17-114">returned successfully.</span></span>|  
|`S_FALSE`|`phEnum` <span data-ttu-id="4eb17-115">ne contient aucun élément de membre.</span><span class="sxs-lookup"><span data-stu-id="4eb17-115">has no member elements.</span></span> <span data-ttu-id="4eb17-116">Dans ce cas, `pcGenericParams` est définie sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="4eb17-116">In this case, `pcGenericParams` is set to 0 (zero).</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4eb17-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4eb17-117">Requirements</span></span>  
 <span data-ttu-id="4eb17-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4eb17-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4eb17-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="4eb17-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="4eb17-120">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4eb17-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="4eb17-121">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="4eb17-121">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="4eb17-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4eb17-122">See also</span></span>

- [<span data-ttu-id="4eb17-123">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="4eb17-123">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
- [<span data-ttu-id="4eb17-124">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="4eb17-124">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
