---
title: IXCLRDataProcess::EnumModule (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumModule Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumModule Method
helpviewer.keywords:
- IXCLRDataProcess::EnumModule Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: fa1e41985444324627c6b66a109b4619d85fc57f
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416460"
---
# <a name="ixclrdataprocessenummodule-method"></a><span data-ttu-id="7ee36-102">IXCLRDataProcess::EnumModule (méthode)</span><span class="sxs-lookup"><span data-stu-id="7ee36-102">IXCLRDataProcess::EnumModule Method</span></span>

<span data-ttu-id="7ee36-103">Énumère les modules de ce processus.</span><span class="sxs-lookup"><span data-stu-id="7ee36-103">Enumerates the modules of this process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="7ee36-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ee36-104">Syntax</span></span>

```
HRESULT EnumModule(
    [in, out] CLRDATA_ENUM  *handle,
    [out] IXCLRDataModule  **mod
);
```

### <a name="parameters"></a><span data-ttu-id="7ee36-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ee36-105">Parameters</span></span>

<span data-ttu-id="7ee36-106">`handle` [in, out] Un handle pour énumérer les modules.</span><span class="sxs-lookup"><span data-stu-id="7ee36-106">`handle` [in, out] A handle for enumerating the modules.</span></span>

<span data-ttu-id="7ee36-107">`mod` [out] Le module énuméré.</span><span class="sxs-lookup"><span data-stu-id="7ee36-107">`mod` [out] The enumerated module.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ee36-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7ee36-108">Remarks</span></span>

<span data-ttu-id="7ee36-109">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 25.</span><span class="sxs-lookup"><span data-stu-id="7ee36-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 25th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ee36-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7ee36-110">Requirements</span></span>

<span data-ttu-id="7ee36-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7ee36-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="7ee36-112">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="7ee36-112">**Header:** None</span></span>  
<span data-ttu-id="7ee36-113">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="7ee36-113">**Library:** None</span></span>  
<span data-ttu-id="7ee36-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="7ee36-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="7ee36-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ee36-115">See Also</span></span>

- [<span data-ttu-id="7ee36-116">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="7ee36-116">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="7ee36-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="7ee36-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="7ee36-118">Interface de IXCLRDataModule</span><span class="sxs-lookup"><span data-stu-id="7ee36-118">IXCLRDataModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)
- [<span data-ttu-id="7ee36-119">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="7ee36-119">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
