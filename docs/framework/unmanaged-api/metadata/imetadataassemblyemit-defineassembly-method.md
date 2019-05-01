---
title: IMetaDataAssemblyEmit::DefineAssembly, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.DefineAssembly
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::DefineAssembly
helpviewer_keywords:
- IMetaDataAssemblyEmit::DefineAssembly method [.NET Framework metadata]
- DefineAssembly method [.NET Framework metadata]
ms.assetid: a0637d66-74bf-4f2d-8137-9ff838bccece
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b95a583aec87e3ba3e247d1ef800302b62657837
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62044822"
---
# <a name="imetadataassemblyemitdefineassembly-method"></a><span data-ttu-id="fed49-102">IMetaDataAssemblyEmit::DefineAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="fed49-102">IMetaDataAssemblyEmit::DefineAssembly Method</span></span>
<span data-ttu-id="fed49-103">Crée un `Assembly` de structure qui contient les métadonnées pour l’assembly spécifié et retourne le jeton de métadonnées associé.</span><span class="sxs-lookup"><span data-stu-id="fed49-103">Creates an `Assembly` structure containing metadata for the specified assembly and returns the associated metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fed49-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fed49-104">Syntax</span></span>  
  
```  
HRESULT DefineAssembly (  
    [in]  void                 *pbPublicKey,  
    [in]  ULONG                cbPublicKey,  
    [in]  ULONG                uHashAlgId,  
    [in]  LPCWSTR              szName,   
    [in]  ASSEMBLYMETADATA     *pMetaData,  
    [in]  DWORD                dwAssemblyFlags,  
    [out] mdAssembly           *pmda  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fed49-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fed49-105">Parameters</span></span>  
 `pbPublicKey`  
 <span data-ttu-id="fed49-106">[in] La clé publique qui identifie l’éditeur de l’assembly, ou NULL si l’assembly n'est pas un nom fort.</span><span class="sxs-lookup"><span data-stu-id="fed49-106">[in] The public key that identifies the publisher of the assembly, or NULL if the assembly is not strongly named.</span></span>  
  
 `cbPublicKey`  
 <span data-ttu-id="fed49-107">[in] La taille en octets de `pbPublicKey`.</span><span class="sxs-lookup"><span data-stu-id="fed49-107">[in] The size in bytes of `pbPublicKey`.</span></span>  
  
 `uHashAlgId`  
 <span data-ttu-id="fed49-108">[in] Identificateur de l’algorithme de hachage à utiliser pour chiffrer les fichiers dans l’assembly, ou NULL pour spécifier l’algorithme SHA-1.</span><span class="sxs-lookup"><span data-stu-id="fed49-108">[in] The identifier of the hashing algorithm to use to encrypt the files in the assembly, or NULL to specify the SHA-1 algorithm.</span></span>  
  
 `szName`  
 <span data-ttu-id="fed49-109">[in] Le nom lisible de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="fed49-109">[in] The human-readable text name of the assembly.</span></span> <span data-ttu-id="fed49-110">Cette valeur ne doit pas dépasser 1 024 caractères.</span><span class="sxs-lookup"><span data-stu-id="fed49-110">This value must not exceed 1024 characters.</span></span>  
  
 `pMetaData`  
 <span data-ttu-id="fed49-111">[in] Pointeur vers une instance ASSEMBLYMETADATA qui contient les informations de version, la plateforme et aux paramètres régionaux de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="fed49-111">[in] A pointer to an ASSEMBLYMETADATA instance that contains the version, platform, and locale information for the assembly.</span></span>  
  
 `dwAssemblyFlags`  
 <span data-ttu-id="fed49-112">[in] Une combinaison de [CorAssemblyFlags](../../../../docs/framework/unmanaged-api/metadata/corassemblyflags-enumeration.md) valeurs qui décrivent les fonctionnalités de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="fed49-112">[in] A combination of [CorAssemblyFlags](../../../../docs/framework/unmanaged-api/metadata/corassemblyflags-enumeration.md) values that describe features of the assembly.</span></span>  
  
 `pmda`  
 <span data-ttu-id="fed49-113">[out] Pointeur vers le jeton de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="fed49-113">[out] A pointer to the metadata token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fed49-114">Notes</span><span class="sxs-lookup"><span data-stu-id="fed49-114">Remarks</span></span>  
 <span data-ttu-id="fed49-115">Seul `Assembly` structure des métadonnées peut être défini dans un manifeste.</span><span class="sxs-lookup"><span data-stu-id="fed49-115">Only one `Assembly` metadata structure can be defined within a manifest.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fed49-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fed49-116">Requirements</span></span>  
 <span data-ttu-id="fed49-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fed49-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fed49-118">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="fed49-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="fed49-119">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fed49-119">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="fed49-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fed49-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fed49-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fed49-121">See also</span></span>

- [<span data-ttu-id="fed49-122">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="fed49-122">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
