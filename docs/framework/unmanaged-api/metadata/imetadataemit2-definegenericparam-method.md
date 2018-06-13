---
title: IMetaDataEmit2::DefineGenericParam, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.DefineGenericParam
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::DefineGenericParam
helpviewer_keywords:
- IMetaDataEmit2::DefineGenericParam method [.NET Framework metadata]
- DefineGenericParam method [.NET Framework metadata]
ms.assetid: 47b2a3b6-907d-43dc-858d-1ae7dca1316a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 66b2b9d6fb3f6379abb92fe081f36b487f9df234
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33446452"
---
# <a name="imetadataemit2definegenericparam-method"></a><span data-ttu-id="7f8e6-102">IMetaDataEmit2::DefineGenericParam, méthode</span><span class="sxs-lookup"><span data-stu-id="7f8e6-102">IMetaDataEmit2::DefineGenericParam Method</span></span>
<span data-ttu-id="7f8e6-103">Crée une définition pour un paramètre de type générique et obtient un jeton pour ce paramètre de type générique.</span><span class="sxs-lookup"><span data-stu-id="7f8e6-103">Creates a definition for a generic type parameter, and gets a token to that generic type parameter.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f8e6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f8e6-104">Syntax</span></span>  
  
```  
HRESULT DefineGenericParam (   
    [in]  mdToken         tk,   
    [in]  ULONG           ulParamSeq,   
    [in]  DWORD           dwParamFlags,   
    [in]  LPCWSTR         szname,   
    [in]  DWORD           reserved,   
    [in]  mdToken         rtkConstraints[],   
    [out] mdGenericParam  *pgp  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7f8e6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f8e6-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="7f8e6-106">[in] Un `mdTypeDef` ou `mdMethodDef` jeton qui représente la méthode ou le constructeur pour laquelle vous définissez un paramètre générique.</span><span class="sxs-lookup"><span data-stu-id="7f8e6-106">[in] An `mdTypeDef` or `mdMethodDef` token that represents the method or constructor for which to define a generic parameter.</span></span>  
  
 `ulParamSeq`  
 <span data-ttu-id="7f8e6-107">[in] L’index du paramètre générique.</span><span class="sxs-lookup"><span data-stu-id="7f8e6-107">[in] The index of the generic parameter.</span></span>  
  
 `dwParamFlags`  
 <span data-ttu-id="7f8e6-108">[in] Une valeur de la [CorGenericParamAttr](../../../../docs/framework/unmanaged-api/metadata/corgenericparamattr-enumeration.md) énumération qui décrit le type du paramètre générique.</span><span class="sxs-lookup"><span data-stu-id="7f8e6-108">[in] A value of the [CorGenericParamAttr](../../../../docs/framework/unmanaged-api/metadata/corgenericparamattr-enumeration.md) enumeration that describes the type for the generic parameter.</span></span>  
  
 `szname`  
 <span data-ttu-id="7f8e6-109">[in] Le nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="7f8e6-109">[in] The name of the parameter.</span></span>  
  
 `reserved`  
 <span data-ttu-id="7f8e6-110">[in] Ce paramètre est réservé pour une future extensibilité.</span><span class="sxs-lookup"><span data-stu-id="7f8e6-110">[in] This parameter is reserved for future extensibility.</span></span>  
  
 `rtkConstraints`  
 <span data-ttu-id="7f8e6-111">[in] Tableau de contraintes de type terminant par zéro.</span><span class="sxs-lookup"><span data-stu-id="7f8e6-111">[in] A zero-terminated array of type constraints.</span></span> <span data-ttu-id="7f8e6-112">Membres de tableau doivent être un `mdTypeDef`, `mdTypeRef`, ou `mdTypeSpec` jeton de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="7f8e6-112">Array members must be an `mdTypeDef`, `mdTypeRef`, or `mdTypeSpec` metadata token.</span></span>  
  
 `pgp`  
 <span data-ttu-id="7f8e6-113">[out] Jeton qui représente le paramètre générique.</span><span class="sxs-lookup"><span data-stu-id="7f8e6-113">[out] A token that represents the generic parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f8e6-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7f8e6-114">Requirements</span></span>  
 <span data-ttu-id="7f8e6-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7f8e6-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7f8e6-116">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="7f8e6-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="7f8e6-117">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7f8e6-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="7f8e6-118">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7f8e6-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f8e6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f8e6-119">See Also</span></span>  
 [<span data-ttu-id="7f8e6-120">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="7f8e6-120">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)  
 [<span data-ttu-id="7f8e6-121">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="7f8e6-121">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
