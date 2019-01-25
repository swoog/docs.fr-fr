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
ms.openlocfilehash: 825cb8ea94bee980f9e10b90cddf04db32c1a33f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491907"
---
# <a name="ixclrdataprocessenummethodinstancebyaddress-method"></a><span data-ttu-id="70fba-102">IXCLRDataProcess::EnumMethodInstanceByAddress (méthode)</span><span class="sxs-lookup"><span data-stu-id="70fba-102">IXCLRDataProcess::EnumMethodInstanceByAddress Method</span></span>

<span data-ttu-id="70fba-103">Énumère les instances de la méthode de ce processus, en commençant à un offset d’adresse.</span><span class="sxs-lookup"><span data-stu-id="70fba-103">Enumerates the method instances of this process starting at an address offset.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="70fba-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70fba-104">Syntax</span></span>

```
HRESULT EnumMethodInstanceByAddress(
    [in] CLRDATA_ENUM              *handle,
    [out] IXCLRDataMethodInstance **method
);
```

### <a name="parameters"></a><span data-ttu-id="70fba-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70fba-105">Parameters</span></span>

<span data-ttu-id="70fba-106">`handle` [in] Un handle pour énumérer les instances de la méthode.</span><span class="sxs-lookup"><span data-stu-id="70fba-106">`handle` [in] A handle for enumerating the method instances.</span></span>

<span data-ttu-id="70fba-107">`mod` [out] L’instance de la méthode énumérée.</span><span class="sxs-lookup"><span data-stu-id="70fba-107">`mod` [out] The enumerated method instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="70fba-108">Notes</span><span class="sxs-lookup"><span data-stu-id="70fba-108">Remarks</span></span>

<span data-ttu-id="70fba-109">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 28.</span><span class="sxs-lookup"><span data-stu-id="70fba-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 28th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="70fba-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="70fba-110">Requirements</span></span>

<span data-ttu-id="70fba-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="70fba-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>   
<span data-ttu-id="70fba-112">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="70fba-112">**Header:** None</span></span>   
<span data-ttu-id="70fba-113">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="70fba-113">**Library:** None</span></span>   
<span data-ttu-id="70fba-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="70fba-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>   
 
## <a name="see-also"></a><span data-ttu-id="70fba-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70fba-115">See also</span></span>
- [<span data-ttu-id="70fba-116">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="70fba-116">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="70fba-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="70fba-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="70fba-118">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="70fba-118">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
