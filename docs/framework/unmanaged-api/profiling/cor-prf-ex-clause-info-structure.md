---
title: COR_PRF_EX_CLAUSE_INFO, structure
ms.date: 03/30/2017
api_name:
- COR_PRF_EX_CLAUSE_INFO
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_EX_CLAUSE_INFO
helpviewer_keywords:
- COR_PRF_EX_CLAUSE_INFO structure [.NET Framework profiling]
ms.assetid: 7d0d6fb7-bc9d-40f0-8163-c0d162eaba7d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5e12410ab9886055dca8c3f9103c1e56475c2d5e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59140346"
---
# <a name="corprfexclauseinfo-structure"></a><span data-ttu-id="8f909-102">COR_PRF_EX_CLAUSE_INFO, structure</span><span class="sxs-lookup"><span data-stu-id="8f909-102">COR_PRF_EX_CLAUSE_INFO Structure</span></span>
<span data-ttu-id="8f909-103">Stocke des informations sur une instance de clause d'exception spécifique et sa trame associée.</span><span class="sxs-lookup"><span data-stu-id="8f909-103">Stores information about a specific exception clause instance and its associated frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f909-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f909-104">Syntax</span></span>  
  
```  
typedef struct COR_PRF_EX_CLAUSE_INFO {  
    COR_PRF_CLAUSE_TYPE clauseType;  
    UINT_PTR programCounter;  
    UINT_PTR framePointer;  
    UINT_PTR shadowStackPointer;  
} COR_PRF_EX_CLAUSE_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="8f909-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8f909-105">Members</span></span>  
  
|<span data-ttu-id="8f909-106">Membre</span><span class="sxs-lookup"><span data-stu-id="8f909-106">Member</span></span>|<span data-ttu-id="8f909-107">Description</span><span class="sxs-lookup"><span data-stu-id="8f909-107">Description</span></span>|  
|------------|-----------------|  
|`clauseType`|<span data-ttu-id="8f909-108">Une valeur de la [COR_PRF_CLAUSE_TYPE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-clause-type-enumeration.md) énumération qui spécifie le type de clause d’exception le code venez d’entrer ou de gauche.</span><span class="sxs-lookup"><span data-stu-id="8f909-108">A value of the [COR_PRF_CLAUSE_TYPE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-clause-type-enumeration.md) enumeration that specifies the type of exception clause the code just entered or left.</span></span>|  
|`programCounter`|<span data-ttu-id="8f909-109">Le point d’entrée natif du Gestionnaire de clause — par exemple, le contenu du Registre X86 EIP.</span><span class="sxs-lookup"><span data-stu-id="8f909-109">The native entry point of the clause handler — for example, the contents of the X86 EIP register.</span></span>|  
|`framePointer`|<span data-ttu-id="8f909-110">Le pointeur vers le frame logique pour le Gestionnaire de clause — par exemple, le contenu du Registre X86 EBP.</span><span class="sxs-lookup"><span data-stu-id="8f909-110">The pointer to the logical frame for the clause handler — for example, the contents of the X86 EBP register.</span></span>|  
|`shadowStackPointer`|<span data-ttu-id="8f909-111">Pointeur vers la pile cachée.</span><span class="sxs-lookup"><span data-stu-id="8f909-111">The pointer to the shadow stack.</span></span> <span data-ttu-id="8f909-112">Cette valeur est le contenu du Registre BSP et s’applique uniquement à IA64.</span><span class="sxs-lookup"><span data-stu-id="8f909-112">This value is the contents of the BSP register and applies only to IA64.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8f909-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8f909-113">Remarks</span></span>  
 <span data-ttu-id="8f909-114">Lorsqu’une notification d’exception est reçue, [ICorProfilerInfo2::GetNotifiedExceptionClauseInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getnotifiedexceptionclauseinfo-method.md) peut être utilisé pour obtenir les informations d’adresse et d’image natives pour la clause d’exception (`catch` / `finally`/filtre) qui doit être exécutée ou vient d’être exécutée.</span><span class="sxs-lookup"><span data-stu-id="8f909-114">When an exception notification is received, [ICorProfilerInfo2::GetNotifiedExceptionClauseInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getnotifiedexceptionclauseinfo-method.md) can be used to get the native address and frame information for the exception clause (`catch`/`finally`/filter) that is about to be run or has just been run.</span></span>  
  
 <span data-ttu-id="8f909-115">L’exécution d’une clause d’exception implique le common language runtime (CLR) les rappels suivants :</span><span class="sxs-lookup"><span data-stu-id="8f909-115">Execution of an exception clause involves these callbacks from the common language runtime (CLR):</span></span>  
  
-   [<span data-ttu-id="8f909-116">ICorProfilerCallback::ExceptionCatcherEnter</span><span class="sxs-lookup"><span data-stu-id="8f909-116">ICorProfilerCallback::ExceptionCatcherEnter</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptioncatcherenter-method.md)  
  
-   [<span data-ttu-id="8f909-117">ICorProfilerCallback::ExceptionUnwindFinallyEnter</span><span class="sxs-lookup"><span data-stu-id="8f909-117">ICorProfilerCallback::ExceptionUnwindFinallyEnter</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionunwindfinallyenter-method.md)  
  
-   [<span data-ttu-id="8f909-118">ICorProfilerCallback::ExceptionSearchFilterEnter</span><span class="sxs-lookup"><span data-stu-id="8f909-118">ICorProfilerCallback::ExceptionSearchFilterEnter</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfilterenter-method.md)  
  
-   [<span data-ttu-id="8f909-119">ICorProfilerCallback::ExceptionCatcherLeave</span><span class="sxs-lookup"><span data-stu-id="8f909-119">ICorProfilerCallback::ExceptionCatcherLeave</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptioncatcherleave-method.md)  
  
-   [<span data-ttu-id="8f909-120">ICorProfilerCallback::ExceptionUnwindFinallyLeave</span><span class="sxs-lookup"><span data-stu-id="8f909-120">ICorProfilerCallback::ExceptionUnwindFinallyLeave</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionunwindfinallyleave-method.md)  
  
-   [<span data-ttu-id="8f909-121">ICorProfilerCallback::ExceptionSearchFilterLeave</span><span class="sxs-lookup"><span data-stu-id="8f909-121">ICorProfilerCallback::ExceptionSearchFilterLeave</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfilterleave-method.md)  
  
## <a name="requirements"></a><span data-ttu-id="8f909-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f909-122">Requirements</span></span>  
 <span data-ttu-id="8f909-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8f909-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8f909-124">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="8f909-124">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="8f909-125">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8f909-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8f909-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8f909-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f909-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f909-127">See also</span></span>

- [<span data-ttu-id="8f909-128">Structures de profilage</span><span class="sxs-lookup"><span data-stu-id="8f909-128">Profiling Structures</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-structures.md)
