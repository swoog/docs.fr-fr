---
title: IXCLRDataProcess::EnumMethodInstanceByAddress (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: b42939e8e64e75337478ace67a9a91c6a03a94e3
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416461"
---
# <a name="ixclrdataprocessenummethodinstancebyaddress-method"></a><span data-ttu-id="fbfc4-102">IXCLRDataProcess::EnumMethodInstanceByAddress (méthode)</span><span class="sxs-lookup"><span data-stu-id="fbfc4-102">IXCLRDataProcess::EnumMethodInstanceByAddress Method</span></span>

<span data-ttu-id="fbfc4-103">Énumère les instances de la méthode de ce processus, en commençant à un offset d’adresse.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-103">Enumerates the method instances of this process starting at an address offset.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="fbfc4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbfc4-104">Syntax</span></span>

```
HRESULT EnumMethodInstanceByAddress(
    [in] CLRDATA_ENUM              *handle,
    [out] IXCLRDataMethodInstance **method
);
```

### <a name="parameters"></a><span data-ttu-id="fbfc4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbfc4-105">Parameters</span></span>

<span data-ttu-id="fbfc4-106">`handle` [in] Un handle pour énumérer les instances de la méthode.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-106">`handle` [in] A handle for enumerating the method instances.</span></span>

<span data-ttu-id="fbfc4-107">`mod` [out] L’instance de la méthode énumérée.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-107">`mod` [out] The enumerated method instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbfc4-108">Notes</span><span class="sxs-lookup"><span data-stu-id="fbfc4-108">Remarks</span></span>

<span data-ttu-id="fbfc4-109">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 28.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 28th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbfc4-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fbfc4-110">Requirements</span></span>

<span data-ttu-id="fbfc4-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fbfc4-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>   
<span data-ttu-id="fbfc4-112">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-112">**Header:** None</span></span>   
<span data-ttu-id="fbfc4-113">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="fbfc4-113">**Library:** None</span></span>   
<span data-ttu-id="fbfc4-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="fbfc4-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>   
 
## <a name="see-also"></a><span data-ttu-id="fbfc4-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbfc4-115">See Also</span></span>
- [<span data-ttu-id="fbfc4-116">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="fbfc4-116">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="fbfc4-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="fbfc4-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="fbfc4-118">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="fbfc4-118">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
