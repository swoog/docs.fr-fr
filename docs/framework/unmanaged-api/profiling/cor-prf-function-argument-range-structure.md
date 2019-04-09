---
title: COR_PRF_FUNCTION_ARGUMENT_RANGE, structure
ms.date: 03/30/2017
api_name:
- COR_PRF_FUNCTION_ARGUMENT_RANGE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_FUNCTION_ARGUMENT_RANGE
helpviewer_keywords:
- COR_PRF_FUNCTION_ARGUMENT_RANGE structure [.NET Framework profiling'
ms.assetid: 9f469eac-ac66-419b-8668-fe705bc1a51f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: dffefedf14d5f219736e429be191021b2de7ddd2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59125591"
---
# <a name="corprffunctionargumentrange-structure"></a><span data-ttu-id="97995-102">COR_PRF_FUNCTION_ARGUMENT_RANGE, structure</span><span class="sxs-lookup"><span data-stu-id="97995-102">COR_PRF_FUNCTION_ARGUMENT_RANGE Structure</span></span>
<span data-ttu-id="97995-103">Représente un bloc d’arguments de fonction stockés de façon contiguë en mémoire selon un ordre de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="97995-103">Represents a block of function arguments stored contiguously in left-to-right order in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97995-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97995-104">Syntax</span></span>  
  
```  
typedef struct _COR_PRF_FUNCTION_ARGUMENT_RANGE {  
    UINT_PTR startAddress;  
    ULONG length;  
} COR_PRF_FUNCTION_ARGUMENT_RANGE;  
```  
  
## <a name="members"></a><span data-ttu-id="97995-105">Membres</span><span class="sxs-lookup"><span data-stu-id="97995-105">Members</span></span>  
  
|<span data-ttu-id="97995-106">Membres</span><span class="sxs-lookup"><span data-stu-id="97995-106">Members</span></span>|<span data-ttu-id="97995-107">Description</span><span class="sxs-lookup"><span data-stu-id="97995-107">Description</span></span>|  
|-------------|-----------------|  
|`startAddress`|<span data-ttu-id="97995-108">Adresse de départ du bloc.</span><span class="sxs-lookup"><span data-stu-id="97995-108">The starting address of the block.</span></span>|  
|`length`|<span data-ttu-id="97995-109">La longueur du bloc contigu.</span><span class="sxs-lookup"><span data-stu-id="97995-109">The length of the contiguous block.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="97995-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97995-110">Requirements</span></span>  
 <span data-ttu-id="97995-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="97995-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="97995-112">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="97995-112">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="97995-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="97995-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="97995-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="97995-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="97995-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97995-115">See also</span></span>

- [<span data-ttu-id="97995-116">Structures de profilage</span><span class="sxs-lookup"><span data-stu-id="97995-116">Profiling Structures</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-structures.md)
