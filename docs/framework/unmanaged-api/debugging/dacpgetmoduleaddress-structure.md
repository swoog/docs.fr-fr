---
title: DacpGetModuleAddress Structure
ms.date: 01/16/2019
api.name:
- DacpGetModuleAddress Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpGetModuleAddress Structure
helpviewer.keywords:
- DacpGetModuleAddress Structure [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: cbea6c0562c68ae5d18247dc97bc53eb9dfbfd7e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59104103"
---
# <a name="dacpgetmoduleaddress-structure"></a><span data-ttu-id="95b25-102">DacpGetModuleAddress Structure</span><span class="sxs-lookup"><span data-stu-id="95b25-102">DacpGetModuleAddress Structure</span></span>

<span data-ttu-id="95b25-103">Définit le conteneur pour une demande d’adresse de module.</span><span class="sxs-lookup"><span data-stu-id="95b25-103">Defines the container for a module address request.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="95b25-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95b25-104">Syntax</span></span>

```
struct DacpGetModuleAddress
{
    CLRDATA_ADDRESS ModulePtr;
};
```

## <a name="members"></a><span data-ttu-id="95b25-105">Membres</span><span class="sxs-lookup"><span data-stu-id="95b25-105">Members</span></span>

| <span data-ttu-id="95b25-106">Membre</span><span class="sxs-lookup"><span data-stu-id="95b25-106">Member</span></span>      | <span data-ttu-id="95b25-107">Description</span><span class="sxs-lookup"><span data-stu-id="95b25-107">Description</span></span>                |
| ----------- | -------------------------- |
| `ModulePtr` | <span data-ttu-id="95b25-108">Pointeur vers le module.</span><span class="sxs-lookup"><span data-stu-id="95b25-108">The pointer to the module.</span></span> |

## <a name="methods"></a><span data-ttu-id="95b25-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="95b25-109">Methods</span></span>

| <span data-ttu-id="95b25-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="95b25-110">Method</span></span>                                                                                               | <span data-ttu-id="95b25-111">Description</span><span class="sxs-lookup"><span data-stu-id="95b25-111">Description</span></span>                                                                    |
| ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| [<span data-ttu-id="95b25-112">Requête</span><span class="sxs-lookup"><span data-stu-id="95b25-112">Request</span></span>](../../../../docs/framework/unmanaged-api/debugging/dacpgetmoduleaddress-request-method.md) | <span data-ttu-id="95b25-113">Exécute une requête pour remplir la structure à partir de la structure de runtime donné.</span><span class="sxs-lookup"><span data-stu-id="95b25-113">Performs a request to populate the structure from the given runtime structure.</span></span> |

## <a name="remarks"></a><span data-ttu-id="95b25-114">Notes</span><span class="sxs-lookup"><span data-stu-id="95b25-114">Remarks</span></span>

<span data-ttu-id="95b25-115">Cette structure se trouve au sein du runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="95b25-115">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="95b25-116">Pour l’utiliser, définir la structure comme indiqué ci-dessus, où `CLRDATA_ADDRESS` est un entier non signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="95b25-116">To use it, define the structure as specified above, where `CLRDATA_ADDRESS` is a 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="95b25-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95b25-117">Requirements</span></span>
<span data-ttu-id="95b25-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="95b25-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="95b25-119">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="95b25-119">**Header:** None</span></span>  
<span data-ttu-id="95b25-120">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="95b25-120">**Library:** None</span></span>  
<span data-ttu-id="95b25-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="95b25-121">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="95b25-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95b25-122">See also</span></span>

- [<span data-ttu-id="95b25-123">Débogage</span><span class="sxs-lookup"><span data-stu-id="95b25-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="95b25-124">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="95b25-124">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
