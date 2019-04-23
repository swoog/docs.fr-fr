---
title: IMetaDataEmit::SetParamProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetParamProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetParamProps
helpviewer_keywords:
- IMetaDataEmit::SetParamProps method [.NET Framework metadata]
- SetParamProps method [.NET Framework metadata]
ms.assetid: a95a3908-9f87-4084-937e-8e01ef03ad63
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6b7cfba90edab44a0053fdfc759417ee7f074401
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59132028"
---
# <a name="imetadataemitsetparamprops-method"></a><span data-ttu-id="8ef90-102">IMetaDataEmit::SetParamProps, méthode</span><span class="sxs-lookup"><span data-stu-id="8ef90-102">IMetaDataEmit::SetParamProps Method</span></span>
<span data-ttu-id="8ef90-103">Définit ou modifie les fonctionnalités d’un paramètre de méthode qui a été défini par un appel antérieur à [IMetaDataEmit::DefineParam](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineparam-method.md).</span><span class="sxs-lookup"><span data-stu-id="8ef90-103">Sets or changes features of a method parameter that was defined by a prior call to [IMetaDataEmit::DefineParam](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineparam-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ef90-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ef90-104">Syntax</span></span>  
  
```  
HRESULT SetParamProps (   
    [in]  mdParamDef  pd,   
    [in]  LPCWSTR     szName,   
    [in]  DWORD       dwParamFlags,   
    [in]  DWORD       dwCPlusTypeFlag,   
    [in]  void const  *pValue,   
    [in]  ULONG       cchValue   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8ef90-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ef90-105">Parameters</span></span>  
 `pd`  
 <span data-ttu-id="8ef90-106">[in] Le jeton pour le paramètre cible.</span><span class="sxs-lookup"><span data-stu-id="8ef90-106">[in] The token for the target parameter.</span></span>  
  
 `szName`  
 <span data-ttu-id="8ef90-107">[in] Le nom du paramètre au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="8ef90-107">[in] The name of the parameter in Unicode.</span></span>  
  
 `dwParamFlags`  
 <span data-ttu-id="8ef90-108">[in] Indicateurs pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="8ef90-108">[in] The flags for the parameter.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="8ef90-109">[in] Le ELEMENT_TYPE_ \* pour la valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="8ef90-109">[in] The ELEMENT_TYPE_\* for the constant value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="8ef90-110">[in] La valeur de constante pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="8ef90-110">[in] The constant value for the parameter.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="8ef90-111">[in] La taille en caractères (Unicode) de `pValue`.</span><span class="sxs-lookup"><span data-stu-id="8ef90-111">[in] The size in (Unicode) characters of `pValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ef90-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ef90-112">Requirements</span></span>  
 <span data-ttu-id="8ef90-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8ef90-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ef90-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="8ef90-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8ef90-115">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8ef90-115">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8ef90-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ef90-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ef90-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ef90-117">See also</span></span>

- [<span data-ttu-id="8ef90-118">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="8ef90-118">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="8ef90-119">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="8ef90-119">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
