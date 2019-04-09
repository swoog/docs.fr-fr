---
title: IMetaDataAssemblyImport::EnumFiles, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.EnumFiles
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::EnumFiles
helpviewer_keywords:
- IMetaDataAssemblyImport::EnumFiles method [.NET Framework metadata]
- EnumFiles method [.NET Framework metadata]
ms.assetid: f0d721e2-b946-426d-8e20-9124bd04e4cb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b2ab06419491093a2de41d2ef25d16c01c03ebaf
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59158845"
---
# <a name="imetadataassemblyimportenumfiles-method"></a><span data-ttu-id="282bb-102">IMetaDataAssemblyImport::EnumFiles, méthode</span><span class="sxs-lookup"><span data-stu-id="282bb-102">IMetaDataAssemblyImport::EnumFiles Method</span></span>
<span data-ttu-id="282bb-103">Énumère les fichiers référencés dans le manifeste d’assembly actuel.</span><span class="sxs-lookup"><span data-stu-id="282bb-103">Enumerates the files referenced in the current assembly manifest.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="282bb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="282bb-104">Syntax</span></span>  
  
```  
HRESULT EnumFiles (  
    [in, out] HCORENUM    *phEnum,   
    [out] mdFile          rFiles[],   
    [in]  ULONG           cMax,   
    [out] ULONG           *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="282bb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="282bb-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="282bb-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="282bb-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="282bb-107">Cela doit être une valeur null pour le premier appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="282bb-107">This must be a null value for the first call of this method.</span></span>  
  
 `rFiles`  
 <span data-ttu-id="282bb-108">[out] Tableau utilisé pour stocker le `mdFile` des jetons de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="282bb-108">[out] The array used to store the `mdFile` metadata tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="282bb-109">[in] Le nombre maximal de `mdFile` jetons qui peuvent être placés dans `rFiles`.</span><span class="sxs-lookup"><span data-stu-id="282bb-109">[in] The maximum number of `mdFile` tokens that can be placed in `rFiles`.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="282bb-110">[out] Le nombre de `mdFile` jetons placés dans `rFiles`.</span><span class="sxs-lookup"><span data-stu-id="282bb-110">[out] The number of `mdFile` tokens actually placed in `rFiles`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="282bb-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="282bb-111">Return Value</span></span>  
  
|<span data-ttu-id="282bb-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="282bb-112">HRESULT</span></span>|<span data-ttu-id="282bb-113">Description</span><span class="sxs-lookup"><span data-stu-id="282bb-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|`EnumFiles` <span data-ttu-id="282bb-114">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="282bb-114">returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="282bb-115">Il n’existe pas de jetons à énumérer.</span><span class="sxs-lookup"><span data-stu-id="282bb-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="282bb-116">Dans ce cas, `pcTokens` est défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="282bb-116">In this case, `pcTokens` is set to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="282bb-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="282bb-117">Requirements</span></span>  
 <span data-ttu-id="282bb-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="282bb-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="282bb-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="282bb-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="282bb-120">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="282bb-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="282bb-121">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="282bb-121">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="282bb-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="282bb-122">See also</span></span>

- [<span data-ttu-id="282bb-123">IMetaDataAssemblyImport, interface</span><span class="sxs-lookup"><span data-stu-id="282bb-123">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
