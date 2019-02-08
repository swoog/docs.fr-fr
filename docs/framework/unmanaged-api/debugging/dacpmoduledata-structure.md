---
title: DacpModuleData Structure
ms.date: 02/01/2019
api.name:
- DacpModuleData Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpModuleData Structure
helpviewer.keywords:
- DacpModuleData Structure [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: db3fdaa768e3d1b445f08c3964521570631f0965
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55828620"
---
# <a name="dacpmoduledata-structure"></a><span data-ttu-id="61845-102">DacpModuleData Structure</span><span class="sxs-lookup"><span data-stu-id="61845-102">DacpModuleData Structure</span></span>

<span data-ttu-id="61845-103">Définit une mémoire tampon de transport pour les informations d’exécution d’un module.</span><span class="sxs-lookup"><span data-stu-id="61845-103">Defines a transport buffer for a module's runtime information.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="61845-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61845-104">Syntax</span></span>

```
struct DacpModuleData
{
    CLRDATA_ADDRESS Address;
    CLRDATA_ADDRESS File; 
    CLRDATA_ADDRESS  ilBase;
    char payLoad[132];
};
```

## <a name="members"></a><span data-ttu-id="61845-105">Membres</span><span class="sxs-lookup"><span data-stu-id="61845-105">Members</span></span>

| <span data-ttu-id="61845-106">Membre</span><span class="sxs-lookup"><span data-stu-id="61845-106">Member</span></span>    | <span data-ttu-id="61845-107">Description</span><span class="sxs-lookup"><span data-stu-id="61845-107">Description</span></span>                                                             |
| --------- | ----------------------------------------------------------------------- |
| `Address` | <span data-ttu-id="61845-108">Adresse de l’objet de module.</span><span class="sxs-lookup"><span data-stu-id="61845-108">Address of the module object.</span></span>                                           |
| `File`    | <span data-ttu-id="61845-109">Pointeur vers le fichier exécutable portable (PE).</span><span class="sxs-lookup"><span data-stu-id="61845-109">A pointer to the portable executable (PE) file.</span></span>                       |
| `ilBase`  | <span data-ttu-id="61845-110">L’adresse de l’image chargée de base.</span><span class="sxs-lookup"><span data-stu-id="61845-110">The address of the loaded image's base.</span></span>                                 |
| `payLoad` | <span data-ttu-id="61845-111">Un tampon de la charge utile pour les informations de module supplémentaire utilisées par le runtime.</span><span class="sxs-lookup"><span data-stu-id="61845-111">A payload buffer for additional module information used by the runtime.</span></span> |


## <a name="remarks"></a><span data-ttu-id="61845-112">Notes</span><span class="sxs-lookup"><span data-stu-id="61845-112">Remarks</span></span>

<span data-ttu-id="61845-113">Cette structure se trouve au sein du runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="61845-113">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="61845-114">Pour l’utiliser, définir la structure comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="61845-114">To use it, define the structure as specified above.</span></span>

## <a name="requirements"></a><span data-ttu-id="61845-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="61845-115">Requirements</span></span>
<span data-ttu-id="61845-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="61845-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="61845-117">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="61845-117">**Header:** None</span></span>  
<span data-ttu-id="61845-118">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="61845-118">**Library:** None</span></span>  
<span data-ttu-id="61845-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="61845-119">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="61845-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61845-120">See also</span></span>
- [<span data-ttu-id="61845-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="61845-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="61845-122">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="61845-122">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
