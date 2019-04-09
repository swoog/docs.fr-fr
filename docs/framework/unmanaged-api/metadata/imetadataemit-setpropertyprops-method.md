---
title: IMetaDataEmit::SetPropertyProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetPropertyProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetPropertyProps
helpviewer_keywords:
- SetPropertyProps method [.NET Framework metadata]
- IMetaDataEmit::SetPropertyProps method [.NET Framework metadata]
ms.assetid: e2501fc8-b2bc-4dcc-9205-e3acd5a53ffe
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fdee8491b22675fb8dd8fa89e77ebf8541185173
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59207889"
---
# <a name="imetadataemitsetpropertyprops-method"></a><span data-ttu-id="36282-102">IMetaDataEmit::SetPropertyProps, méthode</span><span class="sxs-lookup"><span data-stu-id="36282-102">IMetaDataEmit::SetPropertyProps Method</span></span>
<span data-ttu-id="36282-103">Définit les fonctionnalités stockées dans les métadonnées pour une propriété définie par un appel antérieur à [DefineProperty, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineproperty-method.md).</span><span class="sxs-lookup"><span data-stu-id="36282-103">Sets the features stored in metadata for a property defined by a prior call to [DefineProperty Method](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineproperty-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="36282-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36282-104">Syntax</span></span>  
  
```  
HRESULT SetPropertyProps (   
    [in]  mdProperty      pr,   
    [in]  DWORD           dwPropFlags,   
    [in]  DWORD           dwCPlusTypeFlag,   
    [in]  void const      *pValue,   
    [in]  ULONG           cchValue,   
    [in]  mdMethodDef     mdSetter,   
    [in]  mdMethodDef     mdGetter,   
    [in]  mdMethodDef     rmdOtherMethods[]   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="36282-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36282-105">Parameters</span></span>  
 `pr`  
 <span data-ttu-id="36282-106">[in] Le jeton pour la propriété à modifier</span><span class="sxs-lookup"><span data-stu-id="36282-106">[in] The token for the property to be changed</span></span>  
  
 `dwPropFlags`  
 <span data-ttu-id="36282-107">[in] Indicateurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="36282-107">[in] Property flags.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="36282-108">[in] Le type de la valeur de propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="36282-108">[in] The type of the property's default value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="36282-109">[in] La valeur par défaut pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="36282-109">[in] The default value for the property.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="36282-110">[in] Le nombre de caractères (Unicode) les caractères de `pValue`.</span><span class="sxs-lookup"><span data-stu-id="36282-110">[in] The count of (Unicode) characters in `pValue`.</span></span>  
  
 `mdSetter`  
 <span data-ttu-id="36282-111">[in] La méthode qui définit la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="36282-111">[in] The method that sets the property value.</span></span>  
  
 `mdGetter`  
 <span data-ttu-id="36282-112">[in] La méthode qui obtient la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="36282-112">[in] The method that gets the property value.</span></span>  
  
 `rmdOtherMethods[]`  
 <span data-ttu-id="36282-113">[in] Tableau des autres méthodes associées à la propriété.</span><span class="sxs-lookup"><span data-stu-id="36282-113">[in] An array of other methods associated with the property.</span></span> <span data-ttu-id="36282-114">Mettre fin à ce tableau avec un `mdTokenNil` jeton.</span><span class="sxs-lookup"><span data-stu-id="36282-114">Terminate this array with an `mdTokenNil` token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="36282-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36282-115">Requirements</span></span>  
 <span data-ttu-id="36282-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="36282-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="36282-117">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="36282-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="36282-118">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="36282-118">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="36282-119">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="36282-119">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="36282-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36282-120">See also</span></span>

- [<span data-ttu-id="36282-121">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="36282-121">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="36282-122">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="36282-122">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
