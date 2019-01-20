---
title: IXCLRDataMethodDefinition::EndEnumInstances (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition::EndEnumInstances Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition::EndEnumInstances Method
helpviewer.keywords:
- IXCLRDataMethodDefinition::EndEnumInstances Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 7901ba3ac95052e265df619d06996b4c9ce8baa6
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416399"
---
# <a name="ixclrdatamethoddefinitionendenuminstances-method"></a><span data-ttu-id="5c131-102">IXCLRDataMethodDefinition::EndEnumInstances (méthode)</span><span class="sxs-lookup"><span data-stu-id="5c131-102">IXCLRDataMethodDefinition::EndEnumInstances Method</span></span>

<span data-ttu-id="5c131-103">Libère les ressources utilisées par les itérateurs internes utilisés pendant l’énumération de l’instance.</span><span class="sxs-lookup"><span data-stu-id="5c131-103">Releases the resources used by internal iterators used during instance enumeration.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="5c131-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c131-104">Syntax</span></span>

```
HRESULT EndEnumInstances(
    [in] CLRDATA_ENUM handle
);
```

### <a name="parameters"></a><span data-ttu-id="5c131-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c131-105">Parameters</span></span>

<span data-ttu-id="5c131-106">`handle` [out] Un handle pour énumérer les instances.</span><span class="sxs-lookup"><span data-stu-id="5c131-106">`handle` [out] A handle for enumerating the instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c131-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5c131-107">Remarks</span></span>

<span data-ttu-id="5c131-108">La méthode fournie fait partie de la `IXCLRDataMethodDefinition` interface et correspond à l’emplacement de cinquième de la table de la méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5c131-108">The provided method is part of the `IXCLRDataMethodDefinition` interface and corresponds to the fifth slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c131-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5c131-109">Requirements</span></span>

<span data-ttu-id="5c131-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5c131-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="5c131-111">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="5c131-111">**Header:** None</span></span>  
<span data-ttu-id="5c131-112">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="5c131-112">**Library:** None</span></span>  
<span data-ttu-id="5c131-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="5c131-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="5c131-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c131-114">See Also</span></span>

- [<span data-ttu-id="5c131-115">Débogage</span><span class="sxs-lookup"><span data-stu-id="5c131-115">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="5c131-116">Interface de IXCLRDataMethodDefinition</span><span class="sxs-lookup"><span data-stu-id="5c131-116">IXCLRDataMethodDefinition Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-interface.md)
