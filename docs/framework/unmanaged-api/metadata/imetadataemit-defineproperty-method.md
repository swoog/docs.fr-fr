---
title: IMetaDataEmit::DefineProperty, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineProperty
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineProperty
helpviewer_keywords:
- IMetaDataEmit::DefineProperty method [.NET Framework metadata]
- DefineProperty method [.NET Framework metadata]
ms.assetid: 5c4c1dc2-d40d-4173-bbe6-7058fb21c98f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ee9f771a3df1de67bef70cdb6f8c166040150e0d
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57468739"
---
# <a name="imetadataemitdefineproperty-method"></a><span data-ttu-id="ce6a2-102">IMetaDataEmit::DefineProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="ce6a2-102">IMetaDataEmit::DefineProperty Method</span></span>
<span data-ttu-id="ce6a2-103">Crée une définition de propriété pour le type spécifié, avec la valeur `get` et `set` accesseurs de méthode et obtient un jeton pour cette définition de propriété.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-103">Creates a property definition for the specified type, with the specified `get` and `set` method accessors, and gets a token to that property definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce6a2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce6a2-104">Syntax</span></span>  
  
```  
HRESULT DefineProperty (   
    [in]  mdTypeDef          td,   
    [in]  LPCWSTR            szProperty,   
    [in]  DWORD              dwPropFlags,   
    [in]  PCCOR_SIGNATURE    pvSig,   
    [in]  ULONG              cbSig,   
    [in]  DWORD              dwCPlusTypeFlag,   
    [in]  void const         *pValue,   
    [in]  ULONG              cchValue,   
    [in]  mdMethodDef        mdSetter,   
    [in]  mdMethodDef        mdGetter,   
    [in]  mdMethodDef        rmdOtherMethods[],   
    [out] mdProperty         *pmdProp   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ce6a2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce6a2-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="ce6a2-106">[in] Le jeton pour la classe ou interface sur lequel la propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-106">[in] The token for class or interface on which the property is being defined.</span></span>  
  
 `szProperty`  
 <span data-ttu-id="ce6a2-107">[in] Le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-107">[in] The name of the property.</span></span>  
  
 `dwPropFlags`  
 <span data-ttu-id="ce6a2-108">[in] Indicateurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-108">[in] The property flags.</span></span>  
  
 `pvSig`  
 <span data-ttu-id="ce6a2-109">[in] La signature de propriété.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-109">[in] The property signature.</span></span>  
  
 `cbSig`  
 <span data-ttu-id="ce6a2-110">[in] Le nombre d’octets dans `pvSig`.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-110">[in] The count of bytes in `pvSig`.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="ce6a2-111">[in] Le type de la valeur de propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-111">[in] The type of the property's default value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="ce6a2-112">[in] La valeur par défaut pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-112">[in] The default value for the property.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="ce6a2-113">[in] Le nombre de caractères (Unicode) les caractères de `pValue`.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-113">[in] The count of (Unicode) characters in `pValue`.</span></span>  
  
 `mdSetter`  
 <span data-ttu-id="ce6a2-114">[in] La méthode qui définit la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-114">[in] The method that sets the property value.</span></span>  
  
 `mdGetter`  
 <span data-ttu-id="ce6a2-115">[in] La méthode qui obtient la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-115">[in] The method that gets the property value.</span></span>  
  
 `rmdOtherMethods[]`  
 <span data-ttu-id="ce6a2-116">[in] Tableau des autres méthodes associées à la propriété.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-116">[in] An array of other methods associated with the property.</span></span> <span data-ttu-id="ce6a2-117">Terminez le tableau avec un `mdTokenNil`.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-117">Terminate the array with an `mdTokenNil`.</span></span>  
  
 `pmdProp`  
 <span data-ttu-id="ce6a2-118">[out] Le `mdProperty` jeton attribué.</span><span class="sxs-lookup"><span data-stu-id="ce6a2-118">[out] The `mdProperty` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ce6a2-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ce6a2-119">Requirements</span></span>  
 <span data-ttu-id="ce6a2-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ce6a2-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ce6a2-121">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ce6a2-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ce6a2-122">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ce6a2-122">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ce6a2-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ce6a2-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce6a2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce6a2-124">See also</span></span>
- [<span data-ttu-id="ce6a2-125">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="ce6a2-125">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="ce6a2-126">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="ce6a2-126">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
