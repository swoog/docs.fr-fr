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
ms.openlocfilehash: 3b7050e92af6fc58b45837840b2796a5deac955c
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57375335"
---
# <a name="ixclrdataprocessendenummodules-method"></a><span data-ttu-id="2206a-102">IXCLRDataProcess::EndEnumModules (méthode)</span><span class="sxs-lookup"><span data-stu-id="2206a-102">IXCLRDataProcess::EndEnumModules Method</span></span>

<span data-ttu-id="2206a-103">Libère les ressources utilisées par les itérateurs internes utilisés pendant l’énumération de module.</span><span class="sxs-lookup"><span data-stu-id="2206a-103">Releases the resources used by internal iterators used during module enumeration.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="2206a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2206a-104">Syntax</span></span>
```
HRESULT EndEnumModules(
    [in] CLRDATA_ENUM handle
);
```

## <a name="parameters"></a><span data-ttu-id="2206a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2206a-105">Parameters</span></span>

`handle`\
<span data-ttu-id="2206a-106">[out] Un handle pour énumérer les modules.</span><span class="sxs-lookup"><span data-stu-id="2206a-106">[out] A handle for enumerating the modules.</span></span>

## <a name="remarks"></a><span data-ttu-id="2206a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="2206a-107">Remarks</span></span>

<span data-ttu-id="2206a-108">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de 26 de la table de la méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2206a-108">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 26th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="2206a-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2206a-109">Requirements</span></span>

<span data-ttu-id="2206a-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2206a-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>   
<span data-ttu-id="2206a-111">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="2206a-111">**Header:** None</span></span>   
<span data-ttu-id="2206a-112">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="2206a-112">**Library:** None</span></span>   
<span data-ttu-id="2206a-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="2206a-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>   

## <a name="see-also"></a><span data-ttu-id="2206a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2206a-114">See also</span></span>

- [<span data-ttu-id="2206a-115">Débogage</span><span class="sxs-lookup"><span data-stu-id="2206a-115">Debugging</span></span>](index.md)
- [<span data-ttu-id="2206a-116">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="2206a-116">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
