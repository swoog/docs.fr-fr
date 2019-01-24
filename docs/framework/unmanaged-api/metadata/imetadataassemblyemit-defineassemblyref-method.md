---
title: IMetaDataAssemblyEmit::DefineAssemblyRef, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.DefineAssemblyRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::DefineAssemblyRef
helpviewer_keywords:
- DefineAssemblyRef method [.NET Framework metadata]
- IMetaDataAssemblyEmit::DefineAssemblyRef method [.NET Framework metadata]
ms.assetid: 0b284b18-0084-4b3a-912a-5ebe9f29c88b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f82fca1d7701921a10c1feb9cce19371729ff01e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54493468"
---
# <a name="imetadataassemblyemitdefineassemblyref-method"></a><span data-ttu-id="824aa-102">IMetaDataAssemblyEmit::DefineAssemblyRef, méthode</span><span class="sxs-lookup"><span data-stu-id="824aa-102">IMetaDataAssemblyEmit::DefineAssemblyRef Method</span></span>
<span data-ttu-id="824aa-103">Crée une structure `AssemblyRef` contenant les métadonnées pour l'assembly que cet assembly référence et retourne le jeton de métadonnées associé.</span><span class="sxs-lookup"><span data-stu-id="824aa-103">Creates an `AssemblyRef` structure containing metadata for the assembly that this assembly references, and returns the associated metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="824aa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="824aa-104">Syntax</span></span>  
  
```  
HRESULT DefineAssemblyRef (  
    [in]  void                *pbPublicKeyOrToken,  
    [in]  ULONG               cbPublicKeyOrToken,  
    [in]  LPCWSTR             szName,  
    [in]  ASSEMBLYMETADATA    pMetaData,  
    [in]  void                *pbHashValue,  
    [in]  ULONG               cbHashValue,  
    [in]  DWORD               dwAssemblyRefFlags,  
    [out] mdAssemblyRef       *pmdar  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="824aa-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="824aa-105">Parameters</span></span>  
 `pbPublicKeyOrToken`  
 <span data-ttu-id="824aa-106">[in] La clé publique du serveur de publication de l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="824aa-106">[in] The public key of the publisher of the referenced assembly.</span></span> <span data-ttu-id="824aa-107">La fonction d’assistance [StrongNameTokenFromAssembly](../../../../docs/framework/unmanaged-api/strong-naming/strongnametokenfromassembly-function.md) peut être utilisée pour obtenir le hachage de la clé publique à passer comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="824aa-107">The helper function [StrongNameTokenFromAssembly](../../../../docs/framework/unmanaged-api/strong-naming/strongnametokenfromassembly-function.md) can be used to get the hash of the public key to pass as this parameter.</span></span>  
  
 `cbPublicKeyOrToken`  
 <span data-ttu-id="824aa-108">[in] La taille en octets de `pbPublicKeyOrToken`.</span><span class="sxs-lookup"><span data-stu-id="824aa-108">[in] The size in bytes of `pbPublicKeyOrToken`.</span></span>  
  
 `szName`  
 <span data-ttu-id="824aa-109">[in] Le nom lisible de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="824aa-109">[in] The human-readable text name of the assembly.</span></span> <span data-ttu-id="824aa-110">Cette valeur ne doit pas dépasser 1 024 caractères.</span><span class="sxs-lookup"><span data-stu-id="824aa-110">This value must not exceed 1024 characters.</span></span>  
  
 `pMetaData`  
 <span data-ttu-id="824aa-111">[in] Instance ASSEMBLYMETADATA qui contient les informations de version, la plateforme et aux paramètres régionaux de l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="824aa-111">[in] An ASSEMBLYMETADATA instance that contains the version, platform and locale information of the referenced assembly.</span></span>  
  
 `pbHashValue`  
 <span data-ttu-id="824aa-112">[in] Les données de hachage associées à l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="824aa-112">[in] The hash data associated with the referenced assembly.</span></span> <span data-ttu-id="824aa-113">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="824aa-113">Optional.</span></span>  
  
 `cbHashValue`  
 <span data-ttu-id="824aa-114">[in] La taille en octets de `pbHashValue`.</span><span class="sxs-lookup"><span data-stu-id="824aa-114">[in] The size in bytes of `pbHashValue`.</span></span>  
  
 `dwAssemblyRefFlags`  
 <span data-ttu-id="824aa-115">[in] Une combinaison au niveau du bit de [CorAssemblyFlags](../../../../docs/framework/unmanaged-api/metadata/corassemblyflags-enumeration.md) valeurs qui influencent le comportement du moteur d’exécution.</span><span class="sxs-lookup"><span data-stu-id="824aa-115">[in] A bitwise combination of [CorAssemblyFlags](../../../../docs/framework/unmanaged-api/metadata/corassemblyflags-enumeration.md) values that influence the behavior of the execution engine.</span></span>  
  
 `pmdar`  
 <span data-ttu-id="824aa-116">[out] Un pointeur vers le texte retourné `AssemblyRef` jeton de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="824aa-116">[out] A pointer to the returned `AssemblyRef` metadata token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="824aa-117">Notes</span><span class="sxs-lookup"><span data-stu-id="824aa-117">Remarks</span></span>  
 <span data-ttu-id="824aa-118">Un seul `AssemblyRef` structure des métadonnées doit être définie pour chaque assembly qui fait référence à cet assembly.</span><span class="sxs-lookup"><span data-stu-id="824aa-118">One `AssemblyRef` metadata structure must be defined for each assembly that this assembly references.</span></span>  
  
 <span data-ttu-id="824aa-119">Au moment de l’exécution, les détails d’un assembly référencé sont passés à la résolution d’assembly avec une indication qu’ils représentent les informations « comme générée. ».</span><span class="sxs-lookup"><span data-stu-id="824aa-119">At run time, the details of a referenced assembly are passed to the assembly resolver with an indication that they represent the "as built" information.</span></span> <span data-ttu-id="824aa-120">Le programme de résolution d’assembly applique ensuite la stratégie.</span><span class="sxs-lookup"><span data-stu-id="824aa-120">The assembly resolver then applies policy.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="824aa-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="824aa-121">Requirements</span></span>  
 <span data-ttu-id="824aa-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="824aa-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="824aa-123">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="824aa-123">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="824aa-124">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="824aa-124">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="824aa-125">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="824aa-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="824aa-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="824aa-126">See also</span></span>
- [<span data-ttu-id="824aa-127">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="824aa-127">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
