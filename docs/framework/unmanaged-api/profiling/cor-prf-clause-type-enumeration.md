---
title: COR_PRF_CLAUSE_TYPE, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_CLAUSE_TYPE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_CLAUSE_TYPE
helpviewer_keywords:
- COR_PRF_CLAUSE_TYPE enumeration [.NET Framework profiling]
ms.assetid: f64c325a-ed3a-4aaf-b847-a88edbc4fefc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 861f4c18f4c5151dc7215d300775928b88f018aa
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59090626"
---
# <a name="corprfclausetype-enumeration"></a><span data-ttu-id="e2c7c-102">COR_PRF_CLAUSE_TYPE, énumération</span><span class="sxs-lookup"><span data-stu-id="e2c7c-102">COR_PRF_CLAUSE_TYPE Enumeration</span></span>
<span data-ttu-id="e2c7c-103">Indique le type de clause d'exception où le code vient d'entrer ou qu'il vient de quitter.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-103">Indicates the type of exception clause that the code has just entered or left.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2c7c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2c7c-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_CLAUSE_NONE = 0,  
    COR_PRF_CLAUSE_FILTER = 1,  
    COR_PRF_CLAUSE_CATCH = 2,  
    COR_PRF_CLAUSE_FINALLY = 3,  
} COR_PRF_CLAUSE_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="e2c7c-105">Membres</span><span class="sxs-lookup"><span data-stu-id="e2c7c-105">Members</span></span>  
  
|<span data-ttu-id="e2c7c-106">Membre</span><span class="sxs-lookup"><span data-stu-id="e2c7c-106">Member</span></span>|<span data-ttu-id="e2c7c-107">Description</span><span class="sxs-lookup"><span data-stu-id="e2c7c-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_CLAUSE_NONE`|<span data-ttu-id="e2c7c-108">La clause d’exception n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-108">The exception clause is not valid.</span></span>|  
|`COR_PRF_CLAUSE_FILTER`|<span data-ttu-id="e2c7c-109">La clause d’exception est une expression de filtre.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-109">The exception clause is a filter expression.</span></span>|  
|`COR_PRF_CLAUSE_CATCH`|<span data-ttu-id="e2c7c-110">La clause d’exception est un `catch` instruction.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-110">The exception clause is a `catch` statement.</span></span>|  
|`COR_PRF_CLAUSE_FINALLY`|<span data-ttu-id="e2c7c-111">La clause d’exception est un `finally` instruction.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-111">The exception clause is a `finally` statement.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e2c7c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2c7c-112">Requirements</span></span>  
 <span data-ttu-id="e2c7c-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e2c7c-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e2c7c-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e2c7c-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e2c7c-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e2c7c-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="e2c7c-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="e2c7c-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="e2c7c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2c7c-117">See also</span></span>

- [<span data-ttu-id="e2c7c-118">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="e2c7c-118">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
