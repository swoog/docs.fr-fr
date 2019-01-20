---
title: IXCLRDataProcess::StartEnumMethodInstancesByAddress (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::StartEnumMethodInstancesByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::StartEnumMethodInstancesByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::StartEnumMethodInstancesByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 88ce9dd928871d71058fe28c243a9fb51b729778
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416466"
---
# <a name="ixclrdataprocessstartenummethodinstancesbyaddress-method"></a><span data-ttu-id="5460e-102">IXCLRDataProcess::StartEnumMethodInstancesByAddress (méthode)</span><span class="sxs-lookup"><span data-stu-id="5460e-102">IXCLRDataProcess::StartEnumMethodInstancesByAddress Method</span></span>

<span data-ttu-id="5460e-103">Fournit un handle pour énumérer les instances de la méthode de `AppDomain` en commençant à une adresse donnée.</span><span class="sxs-lookup"><span data-stu-id="5460e-103">Provides a handle to enumerate the method instances of `AppDomain` starting at a given address.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="5460e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5460e-104">Syntax</span></span>

```
HRESULT StartEnumMethodInstancesByAddress(
    [in] CLRDATA_ADDRESS     address,
    [in] IXCLRDataAppDomain *appDomain,
    [out] CLRDATA_ENUM      *handle
);
```

### <a name="parameters"></a><span data-ttu-id="5460e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5460e-105">Parameters</span></span>

<span data-ttu-id="5460e-106">`address` [in] L’adresse de la première instance de méthode.</span><span class="sxs-lookup"><span data-stu-id="5460e-106">`address` [in] The address of the first method instance.</span></span>

<span data-ttu-id="5460e-107">`appDomain` [in] Le domaine d’application de la méthode d’instance.</span><span class="sxs-lookup"><span data-stu-id="5460e-107">`appDomain` [in] The AppDomain of the method instances.</span></span>

<span data-ttu-id="5460e-108">`handle` [out] Un handle pour énumérer les instances de la méthode.</span><span class="sxs-lookup"><span data-stu-id="5460e-108">`handle` [out] A handle for enumerating the method instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="5460e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="5460e-109">Remarks</span></span>

<span data-ttu-id="5460e-110">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de 27 de la table de la méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5460e-110">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 27th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="5460e-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5460e-111">Requirements</span></span>

<span data-ttu-id="5460e-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5460e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="5460e-113">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="5460e-113">**Header:** None</span></span>  
<span data-ttu-id="5460e-114">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="5460e-114">**Library:** None</span></span>  
<span data-ttu-id="5460e-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="5460e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="5460e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5460e-116">See Also</span></span>

- [<span data-ttu-id="5460e-117">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="5460e-117">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="5460e-118">Débogage</span><span class="sxs-lookup"><span data-stu-id="5460e-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="5460e-119">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="5460e-119">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
