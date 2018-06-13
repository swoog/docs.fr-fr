---
title: IMetaDataDispenser::DefineScope, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataDispenser.DefineScope
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenser::DefineScope
helpviewer_keywords:
- DefineScope method [.NET Framework metadata]
- IMetaDataDispenser::DefineScope method [.NET Framework metadata]
ms.assetid: af28db02-29af-45ac-aec6-8d6c6123c2ff
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 11382f00839917185ba3c85b8fbae5c32d0b0d4a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33448608"
---
# <a name="imetadatadispenserdefinescope-method"></a><span data-ttu-id="a4ba9-102">IMetaDataDispenser::DefineScope, méthode</span><span class="sxs-lookup"><span data-stu-id="a4ba9-102">IMetaDataDispenser::DefineScope Method</span></span>
<span data-ttu-id="a4ba9-103">Crée une zone en mémoire dans laquelle vous pouvez créer des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-103">Creates a new area in memory in which you can create new metadata.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4ba9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4ba9-104">Syntax</span></span>  
  
```  
HRESULT DefineScope (  
    [in]  REFCLSID    rclsid,  
    [in]  DWORD       dwCreateFlags,  
    [in]  REFIID      riid,   
    [out] IUnknown    **ppIUnk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a4ba9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4ba9-105">Parameters</span></span>  
 `rclsid`  
 <span data-ttu-id="a4ba9-106">[in] Le CLSID de la version de structures de métadonnées doit être créé.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-106">[in] The CLSID of the version of metadata structures to be created.</span></span> <span data-ttu-id="a4ba9-107">Cette valeur doit être CLSID_CorMetaDataRuntime pour le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-107">This value must be CLSID_CorMetaDataRuntime for the .NET Framework version 2.0.</span></span>  
  
 `dwCreateFlags`  
 <span data-ttu-id="a4ba9-108">[in] Indicateurs qui spécifient des options.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-108">[in] Flags that specify options.</span></span> <span data-ttu-id="a4ba9-109">Cette valeur doit être zéro pour le .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-109">This value must be zero for the .NET Framework 2.0.</span></span>  
  
 `riid`  
 <span data-ttu-id="a4ba9-110">[in] L’IID de l’interface de métadonnées souhaitée doit être retourné ; l’appelant utilise l’interface pour créer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-110">[in] The IID of the desired metadata interface to be returned; the caller will use the interface to create the new metadata.</span></span>  
  
 <span data-ttu-id="a4ba9-111">La valeur de `riid` doit spécifier l’une des interfaces « émission ».</span><span class="sxs-lookup"><span data-stu-id="a4ba9-111">The value of `riid` must specify one of the "emit" interfaces.</span></span> <span data-ttu-id="a4ba9-112">Les valeurs valides sont IID_IMetaDataEmit, IID_IMetaDataAssemblyEmit ou IID_IMetaDataEmit2.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-112">Valid values are IID_IMetaDataEmit, IID_IMetaDataAssemblyEmit, or IID_IMetaDataEmit2.</span></span>  
  
 `ppIUnk`  
 <span data-ttu-id="a4ba9-113">[out] Pointeur vers l’interface retournée.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-113">[out] The pointer to the returned interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a4ba9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a4ba9-114">Remarks</span></span>  
 <span data-ttu-id="a4ba9-115">`DefineScope` Crée un ensemble de tables de métadonnées en mémoire, génère un GUID unique (identificateur de version de module ou MVID) pour les métadonnées et crée une entrée dans la table de module pour l’unité de compilation qui est émise.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-115">`DefineScope` creates a set of in-memory metadata tables, generates a unique GUID (module version identifier, or MVID) for the metadata, and creates an entry in the module table for the compilation unit being emitted.</span></span>  
  
 <span data-ttu-id="a4ba9-116">Vous pouvez joindre des attributs à la portée de métadonnées en tant qu’ensemble à l’aide de la [IMetaDataEmit::SetModuleProps](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setmoduleprops-method.md) ou [IMetaDataEmit::DefineCustomAttribute](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definecustomattribute-method.md) méthode, comme il convient.</span><span class="sxs-lookup"><span data-stu-id="a4ba9-116">You can attach attributes to the metadata scope as a whole by using the [IMetaDataEmit::SetModuleProps](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setmoduleprops-method.md) or [IMetaDataEmit::DefineCustomAttribute](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definecustomattribute-method.md) method, as appropriate.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a4ba9-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a4ba9-117">Requirements</span></span>  
 <span data-ttu-id="a4ba9-118">**Plateforme :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a4ba9-118">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a4ba9-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a4ba9-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a4ba9-120">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a4ba9-120">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a4ba9-121">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a4ba9-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a4ba9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4ba9-122">See Also</span></span>  
 [<span data-ttu-id="a4ba9-123">IMetaDataDispenser, interface</span><span class="sxs-lookup"><span data-stu-id="a4ba9-123">IMetaDataDispenser Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)  
 [<span data-ttu-id="a4ba9-124">IMetaDataDispenserEx, interface</span><span class="sxs-lookup"><span data-stu-id="a4ba9-124">IMetaDataDispenserEx Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)  
 [<span data-ttu-id="a4ba9-125">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="a4ba9-125">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)  
 [<span data-ttu-id="a4ba9-126">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="a4ba9-126">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="a4ba9-127">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="a4ba9-127">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
