---
title: IMetaDataEmit::DefineParam, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineParam
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineParam
helpviewer_keywords:
- IMetaDataEmit::DefineParam method [.NET Framework metadata]
- DefineParam method [.NET Framework metadata]
ms.assetid: d86a3d14-4796-4909-9591-dfafe3de5ce4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 86711d107636505ab7aa23f0f72f70bd3e27635d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59167770"
---
# <a name="imetadataemitdefineparam-method"></a><span data-ttu-id="b6077-102">IMetaDataEmit::DefineParam, méthode</span><span class="sxs-lookup"><span data-stu-id="b6077-102">IMetaDataEmit::DefineParam Method</span></span>
<span data-ttu-id="b6077-103">Crée une définition de paramètre avec la signature spécifiée pour la méthode référencée par le jeton spécifié et obtient un jeton pour cette définition de paramètre.</span><span class="sxs-lookup"><span data-stu-id="b6077-103">Creates a parameter definition with the specified signature for the method referenced by the specified token, and gets a token for that parameter definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6077-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6077-104">Syntax</span></span>  
  
```  
HRESULT DefineParam (  
    [in]  mdMethodDef md,   
    [in]  ULONG       ulParamSeq,   
    [in]  LPCWSTR     szName,   
    [in]  DWORD       dwParamFlags,   
    [in]  DWORD       dwCPlusTypeFlag,   
    [in]  void const  *pValue,  
    [in]  ULONG       cchValue,   
    [out] mdParamDef  *ppd   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b6077-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6077-105">Parameters</span></span>  
 `md`  
 <span data-ttu-id="b6077-106">[in] Le jeton pour la méthode dont le paramètre est défini.</span><span class="sxs-lookup"><span data-stu-id="b6077-106">[in] The token for the method whose parameter is being defined.</span></span>  
  
 `ulParamSeq`  
 <span data-ttu-id="b6077-107">[in] Numéro de séquence du paramètre.</span><span class="sxs-lookup"><span data-stu-id="b6077-107">[in] The parameter sequence number.</span></span>  
  
 `szName`  
 <span data-ttu-id="b6077-108">[in] Le nom du paramètre au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="b6077-108">[in] The name of the parameter in Unicode.</span></span>  
  
 `dwParamFlags`  
 <span data-ttu-id="b6077-109">[in] Indicateurs pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="b6077-109">[in] Flags for the parameter.</span></span> <span data-ttu-id="b6077-110">Il s’agit d’un masque de bits de `CorParamAttr` valeurs.</span><span class="sxs-lookup"><span data-stu-id="b6077-110">This is a bitmask of `CorParamAttr` values.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="b6077-111">[in] `ELEMENT_TYPE_` *\** pour la valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="b6077-111">[in] `ELEMENT_TYPE_`*\** for the constant value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="b6077-112">[in] La valeur de constante pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="b6077-112">[in] The constant value for the parameter.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="b6077-113">[in] La taille, en caractères Unicode, de `pValue`.</span><span class="sxs-lookup"><span data-stu-id="b6077-113">[in] The size, in Unicode characters, of `pValue`.</span></span>  
  
 `ppd`  
 <span data-ttu-id="b6077-114">[out] Le `mdParamDef` jeton attribué.</span><span class="sxs-lookup"><span data-stu-id="b6077-114">[out] The `mdParamDef` token assigned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b6077-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b6077-115">Remarks</span></span>  
 <span data-ttu-id="b6077-116">Les valeurs de séquence dans `ulParamSeq` commencent par 1 pour les paramètres.</span><span class="sxs-lookup"><span data-stu-id="b6077-116">The sequence values in `ulParamSeq` begin with 1 for parameters.</span></span> <span data-ttu-id="b6077-117">Une valeur de retour a un numéro de séquence 0.</span><span class="sxs-lookup"><span data-stu-id="b6077-117">A return value has a sequence number of 0.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b6077-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6077-118">Requirements</span></span>  
 <span data-ttu-id="b6077-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b6077-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b6077-120">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b6077-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b6077-121">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b6077-121">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b6077-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b6077-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6077-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6077-123">See also</span></span>

- [<span data-ttu-id="b6077-124">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="b6077-124">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="b6077-125">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="b6077-125">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
