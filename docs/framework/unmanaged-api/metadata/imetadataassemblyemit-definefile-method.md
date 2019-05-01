---
title: IMetaDataAssemblyEmit::DefineFile, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.DefineFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::DefineFile
helpviewer_keywords:
- IMetaDataAssemblyEmit::DefineFile method [.NET Framework metadata]
- DefineFile method [.NET Framework metadata]
ms.assetid: c065aadf-c1ca-4981-bde6-597042cb29c4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5693da3b5e6d883efd9ad8a5a409a5dba8dd8b6e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62044835"
---
# <a name="imetadataassemblyemitdefinefile-method"></a><span data-ttu-id="e68dc-102">IMetaDataAssemblyEmit::DefineFile, méthode</span><span class="sxs-lookup"><span data-stu-id="e68dc-102">IMetaDataAssemblyEmit::DefineFile Method</span></span>
<span data-ttu-id="e68dc-103">Crée une structure `File` contenant les métadonnées pour l'assembly référencé par cet assembly et retourne le jeton de métadonnées associé.</span><span class="sxs-lookup"><span data-stu-id="e68dc-103">Creates a `File` metadata structure containing metadata for assembly referenced by this assembly, and returns the associated metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e68dc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e68dc-104">Syntax</span></span>  
  
```  
HRESULT DefineFile (  
    [in]  LPCWSTR        szName,   
    [in]  const void     *pbHashValue,   
    [in]  ULONG          cbHashValue,  
    [in]  DWORD          dwFileFlags,  
    [out] mdFile         *pmdf  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e68dc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e68dc-105">Parameters</span></span>  
 `szName`  
 <span data-ttu-id="e68dc-106">[in] Le nom du fichier à être consommés.</span><span class="sxs-lookup"><span data-stu-id="e68dc-106">[in] The name of the file to be consumed.</span></span>  
  
 `pbHashValue`  
 <span data-ttu-id="e68dc-107">[in] Pointeur vers les données de hachage associées à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="e68dc-107">[in] A pointer to the hash data associated with the assembly.</span></span>  
  
 `cbHashValue`  
 <span data-ttu-id="e68dc-108">[in] La taille en octets de `pbHashValue`.</span><span class="sxs-lookup"><span data-stu-id="e68dc-108">[in] The size in bytes of `pbHashValue`.</span></span>  
  
 `dwFileFlags`  
 <span data-ttu-id="e68dc-109">[in] Une combinaison au niveau du bit de `FileFlags` valeurs qui spécifient les paramètres de propriété.</span><span class="sxs-lookup"><span data-stu-id="e68dc-109">[in] A bitwise combination of `FileFlags` values that specify property settings.</span></span>  
  
 `pmdf`  
 <span data-ttu-id="e68dc-110">[out] Un pointeur vers le texte retourné `File` jeton.</span><span class="sxs-lookup"><span data-stu-id="e68dc-110">[out] A pointer to the returned `File` token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e68dc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e68dc-111">Remarks</span></span>  
 <span data-ttu-id="e68dc-112">Un seul `File` structure des métadonnées doit être définie pour chaque fichier qui faisait partie de cet assembly au moment où cet assembly a été généré, à l’exclusion du fichier qui contient les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e68dc-112">One `File` metadata structure must be defined for each file that was part of this assembly at the time that this assembly was built, excluding the file that contains the metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e68dc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e68dc-113">Requirements</span></span>  
 <span data-ttu-id="e68dc-114">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e68dc-114">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e68dc-115">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e68dc-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e68dc-116">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e68dc-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e68dc-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e68dc-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e68dc-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e68dc-118">See also</span></span>

- [<span data-ttu-id="e68dc-119">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="e68dc-119">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
