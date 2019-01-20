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
ms.openlocfilehash: 83e7d4e1a4ff3c2e6f573d6c097c7cdb9c5f3c54
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416472"
---
# <a name="ixclrdataprocessgetappdomainbyuniqueid-method"></a><span data-ttu-id="77151-102">IXCLRDataProcess::GetAppDomainByUniqueId Method</span><span class="sxs-lookup"><span data-stu-id="77151-102">IXCLRDataProcess::GetAppDomainByUniqueId Method</span></span>

<span data-ttu-id="77151-103">Obtient un `AppDomain` dans un processus en fonction de son identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="77151-103">Gets an `AppDomain` in a process based on its unique identifier.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="77151-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77151-104">Syntax</span></span>
```
HRESULT GetAppDomainByUniqueID(
    [in] ULONG64               id,
    [out] IXCLRDataAppDomain **appDomain
);
```

### <a name="parameters"></a><span data-ttu-id="77151-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77151-105">Parameters</span></span>
<span data-ttu-id="77151-106">`id` [in] L’identificateur unique du domaine d’application</span><span class="sxs-lookup"><span data-stu-id="77151-106">`id` [in] The unique identifier of the AppDomain</span></span>

<span data-ttu-id="77151-107">`appDomain` [out] Le domaine d’application</span><span class="sxs-lookup"><span data-stu-id="77151-107">`appDomain` [out] The AppDomain</span></span>

## <a name="remarks"></a><span data-ttu-id="77151-108">Notes</span><span class="sxs-lookup"><span data-stu-id="77151-108">Remarks</span></span>

<span data-ttu-id="77151-109">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 20.</span><span class="sxs-lookup"><span data-stu-id="77151-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 20th slot of the virtual method table.</span></span> <span data-ttu-id="77151-110">Le `IXCLRDataAppDomain*` retourné est utilisé pour l’interaction avec d’autres API.</span><span class="sxs-lookup"><span data-stu-id="77151-110">The `IXCLRDataAppDomain*` returned is used for interaction with other APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="77151-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="77151-111">Requirements</span></span>
<span data-ttu-id="77151-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="77151-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="77151-113">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="77151-113">**Header:** None</span></span>  
<span data-ttu-id="77151-114">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="77151-114">**Library:** None</span></span>  
<span data-ttu-id="77151-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="77151-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="77151-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77151-116">See Also</span></span>
- [<span data-ttu-id="77151-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="77151-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="77151-118">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="77151-118">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
