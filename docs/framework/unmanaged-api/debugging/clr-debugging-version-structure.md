---
title: CLR_DEBUGGING_VERSION, structure
ms.date: 03/30/2017
api_name:
- CLR_DEBUGGING_VERSION
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CLR_DEBUGGING_VERSION
helpviewer_keywords:
- CLR_DEBUGGING_VERSION structure [.NET Framework debugging]
ms.assetid: 4d821186-3ddf-405a-ac44-d79438a9f7f3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 87f938a7119abe4a88da65bd779a5f4a02499516
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61996344"
---
# <a name="clrdebuggingversion-structure"></a><span data-ttu-id="f6b51-102">CLR_DEBUGGING_VERSION, structure</span><span class="sxs-lookup"><span data-stu-id="f6b51-102">CLR_DEBUGGING_VERSION Structure</span></span>
<span data-ttu-id="f6b51-103">Définit la version du produit de CLR (Common Language Runtime) à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="f6b51-103">Defines the product version of the common language runtime (CLR) for debugging purposes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6b51-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6b51-104">Syntax</span></span>  
  
```  
typedef struct _CLR_DEBUGGING_VERSION  
{  
    WORD wStructVersion;
    WORD wMajor;
    WORD wMinor;
    WORD wBuild;
    WORD wRevision;
} CLR_DEBUGGING_VERSION;
```  
  
## <a name="members"></a><span data-ttu-id="f6b51-105">Membres</span><span class="sxs-lookup"><span data-stu-id="f6b51-105">Members</span></span>  
  
|<span data-ttu-id="f6b51-106">Membre</span><span class="sxs-lookup"><span data-stu-id="f6b51-106">Member</span></span>|<span data-ttu-id="f6b51-107">Description</span><span class="sxs-lookup"><span data-stu-id="f6b51-107">Description</span></span>|  
|------------|-----------------|  
|`wStructVersion`|<span data-ttu-id="f6b51-108">Le numéro de version de structure</span><span class="sxs-lookup"><span data-stu-id="f6b51-108">The structure version number</span></span>|  
|`wMajor`|<span data-ttu-id="f6b51-109">Numéro de version principale.</span><span class="sxs-lookup"><span data-stu-id="f6b51-109">The major version number.</span></span>|  
|`wMinor`|<span data-ttu-id="f6b51-110">Numéro de version secondaire.</span><span class="sxs-lookup"><span data-stu-id="f6b51-110">The minor version number.</span></span>|  
|`wBuild`|<span data-ttu-id="f6b51-111">Le numéro de build.</span><span class="sxs-lookup"><span data-stu-id="f6b51-111">The build number.</span></span>|  
|`wRevision`|<span data-ttu-id="f6b51-112">Le numéro de révision.</span><span class="sxs-lookup"><span data-stu-id="f6b51-112">The revision number.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f6b51-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f6b51-113">Remarks</span></span>  
 <span data-ttu-id="f6b51-114">Le `CLR_DEBUGGING_VERSION` structure est identique à la structure COR_VERSION, toutefois, le `CLR_DEBUGGING_VERSION` structure fournit un champ de version de structure supplémentaire (`wStructVersion`).</span><span class="sxs-lookup"><span data-stu-id="f6b51-114">The `CLR_DEBUGGING_VERSION` structure is the same as the COR_VERSION structure, however, the `CLR_DEBUGGING_VERSION` structure provides an additional structure version field (`wStructVersion`).</span></span> <span data-ttu-id="f6b51-115">Actuellement, ce champ doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="f6b51-115">Currently, this field must be set to zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f6b51-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6b51-116">Requirements</span></span>  
 <span data-ttu-id="f6b51-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f6b51-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6b51-118">**En-tête :** CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="f6b51-118">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="f6b51-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f6b51-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f6b51-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6b51-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6b51-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6b51-121">See also</span></span>

- [<span data-ttu-id="f6b51-122">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="f6b51-122">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="f6b51-123">Débogage</span><span class="sxs-lookup"><span data-stu-id="f6b51-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
