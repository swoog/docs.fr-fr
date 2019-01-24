---
title: IXCLRDataProcess::StartEnumModules (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::StartEnumModules Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::StartEnumModules Method
helpviewer.keywords:
- IXCLRDataProcess::StartEnumModules Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 4a086157b27b7426cb6d5f17f13426c0f26d2b2d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54658219"
---
# <a name="ixclrdataprocessstartenummodules-method"></a><span data-ttu-id="93018-102">IXCLRDataProcess::StartEnumModules (méthode)</span><span class="sxs-lookup"><span data-stu-id="93018-102">IXCLRDataProcess::StartEnumModules Method</span></span>

<span data-ttu-id="93018-103">Fournit un handle pour énumérer les modules d’un processus.</span><span class="sxs-lookup"><span data-stu-id="93018-103">Provides a handle to enumerate the modules of a process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="93018-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93018-104">Syntax</span></span>

```
HRESULT StartEnumModules(
    [out] CLRDATA_ENUM *handle
);
```

### <a name="parameters"></a><span data-ttu-id="93018-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93018-105">Parameters</span></span>

<span data-ttu-id="93018-106">`handle` [out] Un handle pour énumérer les modules.</span><span class="sxs-lookup"><span data-stu-id="93018-106">`handle` [out] A handle for enumerating the modules.</span></span>

## <a name="remarks"></a><span data-ttu-id="93018-107">Notes</span><span class="sxs-lookup"><span data-stu-id="93018-107">Remarks</span></span>

<span data-ttu-id="93018-108">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 24.</span><span class="sxs-lookup"><span data-stu-id="93018-108">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 24th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="93018-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="93018-109">Requirements</span></span>

<span data-ttu-id="93018-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="93018-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="93018-111">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="93018-111">**Header:** None</span></span>  
<span data-ttu-id="93018-112">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="93018-112">**Library:** None</span></span>  
<span data-ttu-id="93018-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="93018-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="93018-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93018-114">See also</span></span>

- [<span data-ttu-id="93018-115">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="93018-115">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="93018-116">Débogage</span><span class="sxs-lookup"><span data-stu-id="93018-116">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="93018-117">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="93018-117">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
