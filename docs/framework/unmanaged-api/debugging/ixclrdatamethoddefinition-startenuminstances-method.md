---
title: IXCLRDataMethodDefinition::StartEnumInstances (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition::StartEnumInstances Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition::StartEnumInstances Method
helpviewer.keywords:
- IXCLRDataMethodDefinition::StartEnumInstances Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: c78af112e9239143c4854e34e9b6aa8e99344ec3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54623649"
---
# <a name="ixclrdatamethoddefinitionstartenuminstances-method"></a><span data-ttu-id="282c0-102">IXCLRDataMethodDefinition::StartEnumInstances (méthode)</span><span class="sxs-lookup"><span data-stu-id="282c0-102">IXCLRDataMethodDefinition::StartEnumInstances Method</span></span>

<span data-ttu-id="282c0-103">Fournit un handle pour l’énumération des instances de méthode pour une donnée `IXCLRDataAppDomain`.</span><span class="sxs-lookup"><span data-stu-id="282c0-103">Provides a handle for the enumeration of method instances for a given `IXCLRDataAppDomain`.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="282c0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="282c0-104">Syntax</span></span>

```
HRESULT StartEnumInstances(
    [in] IXCLRDataAppDomain* appDomain,
    [out] CLRDATA_ENUM *handle
);
```

### <a name="parameters"></a><span data-ttu-id="282c0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="282c0-105">Parameters</span></span>

<span data-ttu-id="282c0-106">`appDomain` [in] Un AppDomain pour l’énumération.</span><span class="sxs-lookup"><span data-stu-id="282c0-106">`appDomain` [in] An AppDomain for the enumeration.</span></span>

<span data-ttu-id="282c0-107">`handle` [out] Un handle pour énumérer les instances.</span><span class="sxs-lookup"><span data-stu-id="282c0-107">`handle` [out] A handle for enumerating the instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="282c0-108">Notes</span><span class="sxs-lookup"><span data-stu-id="282c0-108">Remarks</span></span>

<span data-ttu-id="282c0-109">La méthode fournie fait partie de la `IXCLRDataMethodDefinition` interface et correspond à la troisième emplacement de la table de la méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="282c0-109">The provided method is part of the `IXCLRDataMethodDefinition` interface and corresponds to the third slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="282c0-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="282c0-110">Requirements</span></span>

<span data-ttu-id="282c0-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="282c0-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="282c0-112">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="282c0-112">**Header:** None</span></span>  
<span data-ttu-id="282c0-113">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="282c0-113">**Library:** None</span></span>  
<span data-ttu-id="282c0-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="282c0-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="282c0-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="282c0-115">See also</span></span>

- [<span data-ttu-id="282c0-116">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="282c0-116">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="282c0-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="282c0-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="282c0-118">Interface de IXCLRDataMethodDefinition</span><span class="sxs-lookup"><span data-stu-id="282c0-118">IXCLRDataMethodDefinition Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-interface.md)
