---
title: COR_PRF_FUNCTION, structure
ms.date: 03/30/2017
api_name:
- COR_PRF_FUNCTION
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_FUNCTION
helpviewer_keywords:
- COR_PRF_FUNCTION structure [.NET Framework profiling]
ms.assetid: 8bb5acf5-cf4b-4ccb-93f1-46db1f3f8bf3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1bc8d588641163ccf98054fdf1930a72a04c770c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452060"
---
# <a name="corprffunction-structure"></a><span data-ttu-id="6a0ee-102">COR_PRF_FUNCTION, structure</span><span class="sxs-lookup"><span data-stu-id="6a0ee-102">COR_PRF_FUNCTION Structure</span></span>
<span data-ttu-id="6a0ee-103">Fournit une représentation unique d'une fonction en combinant son ID avec l'ID de sa version recompilée.</span><span class="sxs-lookup"><span data-stu-id="6a0ee-103">Provides a unique representation of a function by combining its ID with the ID of its recompiled version.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6a0ee-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a0ee-104">Syntax</span></span>  
  
```  
typedef struct _COR_PRF_FUNCTION {    FunctionID functionId;    ReJITID    reJitId;} COR_PRF_FUNCTION;  
```  
  
## <a name="members"></a><span data-ttu-id="6a0ee-105">Membres</span><span class="sxs-lookup"><span data-stu-id="6a0ee-105">Members</span></span>  
  
|<span data-ttu-id="6a0ee-106">Membre</span><span class="sxs-lookup"><span data-stu-id="6a0ee-106">Member</span></span>|<span data-ttu-id="6a0ee-107">Description</span><span class="sxs-lookup"><span data-stu-id="6a0ee-107">Description</span></span>|  
|------------|-----------------|  
|`functionId`|<span data-ttu-id="6a0ee-108">L’ID de la fonction.</span><span class="sxs-lookup"><span data-stu-id="6a0ee-108">The ID of the function.</span></span>|  
|`reJitId`|<span data-ttu-id="6a0ee-109">L’ID de la fonction recompilée.</span><span class="sxs-lookup"><span data-stu-id="6a0ee-109">The ID of the recompiled function.</span></span> <span data-ttu-id="6a0ee-110">La valeur 0 (zéro) représente la version d’origine de la fonction.</span><span class="sxs-lookup"><span data-stu-id="6a0ee-110">A value of 0 (zero) represents the original version of the function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6a0ee-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6a0ee-111">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6a0ee-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6a0ee-112">Requirements</span></span>  
 <span data-ttu-id="6a0ee-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6a0ee-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6a0ee-114">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="6a0ee-114">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="6a0ee-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6a0ee-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6a0ee-116">**Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6a0ee-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a0ee-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a0ee-117">See Also</span></span>  
 [<span data-ttu-id="6a0ee-118">Structures de profilage</span><span class="sxs-lookup"><span data-stu-id="6a0ee-118">Profiling Structures</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-structures.md)
