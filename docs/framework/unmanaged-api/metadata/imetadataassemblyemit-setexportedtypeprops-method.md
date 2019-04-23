---
title: IMetaDataAssemblyEmit::SetExportedTypeProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.SetExportedTypeProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::SetExportedTypeProps
helpviewer_keywords:
- SetExportedTypeProps method [.NET Framework metadata]
- IMetaDataAssemblyEmit::SetExportedTypeProps method [.NET Framework metadata]
ms.assetid: 1c090153-fd5f-46c7-9cff-39a78d992c8f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5c09140488730179616d11932faa3542f704958a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59123743"
---
# <a name="imetadataassemblyemitsetexportedtypeprops-method"></a><span data-ttu-id="7b56b-102">IMetaDataAssemblyEmit::SetExportedTypeProps, méthode</span><span class="sxs-lookup"><span data-stu-id="7b56b-102">IMetaDataAssemblyEmit::SetExportedTypeProps Method</span></span>
<span data-ttu-id="7b56b-103">Modifie la structure de métadonnées `ExportedType` spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7b56b-103">Modifies the specified `ExportedType` metadata structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b56b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b56b-104">Syntax</span></span>  
  
```  
HRESULT SetExportedTypeProps (  
    [in] mdExportedType   ct,   
    [in] mdToken          tkImplementation,  
    [in] mdTypeDef        tkTypeDef,  
    [in] DWORD            dwExportedTypeFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7b56b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b56b-105">Parameters</span></span>  
 `ct`  
 <span data-ttu-id="7b56b-106">[in] Le jeton de métadonnées qui spécifie le `ExportedType` structure des métadonnées à modifier.</span><span class="sxs-lookup"><span data-stu-id="7b56b-106">[in] The metadata token that specifies the `ExportedType` metadata structure to be modified.</span></span>  
  
 `tkImplementation`  
 <span data-ttu-id="7b56b-107">[in] Le jeton, de type `File`, `AssemblyRef`, ou `ExportedType`, qui spécifie la façon dont ce type est implémenté.</span><span class="sxs-lookup"><span data-stu-id="7b56b-107">[in] The token, of type `File`, `AssemblyRef`, or `ExportedType`, that specifies how this type is implemented.</span></span>  
  
 `tkTypeDef`  
 <span data-ttu-id="7b56b-108">[in] Le `TypeDef` jeton référencé dans le fichier de code.</span><span class="sxs-lookup"><span data-stu-id="7b56b-108">[in] The `TypeDef` token referenced in the code file.</span></span>  
  
 `dwExportedTypeFlags`  
 <span data-ttu-id="7b56b-109">[in] Combinaison de bits de valeurs qui spécifient les attributs du type.</span><span class="sxs-lookup"><span data-stu-id="7b56b-109">[in] A bitwise combination of values that specify attributes of the type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7b56b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7b56b-110">Remarks</span></span>  
 <span data-ttu-id="7b56b-111">Pour créer un `ExportedType` structure des métadonnées, utilisez le [IMetaDataAssemblyEmit::DefineExportedType](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="7b56b-111">To create an `ExportedType` metadata structure, use the [IMetaDataAssemblyEmit::DefineExportedType](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7b56b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b56b-112">Requirements</span></span>  
 <span data-ttu-id="7b56b-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7b56b-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7b56b-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="7b56b-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="7b56b-115">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7b56b-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="7b56b-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7b56b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b56b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b56b-117">See also</span></span>

- [<span data-ttu-id="7b56b-118">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="7b56b-118">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
