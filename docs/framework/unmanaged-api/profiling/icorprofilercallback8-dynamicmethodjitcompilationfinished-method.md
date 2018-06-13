---
title: ICorProfilerCallback8::DynamicMethodJITCompilationFinished (méthode)
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback8.DynamicMethodJITCompilationFinished
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 49b5ead8b5428d855b7dab81dced1de6325fd07b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33454995"
---
# <a name="icorprofilercallback8dynamicmethodjitcompilationfinished-method"></a><span data-ttu-id="7b6ec-102">ICorProfilerCallback8::DynamicMethodJITCompilationFinished (méthode)</span><span class="sxs-lookup"><span data-stu-id="7b6ec-102">ICorProfilerCallback8::DynamicMethodJITCompilationFinished Method</span></span>
<span data-ttu-id="7b6ec-103">[Pris en charge dans le .NET Framework 4.7 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="7b6ec-103">[Supported in the .NET Framework 4.7 and later versions]</span></span>  
  
<span data-ttu-id="7b6ec-104">Notifie le profileur chaque fois que la compilation JIT d’une méthode dynamique est terminée.</span><span class="sxs-lookup"><span data-stu-id="7b6ec-104">Notifies the profiler whenever JIT compilation of a dynamic method has completed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b6ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b6ec-105">Syntax</span></span>  
  
```  
HRESULT DynamicMethodJITCompilationFinished(  
     [in]  FunctionID  functionId,   
     [in]  BOOL        hrStatus,   
     [in]  BOOL        fIsSafeToBlock   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7b6ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b6ec-106">Parameters</span></span>  
<span data-ttu-id="7b6ec-107">[in] `functionId`</span><span class="sxs-lookup"><span data-stu-id="7b6ec-107">[in] `functionId`</span></span>  
<span data-ttu-id="7b6ec-108">Identificateur de la fonction en mémoire pour le JIT début de la compilation.</span><span class="sxs-lookup"><span data-stu-id="7b6ec-108">The identifier of the in-memory function for which JIT compilation is started.</span></span>   

<span data-ttu-id="7b6ec-109">[in] `hrStatus` </span><span class="sxs-lookup"><span data-stu-id="7b6ec-109">[in] `hrStatus` </span></span>  
<span data-ttu-id="7b6ec-110">Une valeur qui indique si la compilation JIT a réussi.</span><span class="sxs-lookup"><span data-stu-id="7b6ec-110">A value that indicates whether the JIT compilation was successful.</span></span>

<span data-ttu-id="7b6ec-111">[in] `fIsSafeToBlock` </span><span class="sxs-lookup"><span data-stu-id="7b6ec-111">[in] `fIsSafeToBlock` </span></span>  
<span data-ttu-id="7b6ec-112">`true` pour indiquer que le blocage peut entraîner l’exécution pour attendre que le thread appelant à retourner à partir de ce rappel ; `false` pour indiquer que le blocage n’affecte pas le fonctionnement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="7b6ec-112">`true` to indicate that blocking may cause the runtime to wait for the calling thread to return from this callback; `false` to indicate that blocking will not affect the operation of the runtime.</span></span>  

## <a name="remarks"></a><span data-ttu-id="7b6ec-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7b6ec-113">Remarks</span></span>  

<span data-ttu-id="7b6ec-114">Ce rappel est déclenché chaque fois que la compilation JIT d’une méthode dynamique est terminée.</span><span class="sxs-lookup"><span data-stu-id="7b6ec-114">This callback is triggered whenever JIT compilation of a dynamic method has finished.</span></span> <span data-ttu-id="7b6ec-115">Cela inclut divers des stubs de code IL et les méthodes LCG.</span><span class="sxs-lookup"><span data-stu-id="7b6ec-115">This includes various IL stubs and LCG methods.</span></span> <span data-ttu-id="7b6ec-116">Son objectif est de fournir des auteurs de profileur avec suffisamment d’informations pour identifier la méthode compilée pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7b6ec-116">Its goal is to provide profiler writers with enough information to identify the compiled method to users.</span></span>

> [!NOTE]
> <span data-ttu-id="7b6ec-117">`functionId` Impossible d’utiliser les valeurs pour résoudre leurs jetons de métadonnées, car les méthodes dynamiques ont pas de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="7b6ec-117">`functionId` values cannot be used to resolve to their metadata tokens, because dynamic methods have no metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b6ec-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7b6ec-118">Requirements</span></span>  
 <span data-ttu-id="7b6ec-119">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7b6ec-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7b6ec-120">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7b6ec-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7b6ec-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7b6ec-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7b6ec-122">**Versions du .NET framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="7b6ec-122">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b6ec-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b6ec-123">See Also</span></span>  
 [<span data-ttu-id="7b6ec-124">DynamicMethodJITCompilationStarted (méthode)</span><span class="sxs-lookup"><span data-stu-id="7b6ec-124">DynamicMethodJITCompilationStarted Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)  
 [<span data-ttu-id="7b6ec-125">Interface de ICorProfilerCallback8</span><span class="sxs-lookup"><span data-stu-id="7b6ec-125">ICorProfilerCallback8 Interface</span></span>](icorprofilercallback8-interface.md)
