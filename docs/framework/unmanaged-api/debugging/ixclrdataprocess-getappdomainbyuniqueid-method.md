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
ms.openlocfilehash: 257fa2cf03a62ea888b76519aa5c9f9e84038045
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59126501"
---
# <a name="ixclrdataprocessgetappdomainbyuniqueid-method"></a><span data-ttu-id="f61d3-102">IXCLRDataProcess::GetAppDomainByUniqueId Method</span><span class="sxs-lookup"><span data-stu-id="f61d3-102">IXCLRDataProcess::GetAppDomainByUniqueId Method</span></span>

<span data-ttu-id="f61d3-103">Obtient un `AppDomain` dans un processus en fonction de son identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="f61d3-103">Gets an `AppDomain` in a process based on its unique identifier.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="f61d3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f61d3-104">Syntax</span></span>
```
HRESULT GetAppDomainByUniqueID(
    [in] ULONG64               id,
    [out] IXCLRDataAppDomain **appDomain
);
```

## <a name="parameters"></a><span data-ttu-id="f61d3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f61d3-105">Parameters</span></span>

`id`\
<span data-ttu-id="f61d3-106">[in] L’identificateur unique du domaine d’application</span><span class="sxs-lookup"><span data-stu-id="f61d3-106">[in] The unique identifier of the AppDomain</span></span>

`appDomain`\
<span data-ttu-id="f61d3-107">[out] Le domaine d’application</span><span class="sxs-lookup"><span data-stu-id="f61d3-107">[out] The AppDomain</span></span>

## <a name="remarks"></a><span data-ttu-id="f61d3-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f61d3-108">Remarks</span></span>

<span data-ttu-id="f61d3-109">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 20.</span><span class="sxs-lookup"><span data-stu-id="f61d3-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 20th slot of the virtual method table.</span></span> <span data-ttu-id="f61d3-110">Le `IXCLRDataAppDomain*` retourné est utilisé pour l’interaction avec d’autres API.</span><span class="sxs-lookup"><span data-stu-id="f61d3-110">The `IXCLRDataAppDomain*` returned is used for interaction with other APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="f61d3-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f61d3-111">Requirements</span></span>
<span data-ttu-id="f61d3-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f61d3-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="f61d3-113">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="f61d3-113">**Header:** None</span></span>  
<span data-ttu-id="f61d3-114">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="f61d3-114">**Library:** None</span></span>  
**<span data-ttu-id="f61d3-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="f61d3-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a><span data-ttu-id="f61d3-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f61d3-116">See also</span></span>

- [<span data-ttu-id="f61d3-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="f61d3-117">Debugging</span></span>](index.md)
- [<span data-ttu-id="f61d3-118">IXCLRDataProcess, interface</span><span class="sxs-lookup"><span data-stu-id="f61d3-118">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
