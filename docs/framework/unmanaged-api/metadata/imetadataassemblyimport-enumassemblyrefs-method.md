---
title: IMetaDataAssemblyImport::EnumAssemblyRefs, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.EnumAssemblyRefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::EnumAssemblyRefs
helpviewer_keywords:
- IMetaDataAssemblyImport::EnumAssemblyRefs method [.NET Framework metadata]
- EnumAssemblyRefs method [.NET Framework metadata]
ms.assetid: 8844d0dd-730e-4592-8a7b-c1462d312c70
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0a56d874e5e7ef491c24b0aef2ace700087de677
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447409"
---
# <a name="imetadataassemblyimportenumassemblyrefs-method"></a><span data-ttu-id="4c72c-102">IMetaDataAssemblyImport::EnumAssemblyRefs, méthode</span><span class="sxs-lookup"><span data-stu-id="4c72c-102">IMetaDataAssemblyImport::EnumAssemblyRefs Method</span></span>
<span data-ttu-id="4c72c-103">Énumère les `mdAssemblyRef` instances définies dans le manifeste d’assembly.</span><span class="sxs-lookup"><span data-stu-id="4c72c-103">Enumerates the `mdAssemblyRef` instances that are defined in the assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4c72c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c72c-104">Syntax</span></span>  
  
```  
HRESULT EnumAssemblyRefs (  
    [in, out] HCORENUM        *phEnum,   
    [out]     mdAssemblyRef   rAssemblyRefs[],   
    [in]      ULONG           cMax,   
    [out]     ULONG           *pcTokens  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4c72c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c72c-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="4c72c-106">[dans, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="4c72c-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="4c72c-107">Cela doit être une valeur null lorsque la valeur du `EnumAssemblyRefs` méthode est appelée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="4c72c-107">This must be a null value when the `EnumAssemblyRefs` method is called for the first time.</span></span>  
  
 `rAssemblyRefs`  
 <span data-ttu-id="4c72c-108">[out] L’énumération des `mdAssemblyRef` des jetons de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4c72c-108">[out] The enumeration of `mdAssemblyRef` metadata tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="4c72c-109">[in] Le nombre maximal de jetons qui peuvent être placées dans le `rAssemblyRefs` tableau.</span><span class="sxs-lookup"><span data-stu-id="4c72c-109">[in] The maximum number of tokens that can be placed in the `rAssemblyRefs` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="4c72c-110">[out] Le nombre de jetons placés dans `rAssemblyRefs`.</span><span class="sxs-lookup"><span data-stu-id="4c72c-110">[out] The number of tokens actually placed in `rAssemblyRefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4c72c-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4c72c-111">Return Value</span></span>  
  
|<span data-ttu-id="4c72c-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4c72c-112">HRESULT</span></span>|<span data-ttu-id="4c72c-113">Description</span><span class="sxs-lookup"><span data-stu-id="4c72c-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="4c72c-114">`EnumAssemblyRefs` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="4c72c-114">`EnumAssemblyRefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="4c72c-115">Il n’existe pas de jetons à énumérer.</span><span class="sxs-lookup"><span data-stu-id="4c72c-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="4c72c-116">Dans ce cas, `pcTokens` est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="4c72c-116">In this case, `pcTokens` is set to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4c72c-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4c72c-117">Requirements</span></span>  
 <span data-ttu-id="4c72c-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4c72c-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4c72c-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="4c72c-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="4c72c-120">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4c72c-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="4c72c-121">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4c72c-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c72c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c72c-122">See Also</span></span>  
 [<span data-ttu-id="4c72c-123">IMetaDataAssemblyImport, interface</span><span class="sxs-lookup"><span data-stu-id="4c72c-123">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
