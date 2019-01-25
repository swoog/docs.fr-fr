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
ms.openlocfilehash: b05c9a75bf870dd3b2316d2df7c50932b26894f3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702741"
---
# <a name="imetadataassemblyimportfindmanifestresourcebyname-method"></a><span data-ttu-id="d195b-102">IMetaDataAssemblyImport::FindManifestResourceByName, méthode</span><span class="sxs-lookup"><span data-stu-id="d195b-102">IMetaDataAssemblyImport::FindManifestResourceByName Method</span></span>
<span data-ttu-id="d195b-103">Obtient un pointeur vers la ressource de manifeste avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="d195b-103">Gets a pointer to the manifest resource with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d195b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d195b-104">Syntax</span></span>  
  
```  
HRESULT FindManifestResourceByName (  
    [in]  LPCWSTR                szName,   
    [out] mdManifestResource     *ptkManifestResource  
);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="d195b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d195b-105">Parameters</span></span>  
 `szName`  
 <span data-ttu-id="d195b-106">[in] Le nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="d195b-106">[in] The name of the resource.</span></span>  
  
 `ptkManifestResource`  
 <span data-ttu-id="d195b-107">[out] Tableau utilisé pour stocker le `mdManifestResource` des jetons de métadonnées, chacun représentant une ressource de manifeste.</span><span class="sxs-lookup"><span data-stu-id="d195b-107">[out] The array used to store the `mdManifestResource` metadata tokens, each of which represents a manifest resource.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d195b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d195b-108">Remarks</span></span>  
 <span data-ttu-id="d195b-109">Le `FindManifestResourceByName` méthode utilise les règles standards employées par le common language runtime pour la résolution des références.</span><span class="sxs-lookup"><span data-stu-id="d195b-109">The `FindManifestResourceByName` method uses the standard rules employed by the common language runtime for resolving references.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d195b-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d195b-110">Requirements</span></span>  
 <span data-ttu-id="d195b-111">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d195b-111">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d195b-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="d195b-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d195b-113">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d195b-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d195b-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d195b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d195b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d195b-115">See also</span></span>
- [<span data-ttu-id="d195b-116">IMetaDataAssemblyImport, interface</span><span class="sxs-lookup"><span data-stu-id="d195b-116">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
- [<span data-ttu-id="d195b-117">Méthode de localisation des assemblys par le runtime</span><span class="sxs-lookup"><span data-stu-id="d195b-117">How the Runtime Locates Assemblies</span></span>](../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
