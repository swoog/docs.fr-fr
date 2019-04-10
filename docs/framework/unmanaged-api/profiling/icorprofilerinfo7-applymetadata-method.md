---
title: ICorProfilerInfo7::ApplyMetaData (méthode)
ms.date: 02/15/2019
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
ms.openlocfilehash: aff6f63bb9f41fe45b22854787667070929bf987
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59213764"
---
# <a name="icorprofilerinfo7applymetadata-method"></a><span data-ttu-id="27b08-102">ICorProfilerInfo7::ApplyMetaData (méthode)</span><span class="sxs-lookup"><span data-stu-id="27b08-102">ICorProfilerInfo7::ApplyMetaData Method</span></span>
<span data-ttu-id="27b08-103">[Prise en charge dans le .NET Framework 4.6.1 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="27b08-103">[Supported in the .NET Framework 4.6.1 and later versions]</span></span>  
  
 <span data-ttu-id="27b08-104">Applique les métadonnées qui vient d’être définie par le `IMetadataEmit::Define*` méthodes à un module spécifié.</span><span class="sxs-lookup"><span data-stu-id="27b08-104">Applies the metadata newly defined by the `IMetadataEmit::Define*` methods to a specified module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="27b08-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27b08-105">Syntax</span></span>  
  
```cpp
HRESULT ApplyMetaData(  
        [in] ModuleID moduleID  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="27b08-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27b08-106">Parameters</span></span>  
 `moduleID`  
 <span data-ttu-id="27b08-107">[in] L’identificateur du module dont les métadonnées a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="27b08-107">[in] The identifier of the module whose metadata was changed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="27b08-108">Notes</span><span class="sxs-lookup"><span data-stu-id="27b08-108">Remarks</span></span>  
 <span data-ttu-id="27b08-109">Si des modifications de métadonnées sont apportées après le [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) rappel, vous devez appeler cette méthode avant d’utiliser les nouvelles métadonnées.</span><span class="sxs-lookup"><span data-stu-id="27b08-109">If metadata changes are made after the [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) callback, you must call this method before using the new metadata.</span></span>  
  
 `ApplyMetaData` <span data-ttu-id="27b08-110">prend uniquement en charge l’ajout de types de métadonnées suivants :</span><span class="sxs-lookup"><span data-stu-id="27b08-110">only supports adding the following types of metadata:</span></span>  
  
-   `AssemblyRef` <span data-ttu-id="27b08-111">les enregistrements, vous créez en appelant le [IMetaDataAssemblyEmit::DefineAssemblyRef](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineassemblyref-method.md).</span><span class="sxs-lookup"><span data-stu-id="27b08-111">records, which you create by calling the [IMetaDataAssemblyEmit::DefineAssemblyRef](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineassemblyref-method.md).</span></span> <span data-ttu-id="27b08-112">.</span><span class="sxs-lookup"><span data-stu-id="27b08-112">method.</span></span>  
  
-   `TypeRef` <span data-ttu-id="27b08-113">les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineTypeRefByName](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definetyperefbyname-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="27b08-113">records, which you create by calling the [IMetaDataEmit::DefineTypeRefByName](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definetyperefbyname-method.md) method.</span></span>  
  
-   `TypeSpec` <span data-ttu-id="27b08-114">les enregistrements, vous créez en appelant le [IMetaDataEmit::GetTokenFromTypeSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromtypespec-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="27b08-114">records, which you create by calling the [IMetaDataEmit::GetTokenFromTypeSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromtypespec-method.md) method.</span></span>  
  
-   `MemberRef` <span data-ttu-id="27b08-115">les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineMemberRef](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definememberref-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="27b08-115">records, which you create by calling the [IMetaDataEmit::DefineMemberRef](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definememberref-method.md) method.</span></span>  
  
-   `MemberSpec` <span data-ttu-id="27b08-116">les enregistrements, vous créez en appelant le [IMetaDataEmit2::DefineMethodSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definemethodspec-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="27b08-116">records, which you create by calling the [IMetaDataEmit2::DefineMethodSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definemethodspec-method.md) method.</span></span>  
  
-   `UserString` <span data-ttu-id="27b08-117">les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineUserString](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineuserstring-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="27b08-117">records, which you create by calling the [IMetaDataEmit::DefineUserString](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineuserstring-method.md) method.</span></span>  

<span data-ttu-id="27b08-118">En commençant par .NET Core 3.0, `ApplyMetaData` prend également en charge les types suivants :</span><span class="sxs-lookup"><span data-stu-id="27b08-118">Starting with .NET Core 3.0, `ApplyMetaData` also supports the following types:</span></span>

- `TypeDef` <span data-ttu-id="27b08-119">les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineTypeDef](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definetypedef-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="27b08-119">records, which you create by calling the [IMetaDataEmit::DefineTypeDef](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definetypedef-method.md) method.</span></span>

- `MethodDef` <span data-ttu-id="27b08-120">les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineMethod](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definemethod-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="27b08-120">records, which you create by calling the [IMetaDataEmit::DefineMethod](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definemethod-method.md) method.</span></span> <span data-ttu-id="27b08-121">Toutefois, l’ajout de méthodes virtuelles à un type existant n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="27b08-121">However, adding virtual methods to an existing type is not supported.</span></span> <span data-ttu-id="27b08-122">Méthodes virtuelles doivent être ajoutés avant le [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="27b08-122">Virtual methods must be added before the [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="27b08-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27b08-123">Requirements</span></span>  
 <span data-ttu-id="27b08-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="27b08-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="27b08-125">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="27b08-125">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="27b08-126">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="27b08-126">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="27b08-127">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="27b08-127">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="27b08-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27b08-128">See also</span></span>

- [<span data-ttu-id="27b08-129">ICorProfilerInfo7, interface</span><span class="sxs-lookup"><span data-stu-id="27b08-129">ICorProfilerInfo7 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-interface.md)
