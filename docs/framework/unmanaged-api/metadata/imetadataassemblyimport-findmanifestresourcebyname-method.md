---
title: IMetaDataAssemblyImport::FindManifestResourceByName, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.FindManifestResourceByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::FindManifestResourceByName
helpviewer_keywords:
- FindManifestResourceByName method [.NET Framework metadata]
- IMetaDataAssemblyImport::FindManifestResourceByName method [.NET Framework metadata]
ms.assetid: 7b72fa11-3866-402b-bdea-2b966b77cfe0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8d736a93e7ba6451f1d4755a86749565b9ea071b
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57491514"
---
# <a name="imetadataassemblyimportfindmanifestresourcebyname-method"></a><span data-ttu-id="dccd2-102">IMetaDataAssemblyImport::FindManifestResourceByName, méthode</span><span class="sxs-lookup"><span data-stu-id="dccd2-102">IMetaDataAssemblyImport::FindManifestResourceByName Method</span></span>
<span data-ttu-id="dccd2-103">Obtient un pointeur vers la ressource de manifeste avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="dccd2-103">Gets a pointer to the manifest resource with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dccd2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dccd2-104">Syntax</span></span>  
  
```  
HRESULT FindManifestResourceByName (  
    [in]  LPCWSTR                szName,   
    [out] mdManifestResource     *ptkManifestResource  
);   
```  
  
## <a name="parameters"></a><span data-ttu-id="dccd2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dccd2-105">Parameters</span></span>  
 `szName`  
 <span data-ttu-id="dccd2-106">[in] Le nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="dccd2-106">[in] The name of the resource.</span></span>  
  
 `ptkManifestResource`  
 <span data-ttu-id="dccd2-107">[out] Tableau utilisé pour stocker le `mdManifestResource` des jetons de métadonnées, chacun représentant une ressource de manifeste.</span><span class="sxs-lookup"><span data-stu-id="dccd2-107">[out] The array used to store the `mdManifestResource` metadata tokens, each of which represents a manifest resource.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dccd2-108">Notes</span><span class="sxs-lookup"><span data-stu-id="dccd2-108">Remarks</span></span>  
 <span data-ttu-id="dccd2-109">Le `FindManifestResourceByName` méthode utilise les règles standards employées par le common language runtime pour la résolution des références.</span><span class="sxs-lookup"><span data-stu-id="dccd2-109">The `FindManifestResourceByName` method uses the standard rules employed by the common language runtime for resolving references.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dccd2-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dccd2-110">Requirements</span></span>  
 <span data-ttu-id="dccd2-111">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dccd2-111">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dccd2-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="dccd2-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="dccd2-113">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="dccd2-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="dccd2-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dccd2-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dccd2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dccd2-115">See also</span></span>
- [<span data-ttu-id="dccd2-116">IMetaDataAssemblyImport, interface</span><span class="sxs-lookup"><span data-stu-id="dccd2-116">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
- [<span data-ttu-id="dccd2-117">Méthode de localisation des assemblys par le runtime</span><span class="sxs-lookup"><span data-stu-id="dccd2-117">How the Runtime Locates Assemblies</span></span>](../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
