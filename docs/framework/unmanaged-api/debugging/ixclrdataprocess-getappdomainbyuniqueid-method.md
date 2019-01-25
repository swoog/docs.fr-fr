---
title: IXCLRDataProcess::GetAppDomainByUniqueId Method
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
helpviewer.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: cf610e3af26c60dd9bf738bff8785890394d0f34
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710272"
---
# <a name="ixclrdataprocessgetappdomainbyuniqueid-method"></a><span data-ttu-id="a671a-102">IXCLRDataProcess::GetAppDomainByUniqueId Method</span><span class="sxs-lookup"><span data-stu-id="a671a-102">IXCLRDataProcess::GetAppDomainByUniqueId Method</span></span>

<span data-ttu-id="a671a-103">Obtient un `AppDomain` dans un processus en fonction de son identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="a671a-103">Gets an `AppDomain` in a process based on its unique identifier.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="a671a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a671a-104">Syntax</span></span>
```
HRESULT GetAppDomainByUniqueID(
    [in] ULONG64               id,
    [out] IXCLRDataAppDomain **appDomain
);
```

### <a name="parameters"></a><span data-ttu-id="a671a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a671a-105">Parameters</span></span>
<span data-ttu-id="a671a-106">`id` [in] L’identificateur unique du domaine d’application</span><span class="sxs-lookup"><span data-stu-id="a671a-106">`id` [in] The unique identifier of the AppDomain</span></span>

<span data-ttu-id="a671a-107">`appDomain` [out] Le domaine d’application</span><span class="sxs-lookup"><span data-stu-id="a671a-107">`appDomain` [out] The AppDomain</span></span>

## <a name="remarks"></a><span data-ttu-id="a671a-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a671a-108">Remarks</span></span>

<span data-ttu-id="a671a-109">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 20.</span><span class="sxs-lookup"><span data-stu-id="a671a-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 20th slot of the virtual method table.</span></span> <span data-ttu-id="a671a-110">Le `IXCLRDataAppDomain*` retourné est utilisé pour l’interaction avec d’autres API.</span><span class="sxs-lookup"><span data-stu-id="a671a-110">The `IXCLRDataAppDomain*` returned is used for interaction with other APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a671a-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a671a-111">Requirements</span></span>
<span data-ttu-id="a671a-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a671a-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="a671a-113">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="a671a-113">**Header:** None</span></span>  
<span data-ttu-id="a671a-114">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="a671a-114">**Library:** None</span></span>  
<span data-ttu-id="a671a-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="a671a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="a671a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a671a-116">See also</span></span>
- [<span data-ttu-id="a671a-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="a671a-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="a671a-118">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="a671a-118">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
