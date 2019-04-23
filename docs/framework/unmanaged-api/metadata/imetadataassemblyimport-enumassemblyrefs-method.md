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
ms.openlocfilehash: 91e253669b9f51e7c1d600ba11f13a9ce67fb58a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59072478"
---
# <a name="imetadataassemblyimportenumassemblyrefs-method"></a><span data-ttu-id="4ee0e-102">IMetaDataAssemblyImport::EnumAssemblyRefs, méthode</span><span class="sxs-lookup"><span data-stu-id="4ee0e-102">IMetaDataAssemblyImport::EnumAssemblyRefs Method</span></span>
<span data-ttu-id="4ee0e-103">Énumère les `mdAssemblyRef` instances qui sont définis dans le manifeste d’assembly.</span><span class="sxs-lookup"><span data-stu-id="4ee0e-103">Enumerates the `mdAssemblyRef` instances that are defined in the assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ee0e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ee0e-104">Syntax</span></span>  
  
```  
HRESULT EnumAssemblyRefs (  
    [in, out] HCORENUM        *phEnum,   
    [out]     mdAssemblyRef   rAssemblyRefs[],   
    [in]      ULONG           cMax,   
    [out]     ULONG           *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4ee0e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ee0e-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="4ee0e-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="4ee0e-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="4ee0e-107">Cela doit être une valeur null valeur lorsque le `EnumAssemblyRefs` méthode est appelée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="4ee0e-107">This must be a null value when the `EnumAssemblyRefs` method is called for the first time.</span></span>  
  
 `rAssemblyRefs`  
 <span data-ttu-id="4ee0e-108">[out] L’énumération des `mdAssemblyRef` des jetons de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="4ee0e-108">[out] The enumeration of `mdAssemblyRef` metadata tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="4ee0e-109">[in] Le nombre maximal de jetons qui peuvent être placés dans le `rAssemblyRefs` tableau.</span><span class="sxs-lookup"><span data-stu-id="4ee0e-109">[in] The maximum number of tokens that can be placed in the `rAssemblyRefs` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="4ee0e-110">[out] Le nombre de jetons placés dans `rAssemblyRefs`.</span><span class="sxs-lookup"><span data-stu-id="4ee0e-110">[out] The number of tokens actually placed in `rAssemblyRefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4ee0e-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4ee0e-111">Return Value</span></span>  
  
|<span data-ttu-id="4ee0e-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4ee0e-112">HRESULT</span></span>|<span data-ttu-id="4ee0e-113">Description</span><span class="sxs-lookup"><span data-stu-id="4ee0e-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="4ee0e-114">`EnumAssemblyRefs` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="4ee0e-114">`EnumAssemblyRefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="4ee0e-115">Il n’existe pas de jetons à énumérer.</span><span class="sxs-lookup"><span data-stu-id="4ee0e-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="4ee0e-116">Dans ce cas, `pcTokens` est défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="4ee0e-116">In this case, `pcTokens` is set to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4ee0e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ee0e-117">Requirements</span></span>  
 <span data-ttu-id="4ee0e-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4ee0e-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4ee0e-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="4ee0e-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="4ee0e-120">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4ee0e-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="4ee0e-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4ee0e-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ee0e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ee0e-122">See also</span></span>

- [<span data-ttu-id="4ee0e-123">IMetaDataAssemblyImport, interface</span><span class="sxs-lookup"><span data-stu-id="4ee0e-123">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
