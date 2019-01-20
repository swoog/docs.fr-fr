---
title: CLRDATA_IL_ADDRESS_MAP Structure
ms.date: 01/16/2019
api.name:
- CLRDATA_IL_ADDRESS_MAP Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- CLRDATA_IL_ADDRESS_MAP Structure
helpviewer.keywords:
- CLRDATA_IL_ADDRESS_MAP Structure [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 94ebef007cf2893b63383aa4657d382728d3c759
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416394"
---
# <a name="clrdatailaddressmap-structure"></a><span data-ttu-id="33695-102">CLRDATA_IL_ADDRESS_MAP Structure</span><span class="sxs-lookup"><span data-stu-id="33695-102">CLRDATA_IL_ADDRESS_MAP Structure</span></span>

<span data-ttu-id="33695-103">Définit un langage intermédiaire pour le mappage d’adresses.</span><span class="sxs-lookup"><span data-stu-id="33695-103">Defines an IL to address mapping.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="33695-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33695-104">Syntax</span></span>

```
typedef struct
{
    ULONG32 ilOffset;
    CLRDATA_ADDRESS startAddress;
    CLRDATA_ADDRESS endAddress;
    CLRDataSourceType type;
} CLRDATA_IL_ADDRESS_MAP;
```

## <a name="members"></a><span data-ttu-id="33695-105">Membres</span><span class="sxs-lookup"><span data-stu-id="33695-105">Members</span></span>

| <span data-ttu-id="33695-106">Membre</span><span class="sxs-lookup"><span data-stu-id="33695-106">Member</span></span>         | <span data-ttu-id="33695-107">Description</span><span class="sxs-lookup"><span data-stu-id="33695-107">Description</span></span>                                            |
| -------------- | ------------------------------------------------------ |
| `ilOffset`     | <span data-ttu-id="33695-108">Offset IL de la plage d’adresses de relation contenant-contenu</span><span class="sxs-lookup"><span data-stu-id="33695-108">IL offset for the contained address range</span></span>              |
| `startAddress` | <span data-ttu-id="33695-109">L’adresse de début de la plage.</span><span class="sxs-lookup"><span data-stu-id="33695-109">The start address of the range.</span></span>                        |
| `endAddress`   | <span data-ttu-id="33695-110">L’adresse de fin de la plage.</span><span class="sxs-lookup"><span data-stu-id="33695-110">The end address of the range.</span></span>                          |
| `type`         | <span data-ttu-id="33695-111">Type des données.</span><span class="sxs-lookup"><span data-stu-id="33695-111">The type of the data.</span></span> <span data-ttu-id="33695-112">Cette valeur n’est actuellement pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="33695-112">This value is currently not used</span></span> |

## <a name="remarks"></a><span data-ttu-id="33695-113">Notes</span><span class="sxs-lookup"><span data-stu-id="33695-113">Remarks</span></span>

<span data-ttu-id="33695-114">Cette structure se trouve au sein du runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="33695-114">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="33695-115">Pour l’utiliser, définir la structure comme indiqué ci-dessus, où `CLRDATA_ADDRESS` est un entier non signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="33695-115">To use it, define the structure as specified above, where `CLRDATA_ADDRESS` is a 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="33695-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="33695-116">Requirements</span></span>

<span data-ttu-id="33695-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="33695-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="33695-118">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="33695-118">**Header:** None</span></span>  
<span data-ttu-id="33695-119">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="33695-119">**Library:** None</span></span>   
<span data-ttu-id="33695-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="33695-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="33695-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33695-121">See Also</span></span>

- [<span data-ttu-id="33695-122">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="33695-122">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="33695-123">Débogage</span><span class="sxs-lookup"><span data-stu-id="33695-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="33695-124">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="33695-124">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
