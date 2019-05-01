---
title: CLRDATA_ADDRESS_RANGE, structure
ms.date: 01/16/2019
api.name:
- CLRDATA_ADDRESS_RANGE Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- CLRDATA_ADDRESS_RANGE Structure
helpviewer.keywords:
- CLRDATA_ADDRESS_RANGE Structure [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 484ca79483fc4a5d8f0d1cf2cd5a961c297249e7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61961303"
---
# <a name="clrdataaddressrange-structure"></a><span data-ttu-id="735d4-102">CLRDATA_ADDRESS_RANGE, structure</span><span class="sxs-lookup"><span data-stu-id="735d4-102">CLRDATA_ADDRESS_RANGE Structure</span></span>

<span data-ttu-id="735d4-103">Définit une plage d’adresses.</span><span class="sxs-lookup"><span data-stu-id="735d4-103">Defines an address range.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="735d4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="735d4-104">Syntax</span></span>

```
typedef struct
{
    CLRDATA_ADDRESS startAddress;
    CLRDATA_ADDRESS endAddress;
} CLRDATA_ADDRESS_RANGE;
```

## <a name="members"></a><span data-ttu-id="735d4-105">Membres</span><span class="sxs-lookup"><span data-stu-id="735d4-105">Members</span></span>

| <span data-ttu-id="735d4-106">Membre</span><span class="sxs-lookup"><span data-stu-id="735d4-106">Member</span></span>         | <span data-ttu-id="735d4-107">Description</span><span class="sxs-lookup"><span data-stu-id="735d4-107">Description</span></span>                     |
| -------------- | ------------------------------- |
| `startAddress` | <span data-ttu-id="735d4-108">L’adresse de début de la plage.</span><span class="sxs-lookup"><span data-stu-id="735d4-108">The start address of the range.</span></span> |
| `endAddress`   | <span data-ttu-id="735d4-109">L’adresse de fin de la plage.</span><span class="sxs-lookup"><span data-stu-id="735d4-109">The end address of the range.</span></span>   |

## <a name="remarks"></a><span data-ttu-id="735d4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="735d4-110">Remarks</span></span>

<span data-ttu-id="735d4-111">Cette structure se trouve au sein du runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="735d4-111">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="735d4-112">Pour l’utiliser, définir la structure comme indiqué ci-dessus, où `CLRDATA_ADDRESS` est un entier non signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="735d4-112">To use it, define the structure as specified above, where `CLRDATA_ADDRESS` is a 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="735d4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="735d4-113">Requirements</span></span>

<span data-ttu-id="735d4-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="735d4-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="735d4-115">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="735d4-115">**Header:** None</span></span>  
<span data-ttu-id="735d4-116">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="735d4-116">**Library:** None</span></span>  
<span data-ttu-id="735d4-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="735d4-117">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="735d4-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="735d4-118">See also</span></span>

- [<span data-ttu-id="735d4-119">Débogage</span><span class="sxs-lookup"><span data-stu-id="735d4-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="735d4-120">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="735d4-120">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
