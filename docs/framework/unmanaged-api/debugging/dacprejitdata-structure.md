---
title: Structure de DacpReJitData
ms.date: 02/01/2019
api.name:
- DacpReJitData Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpReJitData Structure
helpviewer.keywords:
- DacpReJitData Structure [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 974b99da085a5cb969ab37cddb0f2f2c62010d14
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55828632"
---
# <a name="dacprejitdata-structure"></a><span data-ttu-id="aaa1f-102">Structure de DacpReJitData</span><span class="sxs-lookup"><span data-stu-id="aaa1f-102">DacpReJitData Structure</span></span>

<span data-ttu-id="aaa1f-103">Définit les informations de base sur une méthode donnée instrumentée du profileur.</span><span class="sxs-lookup"><span data-stu-id="aaa1f-103">Defines the basic information about a given profiler-instrumented method.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="aaa1f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaa1f-104">Syntax</span></span>

```
struct MSLAYOUT DacpReJitData
{
    enum Flags
    {
        kUnknown,
        kRequested,
        kActive,
        kReverted,
    };

    CLRDATA_ADDRESS                 rejitID;
    Flags                           flags;
    CLRDATA_ADDRESS                 NativeCodeAddr;
};
```

## <a name="members"></a><span data-ttu-id="aaa1f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="aaa1f-105">Members</span></span>

| <span data-ttu-id="aaa1f-106">Membre</span><span class="sxs-lookup"><span data-stu-id="aaa1f-106">Member</span></span>           | <span data-ttu-id="aaa1f-107">Description</span><span class="sxs-lookup"><span data-stu-id="aaa1f-107">Description</span></span>                                                                                      |
| ---------------- | ------------------------------------------------------------------------------------------------ |
| `rejitID`        | <span data-ttu-id="aaa1f-108">Le numéro de révision ReJit pour une méthode.</span><span class="sxs-lookup"><span data-stu-id="aaa1f-108">The ReJit revision number for a method.</span></span>                                                          |
| `flags`          | <span data-ttu-id="aaa1f-109">Un indicateur qui spécifie l’état actuel de l’instrumentation ReJit de la méthode pour la version donnée.</span><span class="sxs-lookup"><span data-stu-id="aaa1f-109">A flag indicating the current state of the method's ReJit instrumentation for the given version.</span></span> |
| `NativeCodeAddr` | <span data-ttu-id="aaa1f-110">L’adresse de base d’implémentation de rejitted de la méthode.</span><span class="sxs-lookup"><span data-stu-id="aaa1f-110">The base address of the method's rejitted implementation.</span></span>                                         |


## <a name="remarks"></a><span data-ttu-id="aaa1f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="aaa1f-111">Remarks</span></span>

<span data-ttu-id="aaa1f-112">Cette structure se trouve au sein du runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="aaa1f-112">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="aaa1f-113">Pour l’utiliser, définir la structure comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="aaa1f-113">To use it, define the structure as specified above.</span></span> <span data-ttu-id="aaa1f-114">La structure doit également être définie à l’aide de `ms_struct` de livraison si ce n’est pas à l’aide de compilateurs Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aaa1f-114">The structure must also be defined using `ms_struct` packing if not using the Microsoft compilers.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa1f-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="aaa1f-115">Requirements</span></span>
<span data-ttu-id="aaa1f-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="aaa1f-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="aaa1f-117">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="aaa1f-117">**Header:** None</span></span>  
<span data-ttu-id="aaa1f-118">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="aaa1f-118">**Library:** None</span></span>  
<span data-ttu-id="aaa1f-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="aaa1f-119">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="aaa1f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaa1f-120">See also</span></span>
- [<span data-ttu-id="aaa1f-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="aaa1f-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="aaa1f-122">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="aaa1f-122">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
