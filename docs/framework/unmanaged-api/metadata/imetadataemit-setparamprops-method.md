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
ms.openlocfilehash: e51cb1049737e6b325656057060a88123f69a9b4
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57493321"
---
# <a name="imetadataemitsetparamprops-method"></a><span data-ttu-id="f0b93-102">IMetaDataEmit::SetParamProps, méthode</span><span class="sxs-lookup"><span data-stu-id="f0b93-102">IMetaDataEmit::SetParamProps Method</span></span>
<span data-ttu-id="f0b93-103">Définit ou modifie les fonctionnalités d’un paramètre de méthode qui a été défini par un appel antérieur à [IMetaDataEmit::DefineParam](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineparam-method.md).</span><span class="sxs-lookup"><span data-stu-id="f0b93-103">Sets or changes features of a method parameter that was defined by a prior call to [IMetaDataEmit::DefineParam](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineparam-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0b93-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0b93-104">Syntax</span></span>  
  
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
  
## <a name="parameters"></a><span data-ttu-id="f0b93-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0b93-105">Parameters</span></span>  
 `pd`  
 <span data-ttu-id="f0b93-106">[in] Le jeton pour le paramètre cible.</span><span class="sxs-lookup"><span data-stu-id="f0b93-106">[in] The token for the target parameter.</span></span>  
  
 `szName`  
 <span data-ttu-id="f0b93-107">[in] Le nom du paramètre au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="f0b93-107">[in] The name of the parameter in Unicode.</span></span>  
  
 `dwParamFlags`  
 <span data-ttu-id="f0b93-108">[in] Indicateurs pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="f0b93-108">[in] The flags for the parameter.</span></span>  
  
 `dwCPlusTypeFlag`  
 <span data-ttu-id="f0b93-109">[in] Le ELEMENT_TYPE_ \* pour la valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="f0b93-109">[in] The ELEMENT_TYPE_\* for the constant value.</span></span>  
  
 `pValue`  
 <span data-ttu-id="f0b93-110">[in] La valeur de constante pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="f0b93-110">[in] The constant value for the parameter.</span></span>  
  
 `cchValue`  
 <span data-ttu-id="f0b93-111">[in] La taille en caractères (Unicode) de `pValue`.</span><span class="sxs-lookup"><span data-stu-id="f0b93-111">[in] The size in (Unicode) characters of `pValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0b93-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f0b93-112">Requirements</span></span>  
 <span data-ttu-id="f0b93-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f0b93-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0b93-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="f0b93-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f0b93-115">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f0b93-115">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f0b93-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0b93-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0b93-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0b93-117">See also</span></span>
- [<span data-ttu-id="f0b93-118">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="f0b93-118">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="f0b93-119">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="f0b93-119">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
