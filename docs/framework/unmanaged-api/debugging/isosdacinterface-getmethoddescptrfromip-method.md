---
title: ISOSDacInterface::GetMethodDescPtrFromIP (méthode)
ms.date: 02/01/2019
api.name:
- ISOSDacInterface::GetMethodDescPtrFromIP Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetMethodDescPtrFromIP Method
helpviewer.keywords:
- ISOSDacInterface::GetMethodDescPtrFromIP Method [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 74853733b1fb7f023d9f192d3e862dbf6875ecda
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55828616"
---
# <a name="isosdacinterfacegetmethoddescptrfromip-method"></a><span data-ttu-id="7c9f3-102">ISOSDacInterface::GetMethodDescPtrFromIP (méthode)</span><span class="sxs-lookup"><span data-stu-id="7c9f3-102">ISOSDacInterface::GetMethodDescPtrFromIP Method</span></span>

<span data-ttu-id="7c9f3-103">Récupère le pointeur de la MethodDesc correspondant de la méthode contenant l’adresse d’instruction natif donné.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-103">Retrieves the pointer of the MethodDesc corresponding the method containing the given native instruction address.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="7c9f3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c9f3-104">Syntax</span></span>

```
HRESULT GetMethodDescPtrFromIP(
    CLRDATA_ADDRESS ip,
    CLRDATA_ADDRESS * ppMD
);
```

### <a name="parameters"></a><span data-ttu-id="7c9f3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c9f3-105">Parameters</span></span>

<span data-ttu-id="7c9f3-106">`ip` [in] Une adresse dans la méthode lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-106">`ip` [in] An address within the method at runtime.</span></span>

<span data-ttu-id="7c9f3-107">`ppMD` [out] L’adresse de le `MethodDesc` pour la méthode particulière.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-107">`ppMD` [out] The address of the `MethodDesc` for the particular method.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c9f3-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7c9f3-108">Remarks</span></span>

<span data-ttu-id="7c9f3-109">La méthode fournie fait partie de la [ `ISOSDacInterface` interface](isosdacinterface-interface.md) et correspond à l’emplacement de la table de la méthode virtuelle de 21.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-109">The provided method is part of the [`ISOSDacInterface` interface](isosdacinterface-interface.md) and corresponds to the 21st slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c9f3-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7c9f3-110">Requirements</span></span>

<span data-ttu-id="7c9f3-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7c9f3-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="7c9f3-112">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-112">**Header:** None</span></span>  
<span data-ttu-id="7c9f3-113">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-113">**Library:** None</span></span>  
<span data-ttu-id="7c9f3-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="7c9f3-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="7c9f3-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c9f3-115">See also</span></span>

- [<span data-ttu-id="7c9f3-116">Débogage</span><span class="sxs-lookup"><span data-stu-id="7c9f3-116">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="7c9f3-117">Interface de ISOSDacInterface</span><span class="sxs-lookup"><span data-stu-id="7c9f3-117">ISOSDacInterface Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-interface.md)
