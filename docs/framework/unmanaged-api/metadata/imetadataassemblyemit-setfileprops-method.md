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
ms.openlocfilehash: 203c31129218be585960e771b1d7e669defd8cde
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743294"
---
# <a name="imetadataassemblyemitsetfileprops-method"></a><span data-ttu-id="8b678-102">IMetaDataAssemblyEmit::SetFileProps, méthode</span><span class="sxs-lookup"><span data-stu-id="8b678-102">IMetaDataAssemblyEmit::SetFileProps Method</span></span>
<span data-ttu-id="8b678-103">Modifie la structure de métadonnées `File` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8b678-103">Modifies the specified `File` metadata structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b678-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b678-104">Syntax</span></span>  
  
```  
HRESULT SetFileProps (  
    [in] mdFile        file,  
    [in] const void    *pbHashValue,   
    [in] ULONG         cbHashValue,  
    [in] DWORD         dwFileFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8b678-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b678-105">Parameters</span></span>  
 `file`  
 <span data-ttu-id="8b678-106">[in] Le jeton de métadonnées qui spécifie le `File` structure des métadonnées à modifier.</span><span class="sxs-lookup"><span data-stu-id="8b678-106">[in] The metadata token that specifies the `File` metadata structure to be modified.</span></span>  
  
 `pbHashValue`  
 <span data-ttu-id="8b678-107">[in] Un pointeur vers les données de hachage associés au fichier.</span><span class="sxs-lookup"><span data-stu-id="8b678-107">[in] A pointer to the hash data associated with the file.</span></span>  
  
 `cbHashValue`  
 <span data-ttu-id="8b678-108">[in] La taille en octets de `pbHashValue`.</span><span class="sxs-lookup"><span data-stu-id="8b678-108">[in] The size in bytes of `pbHashValue`.</span></span>  
  
 `dwFileFlags`  
 <span data-ttu-id="8b678-109">[in] Une combinaison au niveau du bit de [CorFileFlags](../../../../docs/framework/unmanaged-api/metadata/corfileflags-enumeration.md) valeurs qui spécifient différents attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="8b678-109">[in] A bitwise combination of [CorFileFlags](../../../../docs/framework/unmanaged-api/metadata/corfileflags-enumeration.md) values that specify various attributes of the file.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8b678-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8b678-110">Remarks</span></span>  
 <span data-ttu-id="8b678-111">Pour créer un `File` structure des métadonnées, utilisez le [IMetaDataAssemblyEmit::DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="8b678-111">To create a `File` metadata structure, use the [IMetaDataAssemblyEmit::DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8b678-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8b678-112">Requirements</span></span>  
 <span data-ttu-id="8b678-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8b678-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8b678-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="8b678-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8b678-115">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8b678-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="8b678-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8b678-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b678-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b678-117">See also</span></span>
- [<span data-ttu-id="8b678-118">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="8b678-118">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
