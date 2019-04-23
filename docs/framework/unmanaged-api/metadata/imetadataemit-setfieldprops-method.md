---
title: IMetaDataEmit::SetFieldProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetFieldProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetFieldProps
helpviewer_keywords:
- IMetaDataEmit::SetFieldProps method [.NET Framework metadata]
- SetFieldProps method [.NET Framework metadata]
ms.assetid: 47132dda-fa92-4bd1-ae4b-24cd9a60665a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 94ba607669b4b1ca68294470cf1cc4fb27464d28
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59097653"
---
# <a name="imetadataemitsetfieldprops-method"></a><span data-ttu-id="088b6-102">IMetaDataEmit::SetFieldProps, méthode</span><span class="sxs-lookup"><span data-stu-id="088b6-102">IMetaDataEmit::SetFieldProps Method</span></span>
<span data-ttu-id="088b6-103">Définit ou met à jour la valeur par défaut pour le champ référencé par le jeton de champ spécifié.</span><span class="sxs-lookup"><span data-stu-id="088b6-103">Sets or updates the default value for the field referenced by the specified field token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="088b6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="088b6-104">Syntax</span></span>  
  
```  
HRESULT SetFieldProps (  
    [in]  mdFieldDef  fd,   
    [in]  DWORD       dwFieldFlags,   
    [in]  DWORD       dwCPlusTypeFlag,   
    [in]  void const  *pValue,   
    [in]  ULONG       cchValue   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="088b6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="088b6-105">Parameters</span></span>  
 `fd`  
 <span data-ttu-id="088b6-106">[in] Le jeton pour le champ cible.</span><span class="sxs-lookup"><span data-stu-id="088b6-106">[in] The token for the target field.</span></span>  
  
 `dwFieldFlags`  
 <span data-ttu-id="088b6-107">[in] Attributs de champ.</span><span class="sxs-lookup"><span data-stu-id="088b6-107">[in] Field attributes.</span></span> <span data-ttu-id="088b6-108">Il s’agit d’un masque de bits de `CorFieldAttr` valeurs.</span><span class="sxs-lookup"><span data-stu-id="088b6-108">This is a bitmask of `CorFieldAttr` values.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="088b6-109">[in] Le `ELEMENT_TYPE_` *\** pour la valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="088b6-109">[in] The `ELEMENT_TYPE_`*\** for the constant value.</span></span> <span data-ttu-id="088b6-110">Il s’agit d’un `CorElementType` valeur.</span><span class="sxs-lookup"><span data-stu-id="088b6-110">This is a `CorElementType` value.</span></span> <span data-ttu-id="088b6-111">Si une constante n’est pas définie, définissez cette valeur sur `ELEMENT_TYPE_END`.</span><span class="sxs-lookup"><span data-stu-id="088b6-111">If a constant is not being defined, set this value to `ELEMENT_TYPE_END`.</span></span>  
  
 `pValue`  
 <span data-ttu-id="088b6-112">[in] La valeur de constante pour le champ.</span><span class="sxs-lookup"><span data-stu-id="088b6-112">[in] The constant value for the field.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="088b6-113">[in] La taille, en caractères Unicode, de `pValue`.</span><span class="sxs-lookup"><span data-stu-id="088b6-113">[in] The size, in Unicode characters, of `pValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="088b6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="088b6-114">Requirements</span></span>  
 <span data-ttu-id="088b6-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="088b6-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="088b6-116">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="088b6-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="088b6-117">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="088b6-117">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="088b6-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="088b6-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="088b6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="088b6-119">See also</span></span>

- [<span data-ttu-id="088b6-120">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="088b6-120">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="088b6-121">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="088b6-121">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
