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
ms.openlocfilehash: 1b80833892fc1c0290e94f5de7d9b081529c6a37
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59085023"
---
# <a name="imetadataemitdefineproperty-method"></a><span data-ttu-id="b5c00-102">IMetaDataEmit::DefineProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="b5c00-102">IMetaDataEmit::DefineProperty Method</span></span>
<span data-ttu-id="b5c00-103">Crée une définition de propriété pour le type spécifié, avec la valeur `get` et `set` accesseurs de méthode et obtient un jeton pour cette définition de propriété.</span><span class="sxs-lookup"><span data-stu-id="b5c00-103">Creates a property definition for the specified type, with the specified `get` and `set` method accessors, and gets a token to that property definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b5c00-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5c00-104">Syntax</span></span>  
  
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
  
## <a name="parameters"></a><span data-ttu-id="b5c00-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5c00-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="b5c00-106">[in] Le jeton pour la classe ou interface sur lequel la propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="b5c00-106">[in] The token for class or interface on which the property is being defined.</span></span>  
  
 `szProperty`  
 <span data-ttu-id="b5c00-107">[in] Le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="b5c00-107">[in] The name of the property.</span></span>  
  
 `dwPropFlags`  
 <span data-ttu-id="b5c00-108">[in] Indicateurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="b5c00-108">[in] The property flags.</span></span>  
  
 `pvSig`  
 <span data-ttu-id="b5c00-109">[in] La signature de propriété.</span><span class="sxs-lookup"><span data-stu-id="b5c00-109">[in] The property signature.</span></span>  
  
 `cbSig`  
 <span data-ttu-id="b5c00-110">[in] Le nombre d’octets dans `pvSig`.</span><span class="sxs-lookup"><span data-stu-id="b5c00-110">[in] The count of bytes in `pvSig`.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="b5c00-111">[in] Le type de la valeur de propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="b5c00-111">[in] The type of the property's default value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="b5c00-112">[in] La valeur par défaut pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="b5c00-112">[in] The default value for the property.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="b5c00-113">[in] Le nombre de caractères (Unicode) les caractères de `pValue`.</span><span class="sxs-lookup"><span data-stu-id="b5c00-113">[in] The count of (Unicode) characters in `pValue`.</span></span>  
  
 `mdSetter`  
 <span data-ttu-id="b5c00-114">[in] La méthode qui définit la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="b5c00-114">[in] The method that sets the property value.</span></span>  
  
 `mdGetter`  
 <span data-ttu-id="b5c00-115">[in] La méthode qui obtient la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="b5c00-115">[in] The method that gets the property value.</span></span>  
  
 `rmdOtherMethods[]`  
 <span data-ttu-id="b5c00-116">[in] Tableau des autres méthodes associées à la propriété.</span><span class="sxs-lookup"><span data-stu-id="b5c00-116">[in] An array of other methods associated with the property.</span></span> <span data-ttu-id="b5c00-117">Terminez le tableau avec un `mdTokenNil`.</span><span class="sxs-lookup"><span data-stu-id="b5c00-117">Terminate the array with an `mdTokenNil`.</span></span>  
  
 `pmdProp`  
 <span data-ttu-id="b5c00-118">[out] Le `mdProperty` jeton attribué.</span><span class="sxs-lookup"><span data-stu-id="b5c00-118">[out] The `mdProperty` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b5c00-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5c00-119">Requirements</span></span>  
 <span data-ttu-id="b5c00-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b5c00-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b5c00-121">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b5c00-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b5c00-122">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b5c00-122">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="b5c00-123">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b5c00-123">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b5c00-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5c00-124">See also</span></span>

- [<span data-ttu-id="b5c00-125">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="b5c00-125">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="b5c00-126">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="b5c00-126">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
