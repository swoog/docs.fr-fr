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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775146"
---
# <a name="corprfexclauseinfo-structure"></a><span data-ttu-id="46c53-102">COR_PRF_EX_CLAUSE_INFO, structure</span><span class="sxs-lookup"><span data-stu-id="46c53-102">COR_PRF_EX_CLAUSE_INFO Structure</span></span>
<span data-ttu-id="46c53-103">Stocke des informations sur une instance de clause d'exception spécifique et sa trame associée.</span><span class="sxs-lookup"><span data-stu-id="46c53-103">Stores information about a specific exception clause instance and its associated frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46c53-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46c53-104">Syntax</span></span>  
  
```  
typedef struct COR_PRF_EX_CLAUSE_INFO {  
    COR_PRF_CLAUSE_TYPE clauseType;  
    UINT_PTR programCounter;  
    UINT_PTR framePointer;  
    UINT_PTR shadowStackPointer;  
} COR_PRF_EX_CLAUSE_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="46c53-105">Membres</span><span class="sxs-lookup"><span data-stu-id="46c53-105">Members</span></span>  
  
|<span data-ttu-id="46c53-106">Membre</span><span class="sxs-lookup"><span data-stu-id="46c53-106">Member</span></span>|<span data-ttu-id="46c53-107">Description</span><span class="sxs-lookup"><span data-stu-id="46c53-107">Description</span></span>|  
|------------|-----------------|  
|`clauseType`|<span data-ttu-id="46c53-108">Une valeur de la [COR_PRF_CLAUSE_TYPE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-clause-type-enumeration.md) énumération qui spécifie le type de clause d’exception le code venez d’entrer ou de gauche.</span><span class="sxs-lookup"><span data-stu-id="46c53-108">A value of the [COR_PRF_CLAUSE_TYPE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-clause-type-enumeration.md) enumeration that specifies the type of exception clause the code just entered or left.</span></span>|  
|`programCounter`|<span data-ttu-id="46c53-109">Le point d’entrée natif du Gestionnaire de clause — par exemple, le contenu du Registre X86 EIP.</span><span class="sxs-lookup"><span data-stu-id="46c53-109">The native entry point of the clause handler — for example, the contents of the X86 EIP register.</span></span>|  
|`framePointer`|<span data-ttu-id="46c53-110">Le pointeur vers le frame logique pour le Gestionnaire de clause — par exemple, le contenu du Registre X86 EBP.</span><span class="sxs-lookup"><span data-stu-id="46c53-110">The pointer to the logical frame for the clause handler — for example, the contents of the X86 EBP register.</span></span>|  
|`shadowStackPointer`|<span data-ttu-id="46c53-111">Pointeur vers la pile cachée.</span><span class="sxs-lookup"><span data-stu-id="46c53-111">The pointer to the shadow stack.</span></span> <span data-ttu-id="46c53-112">Cette valeur est le contenu du Registre BSP et s’applique uniquement à IA64.</span><span class="sxs-lookup"><span data-stu-id="46c53-112">This value is the contents of the BSP register and applies only to IA64.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="46c53-113">Notes</span><span class="sxs-lookup"><span data-stu-id="46c53-113">Remarks</span></span>  
 <span data-ttu-id="46c53-114">Lorsqu’une notification d’exception est reçue, [ICorProfilerInfo2::GetNotifiedExceptionClauseInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getnotifiedexceptionclauseinfo-method.md) peut être utilisé pour obtenir les informations d’adresse et d’image natives pour la clause d’exception (`catch` / `finally`/filtre) qui doit être exécutée ou vient d’être exécutée.</span><span class="sxs-lookup"><span data-stu-id="46c53-114">When an exception notification is received, [ICorProfilerInfo2::GetNotifiedExceptionClauseInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getnotifiedexceptionclauseinfo-method.md) can be used to get the native address and frame information for the exception clause (`catch`/`finally`/filter) that is about to be run or has just been run.</span></span>  
  
 <span data-ttu-id="46c53-115">L’exécution d’une clause d’exception implique le common language runtime (CLR) les rappels suivants :</span><span class="sxs-lookup"><span data-stu-id="46c53-115">Execution of an exception clause involves these callbacks from the common language runtime (CLR):</span></span>  
  
- [<span data-ttu-id="46c53-116">ICorProfilerCallback::ExceptionCatcherEnter</span><span class="sxs-lookup"><span data-stu-id="46c53-116">ICorProfilerCallback::ExceptionCatcherEnter</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptioncatcherenter-method.md)  
  
- [<span data-ttu-id="46c53-117">ICorProfilerCallback::ExceptionUnwindFinallyEnter</span><span class="sxs-lookup"><span data-stu-id="46c53-117">ICorProfilerCallback::ExceptionUnwindFinallyEnter</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionunwindfinallyenter-method.md)  
  
- [<span data-ttu-id="46c53-118">ICorProfilerCallback::ExceptionSearchFilterEnter</span><span class="sxs-lookup"><span data-stu-id="46c53-118">ICorProfilerCallback::ExceptionSearchFilterEnter</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfilterenter-method.md)  
  
- [<span data-ttu-id="46c53-119">ICorProfilerCallback::ExceptionCatcherLeave</span><span class="sxs-lookup"><span data-stu-id="46c53-119">ICorProfilerCallback::ExceptionCatcherLeave</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptioncatcherleave-method.md)  
  
- [<span data-ttu-id="46c53-120">ICorProfilerCallback::ExceptionUnwindFinallyLeave</span><span class="sxs-lookup"><span data-stu-id="46c53-120">ICorProfilerCallback::ExceptionUnwindFinallyLeave</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionunwindfinallyleave-method.md)  
  
- [<span data-ttu-id="46c53-121">ICorProfilerCallback::ExceptionSearchFilterLeave</span><span class="sxs-lookup"><span data-stu-id="46c53-121">ICorProfilerCallback::ExceptionSearchFilterLeave</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfilterleave-method.md)  
  
## <a name="requirements"></a><span data-ttu-id="46c53-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46c53-122">Requirements</span></span>  
 <span data-ttu-id="46c53-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="46c53-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46c53-124">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="46c53-124">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="46c53-125">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="46c53-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="46c53-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46c53-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46c53-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46c53-127">See also</span></span>

- [<span data-ttu-id="46c53-128">Structures de profilage</span><span class="sxs-lookup"><span data-stu-id="46c53-128">Profiling Structures</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-structures.md)
