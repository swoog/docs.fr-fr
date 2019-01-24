---
title: ICorProfilerInfo7::ApplyMetaData (méthode)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorProfilerInfo7.ApplyMetaData
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: a1bfb649-4584-4d35-b3e6-8fe59b53992a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7209314f9cf3170ba0b577395a5134f9549475e9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54536566"
---
# <a name="icorprofilerinfo7applymetadata-method"></a><span data-ttu-id="ebe78-102">ICorProfilerInfo7::ApplyMetaData (méthode)</span><span class="sxs-lookup"><span data-stu-id="ebe78-102">ICorProfilerInfo7::ApplyMetaData Method</span></span>
<span data-ttu-id="ebe78-103">[Prise en charge dans le .NET Framework 4.6.1 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="ebe78-103">[Supported in the .NET Framework 4.6.1 and later versions]</span></span>  
  
 <span data-ttu-id="ebe78-104">Applique les métadonnées qui vient d’être définie par le `IMetadataEmit::Define*` méthodes à un module spécifié.</span><span class="sxs-lookup"><span data-stu-id="ebe78-104">Applies the metadata newly defined by the `IMetadataEmit::Define*` methods to a specified module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ebe78-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebe78-105">Syntax</span></span>  
  
```cpp
HRESULT ApplyMetaData(  
        [in] ModuleID moduleID  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ebe78-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebe78-106">Parameters</span></span>  
 `moduleID`  
 <span data-ttu-id="ebe78-107">[in] L’identificateur du module dont les métadonnées a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="ebe78-107">[in] The identifier of the module whose metadata was changed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ebe78-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ebe78-108">Remarks</span></span>  
 <span data-ttu-id="ebe78-109">Si des modifications de métadonnées sont apportées après le [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) rappel, vous devez appeler cette méthode avant d’utiliser les nouvelles métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ebe78-109">If metadata changes are made after the [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) callback, you must call this method before using the new metadata.</span></span>  
  
 <span data-ttu-id="ebe78-110">`ApplyMetaData` prend uniquement en charge l’ajout de types de métadonnées suivants :</span><span class="sxs-lookup"><span data-stu-id="ebe78-110">`ApplyMetaData` only supports adding the following types of metadata:</span></span>  
  
-   <span data-ttu-id="ebe78-111">`AssemblyRef` les enregistrements, vous créez en appelant le [IMetaDataAssemblyEmit::DefineAssemblyRef](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineassemblyref-method.md).</span><span class="sxs-lookup"><span data-stu-id="ebe78-111">`AssemblyRef` records, which you create by calling the [IMetaDataAssemblyEmit::DefineAssemblyRef](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineassemblyref-method.md).</span></span> <span data-ttu-id="ebe78-112">.</span><span class="sxs-lookup"><span data-stu-id="ebe78-112">method.</span></span>  
  
-   <span data-ttu-id="ebe78-113">`TypeRef` les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineTypeRefByName](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definetyperefbyname-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="ebe78-113">`TypeRef` records, which you create by calling the [IMetaDataEmit::DefineTypeRefByName](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definetyperefbyname-method.md) method.</span></span>  
  
-   <span data-ttu-id="ebe78-114">`TypeSpec` les enregistrements, vous créez en appelant le [IMetaDataEmit::GetTokenFromTypeSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromtypespec-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="ebe78-114">`TypeSpec` records, which you create by calling the [IMetaDataEmit::GetTokenFromTypeSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromtypespec-method.md) method.</span></span>  
  
-   <span data-ttu-id="ebe78-115">`MemberRef` les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineMemberRef](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definememberref-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="ebe78-115">`MemberRef` records, which you create by calling the [IMetaDataEmit::DefineMemberRef](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definememberref-method.md) method.</span></span>  
  
-   <span data-ttu-id="ebe78-116">`MemberSpec` les enregistrements, vous créez en appelant le [IMetaDataEmit2::DefineMethodSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definemethodspec-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="ebe78-116">`MemberSpec` records, which you create by calling the [IMetaDataEmit2::DefineMethodSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definemethodspec-method.md) method.</span></span>  
  
-   <span data-ttu-id="ebe78-117">`UserString` les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineUserString](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineuserstring-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="ebe78-117">`UserString` records, which you create by calling the [IMetaDataEmit::DefineUserString](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineuserstring-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ebe78-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ebe78-118">Requirements</span></span>  
 <span data-ttu-id="ebe78-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ebe78-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ebe78-120">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ebe78-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ebe78-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ebe78-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ebe78-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ebe78-122">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebe78-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebe78-123">See also</span></span>
- [<span data-ttu-id="ebe78-124">ICorProfilerInfo7, interface</span><span class="sxs-lookup"><span data-stu-id="ebe78-124">ICorProfilerInfo7 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-interface.md)
