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
ms.openlocfilehash: bf61da362251577acadb83915404eba7508b3099
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59141568"
---
# <a name="imetadataassemblyimportfindmanifestresourcebyname-method"></a><span data-ttu-id="cdcfe-102">IMetaDataAssemblyImport::FindManifestResourceByName, méthode</span><span class="sxs-lookup"><span data-stu-id="cdcfe-102">IMetaDataAssemblyImport::FindManifestResourceByName Method</span></span>
<span data-ttu-id="cdcfe-103">Obtient un pointeur vers la ressource de manifeste avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="cdcfe-103">Gets a pointer to the manifest resource with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cdcfe-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdcfe-104">Syntax</span></span>  
  
```  
HRESULT FindManifestResourceByName (  
    [in]  LPCWSTR                szName,   
    [out] mdManifestResource     *ptkManifestResource  
);   
```  
  
## <a name="parameters"></a><span data-ttu-id="cdcfe-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdcfe-105">Parameters</span></span>  
 `szName`  
 <span data-ttu-id="cdcfe-106">[in] Le nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="cdcfe-106">[in] The name of the resource.</span></span>  
  
 `ptkManifestResource`  
 <span data-ttu-id="cdcfe-107">[out] Tableau utilisé pour stocker le `mdManifestResource` des jetons de métadonnées, chacun représentant une ressource de manifeste.</span><span class="sxs-lookup"><span data-stu-id="cdcfe-107">[out] The array used to store the `mdManifestResource` metadata tokens, each of which represents a manifest resource.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cdcfe-108">Notes</span><span class="sxs-lookup"><span data-stu-id="cdcfe-108">Remarks</span></span>  
 <span data-ttu-id="cdcfe-109">Le `FindManifestResourceByName` méthode utilise les règles standards employées par le common language runtime pour la résolution des références.</span><span class="sxs-lookup"><span data-stu-id="cdcfe-109">The `FindManifestResourceByName` method uses the standard rules employed by the common language runtime for resolving references.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cdcfe-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdcfe-110">Requirements</span></span>  
 <span data-ttu-id="cdcfe-111">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cdcfe-111">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cdcfe-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="cdcfe-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="cdcfe-113">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cdcfe-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="cdcfe-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="cdcfe-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="cdcfe-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdcfe-115">See also</span></span>

- [<span data-ttu-id="cdcfe-116">IMetaDataAssemblyImport, interface</span><span class="sxs-lookup"><span data-stu-id="cdcfe-116">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
- [<span data-ttu-id="cdcfe-117">Méthode de localisation des assemblys par le runtime</span><span class="sxs-lookup"><span data-stu-id="cdcfe-117">How the Runtime Locates Assemblies</span></span>](../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
