---
title: IMetaDataImport2::EnumMethodSpecs, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.EnumMethodSpecs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::EnumMethodSpecs
helpviewer_keywords:
- IMetaDataImport2::EnumMethodSpecs method [.NET Framework metadata]
- EnumMethodSpecs method [.NET Framework metadata]
ms.assetid: b3fc1e6c-bcb6-4915-baf8-7dc0a31b8724
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 24ad5ff05e4f7fe7fcfc06ff5fe096d47e8b3cbb
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57468206"
---
# <a name="imetadataimport2enummethodspecs-method"></a><span data-ttu-id="c3249-102">IMetaDataImport2::EnumMethodSpecs, méthode</span><span class="sxs-lookup"><span data-stu-id="c3249-102">IMetaDataImport2::EnumMethodSpecs Method</span></span>
<span data-ttu-id="c3249-103">Obtient un énumérateur pour un tableau de jetons MethodSpec associé à le MethodDef ou MemberRef spécifié de jeton.</span><span class="sxs-lookup"><span data-stu-id="c3249-103">Gets an enumerator for an array of MethodSpec tokens associated with the specified MethodDef or MemberRef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c3249-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3249-104">Syntax</span></span>  
  
```  
HRESULT EnumMethodSpecs (  
    [in, out] HCORENUM      *phEnum,   
    [in]      mdToken       tk,  
    [out]     mdMethodSpec  rMethodSpecs[],  
    [in]      ULONG         cMax,  
    [out]     ULONG         *pcMethodSpecs  
);   
```  
  
## <a name="parameters"></a><span data-ttu-id="c3249-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3249-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="c3249-106">[in, out] Un pointeur vers l’énumérateur pour `rMethodSpecs`.</span><span class="sxs-lookup"><span data-stu-id="c3249-106">[in, out] A pointer to the enumerator for `rMethodSpecs`.</span></span>  
  
 `tk`  
 <span data-ttu-id="c3249-107">[in] Le jeton MemberRef ou MethodDef qui représente la méthode dont les jetons MethodSpec doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="c3249-107">[in] The MemberRef or MethodDef token that represents the method whose MethodSpec tokens are to be enumerated.</span></span> <span data-ttu-id="c3249-108">Si la valeur de `tk` est 0 (zéro), tous les jetons MethodSpec dans la portée seront énumérés.</span><span class="sxs-lookup"><span data-stu-id="c3249-108">If the value of `tk` is 0 (zero), all MethodSpec tokens in the scope will be enumerated.</span></span>  
  
 `rMethodSpecs`  
 <span data-ttu-id="c3249-109">[out] Le tableau de jetons MethodSpec à énumérer.</span><span class="sxs-lookup"><span data-stu-id="c3249-109">[out] The array of MethodSpec tokens to enumerate.</span></span>  
  
 `cMax`  
 <span data-ttu-id="c3249-110">[in] Le nombre maximal demandé de jetons à placer dans `rMethodSpecs`.</span><span class="sxs-lookup"><span data-stu-id="c3249-110">[in] The requested maximum number of tokens to place in `rMethodSpecs`.</span></span>  
  
 `pcMethodSpecs`  
 <span data-ttu-id="c3249-111">[out] Le nombre retourné de jetons placés dans `rMethodSpecs`.</span><span class="sxs-lookup"><span data-stu-id="c3249-111">[out] The returned number of tokens placed in `rMethodSpecs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c3249-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c3249-112">Return Value</span></span>  
  
|<span data-ttu-id="c3249-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c3249-113">HRESULT</span></span>|<span data-ttu-id="c3249-114">Description</span><span class="sxs-lookup"><span data-stu-id="c3249-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="c3249-115">`EnumMethodSpecs` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="c3249-115">`EnumMethodSpecs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="c3249-116">`phEnum` ne contient aucun élément de membre.</span><span class="sxs-lookup"><span data-stu-id="c3249-116">`phEnum` has no member elements.</span></span> <span data-ttu-id="c3249-117">Dans ce cas, `pcMethodSpecs` est définie sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="c3249-117">In this case, `pcMethodSpecs` is set to 0 (zero).</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c3249-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c3249-118">Requirements</span></span>  
 <span data-ttu-id="c3249-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c3249-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c3249-120">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c3249-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c3249-121">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c3249-121">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c3249-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c3249-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c3249-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3249-123">See also</span></span>
- [<span data-ttu-id="c3249-124">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="c3249-124">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
- [<span data-ttu-id="c3249-125">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="c3249-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
