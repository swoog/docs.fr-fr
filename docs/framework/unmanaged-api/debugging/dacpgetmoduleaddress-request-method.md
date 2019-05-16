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
ms.openlocfilehash: 94279675b5a50bf2a19bb080876b91b85599c077
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65630095"
---
# <a name="dacpgetmoduleaddressrequest-method"></a><span data-ttu-id="90f23-102">DacpGetModuleAddress::Request (méthode)</span><span class="sxs-lookup"><span data-stu-id="90f23-102">DacpGetModuleAddress::Request Method</span></span>

<span data-ttu-id="90f23-103">Exécute une requête pour remplir la structure à partir de la structure de runtime donné.</span><span class="sxs-lookup"><span data-stu-id="90f23-103">Performs a request to populate the structure from the given runtime structure.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="90f23-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90f23-104">Syntax</span></span>

```
HRESULT Request(
    [in] IXCLRDataModule* pDataModule
);
```

## <a name="parameters"></a><span data-ttu-id="90f23-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90f23-105">Parameters</span></span>

`pDataModule`\
<span data-ttu-id="90f23-106">[in] Pointeur vers le module de données de valeur initiale.</span><span class="sxs-lookup"><span data-stu-id="90f23-106">[in] A pointer to the seed data module.</span></span>

## <a name="remarks"></a><span data-ttu-id="90f23-107">Notes</span><span class="sxs-lookup"><span data-stu-id="90f23-107">Remarks</span></span>

<span data-ttu-id="90f23-108">Cette structure se trouve au sein du runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="90f23-108">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="90f23-109">Pour l’utiliser, le moyen le plus simple est d’imiter l’implémentation :</span><span class="sxs-lookup"><span data-stu-id="90f23-109">To use it, the easiest way is to mimic the implementation:</span></span>

- <span data-ttu-id="90f23-110">Retourne la valeur obtenue en appelant le `Request` méthode sur le `IXCLRDataModule*` paramètre avec les paramètres suivants : `((uint32) 0xf0000000, 0, 0, (uint32) sizeof(*this), (uint8*) this)`</span><span class="sxs-lookup"><span data-stu-id="90f23-110">Return the value obtained from calling the `Request` method on the `IXCLRDataModule*` parameter with the following parameters: `((uint32) 0xf0000000, 0, 0, (uint32) sizeof(*this), (uint8*) this)`</span></span>

## <a name="requirements"></a><span data-ttu-id="90f23-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90f23-111">Requirements</span></span>

<span data-ttu-id="90f23-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="90f23-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="90f23-113">**En-tête :** None</span><span class="sxs-lookup"><span data-stu-id="90f23-113">**Header:** None</span></span>     
<span data-ttu-id="90f23-114">**Bibliothèque :** None</span><span class="sxs-lookup"><span data-stu-id="90f23-114">**Library:** None</span></span>  
<span data-ttu-id="90f23-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="90f23-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="90f23-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90f23-116">See also</span></span>

- [<span data-ttu-id="90f23-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="90f23-117">Debugging</span></span>](index.md)
- [<span data-ttu-id="90f23-118">DacpGetModuleAddress Interface</span><span class="sxs-lookup"><span data-stu-id="90f23-118">DacpGetModuleAddress Interface</span></span>](dacpgetmoduleaddress-structure.md)
