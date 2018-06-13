---
title: IMetaDataAssemblyEmit::SetFileProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.SetFileProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::SetFileProps
helpviewer_keywords:
- IMetaDataAssemblyEmit::SetFileProps method [.NET Framework metadata]
- SetFileProps method [.NET Framework metadata]
ms.assetid: 85667d38-611c-45a9-938d-930ac7a7b681
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8017f816632cffc42676761a367e980d1cafe088
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443614"
---
# <a name="imetadataassemblyemitsetfileprops-method"></a><span data-ttu-id="f8d17-102">IMetaDataAssemblyEmit::SetFileProps, méthode</span><span class="sxs-lookup"><span data-stu-id="f8d17-102">IMetaDataAssemblyEmit::SetFileProps Method</span></span>
<span data-ttu-id="f8d17-103">Modifie la structure de métadonnées `File` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8d17-103">Modifies the specified `File` metadata structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8d17-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8d17-104">Syntax</span></span>  
  
```  
HRESULT SetFileProps (  
    [in] mdFile        file,  
    [in] const void    *pbHashValue,   
    [in] ULONG         cbHashValue,  
    [in] DWORD         dwFileFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f8d17-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8d17-105">Parameters</span></span>  
 `file`  
 <span data-ttu-id="f8d17-106">[in] Le jeton de métadonnées qui spécifie le `File` structure de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="f8d17-106">[in] The metadata token that specifies the `File` metadata structure to be modified.</span></span>  
  
 `pbHashValue`  
 <span data-ttu-id="f8d17-107">[in] Pointeur vers les données de hachage associés au fichier.</span><span class="sxs-lookup"><span data-stu-id="f8d17-107">[in] A pointer to the hash data associated with the file.</span></span>  
  
 `cbHashValue`  
 <span data-ttu-id="f8d17-108">[in] La taille en octets de `pbHashValue`.</span><span class="sxs-lookup"><span data-stu-id="f8d17-108">[in] The size in bytes of `pbHashValue`.</span></span>  
  
 `dwFileFlags`  
 <span data-ttu-id="f8d17-109">[in] Une combinaison d’opérations de [CorFileFlags](../../../../docs/framework/unmanaged-api/metadata/corfileflags-enumeration.md) valeurs qui spécifient plusieurs attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="f8d17-109">[in] A bitwise combination of [CorFileFlags](../../../../docs/framework/unmanaged-api/metadata/corfileflags-enumeration.md) values that specify various attributes of the file.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f8d17-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f8d17-110">Remarks</span></span>  
 <span data-ttu-id="f8d17-111">Pour créer un `File` structure des métadonnées, utilisez le [IMetaDataAssemblyEmit::DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="f8d17-111">To create a `File` metadata structure, use the [IMetaDataAssemblyEmit::DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f8d17-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f8d17-112">Requirements</span></span>  
 <span data-ttu-id="f8d17-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f8d17-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f8d17-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="f8d17-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f8d17-115">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f8d17-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f8d17-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f8d17-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8d17-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8d17-117">See Also</span></span>  
 [<span data-ttu-id="f8d17-118">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="f8d17-118">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
