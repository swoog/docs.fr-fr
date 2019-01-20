---
title: DacpGetModuleAddress::Request (méthode)
ms.date: 01/16/2019
api.name:
- DacpGetModuleAddress::Request Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpGetModuleAddress::Request Method
helpviewer.keywords:
- DacpGetModuleAddress::Request Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 86a51605ad8ea8b394c5b8a5961f32e96baf9e58
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416426"
---
# <a name="dacpgetmoduleaddressrequest-method"></a><span data-ttu-id="0f917-102">DacpGetModuleAddress::Request (méthode)</span><span class="sxs-lookup"><span data-stu-id="0f917-102">DacpGetModuleAddress::Request Method</span></span>

<span data-ttu-id="0f917-103">Exécute une requête pour remplir la structure à partir de la structure de runtime donné.</span><span class="sxs-lookup"><span data-stu-id="0f917-103">Performs a request to populate the structure from the given runtime structure.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="0f917-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f917-104">Syntax</span></span>

```
HRESULT Request(
    [in] IXCLRDataModule* pDataModule
);
```

### <a name="parameters"></a><span data-ttu-id="0f917-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f917-105">Parameters</span></span>

<span data-ttu-id="0f917-106">`pDataModule` [in] Pointeur vers le module de données de valeur initiale.</span><span class="sxs-lookup"><span data-stu-id="0f917-106">`pDataModule` [in] A pointer to the seed data module.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f917-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0f917-107">Remarks</span></span>

<span data-ttu-id="0f917-108">Cette structure se trouve au sein du runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="0f917-108">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="0f917-109">Pour l’utiliser, le moyen le plus simple est d’imiter l’implémentation :</span><span class="sxs-lookup"><span data-stu-id="0f917-109">To use it, the easiest way is to mimic the implementation:</span></span>

- <span data-ttu-id="0f917-110">Retourne la valeur obtenue en appelant le `Request` méthode sur le `IXCLRDataModule*` paramètre avec les paramètres suivants : `((uint32) 0xf0000000, 0, 0, (uint32) sizeof(*this), (uint8*) this)`</span><span class="sxs-lookup"><span data-stu-id="0f917-110">Return the value obtained from calling the `Request` method on the `IXCLRDataModule*` parameter with the following parameters: `((uint32) 0xf0000000, 0, 0, (uint32) sizeof(*this), (uint8*) this)`</span></span>


## <a name="requirements"></a><span data-ttu-id="0f917-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0f917-111">Requirements</span></span>

<span data-ttu-id="0f917-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0f917-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="0f917-113">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="0f917-113">**Header:** None</span></span>     
<span data-ttu-id="0f917-114">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="0f917-114">**Library:** None</span></span>  
<span data-ttu-id="0f917-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="0f917-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="0f917-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f917-116">See Also</span></span>

- [<span data-ttu-id="0f917-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="0f917-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="0f917-118">DacpGetModuleAddress Interface</span><span class="sxs-lookup"><span data-stu-id="0f917-118">DacpGetModuleAddress Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/dacpgetmoduleaddress-structure.md)
