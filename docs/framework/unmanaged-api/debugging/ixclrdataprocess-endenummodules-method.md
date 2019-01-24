---
title: IXCLRDataProcess::EndEnumModules (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EndEnumModules Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EndEnumModules Method
helpviewer.keywords:
- IXCLRDataProcess::EndEnumModules Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 50ad55674360d7b880af3ddf701cf17005f30ce7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722736"
---
# <a name="ixclrdataprocessendenummodules-method"></a><span data-ttu-id="8a625-102">IXCLRDataProcess::EndEnumModules (méthode)</span><span class="sxs-lookup"><span data-stu-id="8a625-102">IXCLRDataProcess::EndEnumModules Method</span></span>

<span data-ttu-id="8a625-103">Libère les ressources utilisées par les itérateurs internes utilisés pendant l’énumération de module.</span><span class="sxs-lookup"><span data-stu-id="8a625-103">Releases the resources used by internal iterators used during module enumeration.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="8a625-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a625-104">Syntax</span></span>
```
HRESULT EndEnumModules(
    [in] CLRDATA_ENUM handle
);
```

### <a name="parameters"></a><span data-ttu-id="8a625-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a625-105">Parameters</span></span>
<span data-ttu-id="8a625-106">`handle` [out] Un handle pour énumérer les modules.</span><span class="sxs-lookup"><span data-stu-id="8a625-106">`handle` [out] A handle for enumerating the modules.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a625-107">Notes</span><span class="sxs-lookup"><span data-stu-id="8a625-107">Remarks</span></span>

<span data-ttu-id="8a625-108">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de 26 de la table de la méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="8a625-108">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 26th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a625-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8a625-109">Requirements</span></span>

<span data-ttu-id="8a625-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8a625-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>   
<span data-ttu-id="8a625-111">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="8a625-111">**Header:** None</span></span>   
<span data-ttu-id="8a625-112">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="8a625-112">**Library:** None</span></span>   
<span data-ttu-id="8a625-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="8a625-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>   

## <a name="see-also"></a><span data-ttu-id="8a625-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a625-114">See also</span></span>

- [<span data-ttu-id="8a625-115">Débogage</span><span class="sxs-lookup"><span data-stu-id="8a625-115">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="8a625-116">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="8a625-116">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
