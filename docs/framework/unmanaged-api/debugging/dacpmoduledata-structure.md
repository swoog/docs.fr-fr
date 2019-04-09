---
title: DacpModuleData, structure
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
ms.openlocfilehash: 752d87c5f4a6b8d854a06be8962ee754cdd4622d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59132000"
---
# <a name="dacpmoduledata-structure"></a><span data-ttu-id="bf945-102">DacpModuleData, structure</span><span class="sxs-lookup"><span data-stu-id="bf945-102">DacpModuleData Structure</span></span>

<span data-ttu-id="bf945-103">Définit une mémoire tampon de transport pour les informations d’exécution d’un module.</span><span class="sxs-lookup"><span data-stu-id="bf945-103">Defines a transport buffer for a module's runtime information.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="bf945-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf945-104">Syntax</span></span>

```
struct DacpModuleData
{
    CLRDATA_ADDRESS Address;
    CLRDATA_ADDRESS File; 
    CLRDATA_ADDRESS  ilBase;
    char payLoad[132];
};
```

## <a name="members"></a><span data-ttu-id="bf945-105">Membres</span><span class="sxs-lookup"><span data-stu-id="bf945-105">Members</span></span>

| <span data-ttu-id="bf945-106">Membre</span><span class="sxs-lookup"><span data-stu-id="bf945-106">Member</span></span>    | <span data-ttu-id="bf945-107">Description</span><span class="sxs-lookup"><span data-stu-id="bf945-107">Description</span></span>                                                             |
| --------- | ----------------------------------------------------------------------- |
| `Address` | <span data-ttu-id="bf945-108">Adresse de l’objet de module.</span><span class="sxs-lookup"><span data-stu-id="bf945-108">Address of the module object.</span></span>                                           |
| `File`    | <span data-ttu-id="bf945-109">Pointeur vers le fichier exécutable portable (PE).</span><span class="sxs-lookup"><span data-stu-id="bf945-109">A pointer to the portable executable (PE) file.</span></span>                       |
| `ilBase`  | <span data-ttu-id="bf945-110">L’adresse de l’image chargée de base.</span><span class="sxs-lookup"><span data-stu-id="bf945-110">The address of the loaded image's base.</span></span>                                 |
| `payLoad` | <span data-ttu-id="bf945-111">Un tampon de la charge utile pour les informations de module supplémentaire utilisées par le runtime.</span><span class="sxs-lookup"><span data-stu-id="bf945-111">A payload buffer for additional module information used by the runtime.</span></span> |

## <a name="remarks"></a><span data-ttu-id="bf945-112">Notes</span><span class="sxs-lookup"><span data-stu-id="bf945-112">Remarks</span></span>

<span data-ttu-id="bf945-113">Cette structure se trouve au sein du runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="bf945-113">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="bf945-114">Pour l’utiliser, définir la structure comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="bf945-114">To use it, define the structure as specified above.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf945-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf945-115">Requirements</span></span>
<span data-ttu-id="bf945-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bf945-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="bf945-117">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="bf945-117">**Header:** None</span></span>  
<span data-ttu-id="bf945-118">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="bf945-118">**Library:** None</span></span>  
**<span data-ttu-id="bf945-119">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="bf945-119">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a><span data-ttu-id="bf945-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf945-120">See also</span></span>

- [<span data-ttu-id="bf945-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="bf945-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="bf945-122">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="bf945-122">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
