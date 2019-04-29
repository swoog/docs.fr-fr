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
ms.openlocfilehash: 41b6ff0a3c44d3ad997c54b1c82590cc3583fe52
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775230"
---
# <a name="ixclrdataprocessstartenummethodinstancesbyaddress-method"></a><span data-ttu-id="896fa-102">IXCLRDataProcess::StartEnumMethodInstancesByAddress (méthode)</span><span class="sxs-lookup"><span data-stu-id="896fa-102">IXCLRDataProcess::StartEnumMethodInstancesByAddress Method</span></span>

<span data-ttu-id="896fa-103">Fournit un handle pour énumérer les instances de la méthode de `AppDomain` en commençant à une adresse donnée.</span><span class="sxs-lookup"><span data-stu-id="896fa-103">Provides a handle to enumerate the method instances of `AppDomain` starting at a given address.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="896fa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="896fa-104">Syntax</span></span>

```
HRESULT StartEnumMethodInstancesByAddress(
    [in] CLRDATA_ADDRESS     address,
    [in] IXCLRDataAppDomain *appDomain,
    [out] CLRDATA_ENUM      *handle
);
```

## <a name="parameters"></a><span data-ttu-id="896fa-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="896fa-105">Parameters</span></span>

`address`\
<span data-ttu-id="896fa-106">[in] L’adresse de la première instance de méthode.</span><span class="sxs-lookup"><span data-stu-id="896fa-106">[in] The address of the first method instance.</span></span>

`appDomain`\
<span data-ttu-id="896fa-107">[in] Le domaine d’application de la méthode d’instance.</span><span class="sxs-lookup"><span data-stu-id="896fa-107">[in] The AppDomain of the method instances.</span></span>

`handle`\
<span data-ttu-id="896fa-108">[out] Un handle pour énumérer les instances de la méthode.</span><span class="sxs-lookup"><span data-stu-id="896fa-108">[out] A handle for enumerating the method instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="896fa-109">Notes</span><span class="sxs-lookup"><span data-stu-id="896fa-109">Remarks</span></span>

<span data-ttu-id="896fa-110">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de 27 de la table de la méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="896fa-110">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 27th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="896fa-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="896fa-111">Requirements</span></span>

<span data-ttu-id="896fa-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="896fa-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="896fa-113">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="896fa-113">**Header:** None</span></span>  
<span data-ttu-id="896fa-114">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="896fa-114">**Library:** None</span></span>  
<span data-ttu-id="896fa-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="896fa-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="896fa-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="896fa-116">See also</span></span>

- [<span data-ttu-id="896fa-117">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="896fa-117">CLRDataSourceType Enumeration</span></span>](clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="896fa-118">Débogage</span><span class="sxs-lookup"><span data-stu-id="896fa-118">Debugging</span></span>](index.md)
- [<span data-ttu-id="896fa-119">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="896fa-119">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
