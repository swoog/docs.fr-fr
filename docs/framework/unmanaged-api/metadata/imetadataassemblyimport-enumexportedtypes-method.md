---
title: IMetaDataAssemblyImport::EnumExportedTypes, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.EnumExportedTypes
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::EnumExportedTypes
helpviewer_keywords:
- EnumExportedTypes method [.NET Framework metadata]
- IMetaDataAssemblyImport::EnumExportedTypes method [.NET Framework metadata]
ms.assetid: e5912ed8-e4ce-438b-8ea3-d9e4c288d109
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1c32dcfe5d00e1d35f7c63aa98a33d26f6b179c6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59152683"
---
# <a name="imetadataassemblyimportenumexportedtypes-method"></a><span data-ttu-id="33de2-102">IMetaDataAssemblyImport::EnumExportedTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="33de2-102">IMetaDataAssemblyImport::EnumExportedTypes Method</span></span>
<span data-ttu-id="33de2-103">Énumère les types exportés référencés dans le manifeste d’assembly dans la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="33de2-103">Enumerates the exported types referenced in the assembly manifest in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="33de2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33de2-104">Syntax</span></span>  
  
```  
HRESULT EnumExportedTypes (  
    [in, out] HCORENUM     *phEnum,   
    [out] mdExportedType   rExportedTypes[],   
    [in]  ULONG            cMax,   
    [out] ULONG            *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="33de2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33de2-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="33de2-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="33de2-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="33de2-107">Cela doit être une valeur null valeur lorsque le `EnumExportedTypes` méthode est appelée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="33de2-107">This must be a null value when the `EnumExportedTypes` method is called for the first time.</span></span>  
  
 `rExportedTypes`  
 <span data-ttu-id="33de2-108">[out] L’énumération des `mdExportedType` des jetons de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="33de2-108">[out] The enumeration of `mdExportedType` metadata tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="33de2-109">[in] Le nombre maximal de `mdExportedType` jetons qui peuvent être placés dans le `rExportedTypes` tableau.</span><span class="sxs-lookup"><span data-stu-id="33de2-109">[in] The maximum number of `mdExportedType` tokens that can be placed in the `rExportedTypes` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="33de2-110">[out] Le nombre de `mdExportedType` jetons placés dans `rExportedTypes`.</span><span class="sxs-lookup"><span data-stu-id="33de2-110">[out] The number of `mdExportedType` tokens actually placed in `rExportedTypes`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="33de2-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="33de2-111">Return Value</span></span>  
  
|<span data-ttu-id="33de2-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="33de2-112">HRESULT</span></span>|<span data-ttu-id="33de2-113">Description</span><span class="sxs-lookup"><span data-stu-id="33de2-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|`EnumExportedTypes` <span data-ttu-id="33de2-114">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="33de2-114">returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="33de2-115">Il n’existe pas de jetons à énumérer.</span><span class="sxs-lookup"><span data-stu-id="33de2-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="33de2-116">Dans ce cas, `pcTokens` est défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="33de2-116">In this case, `pcTokens` is set to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="33de2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33de2-117">Requirements</span></span>  
 <span data-ttu-id="33de2-118">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="33de2-118">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="33de2-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="33de2-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="33de2-120">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="33de2-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="33de2-121">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="33de2-121">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="33de2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33de2-122">See also</span></span>

- [<span data-ttu-id="33de2-123">IMetaDataAssemblyImport, interface</span><span class="sxs-lookup"><span data-stu-id="33de2-123">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
