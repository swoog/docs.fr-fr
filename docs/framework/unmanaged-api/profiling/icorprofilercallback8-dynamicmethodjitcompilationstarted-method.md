---
title: ICorProfilerCallback8::DynamicMethodJITCompilationStarted (méthode)
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback8.DynamicMethodJITCompilationStarted
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ad74eeb4deeae73be40b3a0bc0f6a18ec2299780
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33454748"
---
# <a name="icorprofilercallback8dynamicmethodjitcompilationstarted-method"></a><span data-ttu-id="7a3d5-102">ICorProfilerCallback8::DynamicMethodJITCompilationStarted (méthode)</span><span class="sxs-lookup"><span data-stu-id="7a3d5-102">ICorProfilerCallback8::DynamicMethodJITCompilationStarted Method</span></span>
<span data-ttu-id="7a3d5-103">[Pris en charge dans le .NET Framework 4.7 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="7a3d5-103">[Supported in the .NET Framework 4.7 and later versions]</span></span>  
  
<span data-ttu-id="7a3d5-104">Notifie le profileur chaque fois que la compilation JIT d’une méthode dynamique a démarré.</span><span class="sxs-lookup"><span data-stu-id="7a3d5-104">Notifies the profiler whenever JIT compilation of a dynamic method has started.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a3d5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a3d5-105">Syntax</span></span>  
  
```  
HRESULT DynamicMethodJITCompilationStarted(  
     [in]  FunctionID  functionId,   
     [in]  BOOL        fIsSafeToBlock,   
     [in]  LPCBYTE     pILHeader,   
     [in]  LONG        cbILHeader   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7a3d5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a3d5-106">Parameters</span></span>  
<span data-ttu-id="7a3d5-107">[in] `functionId`</span><span class="sxs-lookup"><span data-stu-id="7a3d5-107">[in] `functionId`</span></span>  
<span data-ttu-id="7a3d5-108">Identificateur de la fonction en mémoire pour le JIT début de la compilation.</span><span class="sxs-lookup"><span data-stu-id="7a3d5-108">The identifier of the in-memory function for which JIT compilation is started.</span></span>   

<span data-ttu-id="7a3d5-109">[in] `fIsSafeToBlock` </span><span class="sxs-lookup"><span data-stu-id="7a3d5-109">[in] `fIsSafeToBlock` </span></span>  
<span data-ttu-id="7a3d5-110">`true` pour indiquer que le blocage peut entraîner l’exécution pour attendre que le thread appelant à retourner à partir de ce rappel ; `false` pour indiquer que le blocage n’affecte pas le fonctionnement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="7a3d5-110">`true` to indicate that blocking may cause the runtime to wait for the calling thread to return from this callback; `false` to indicate that blocking will not affect the operation of the runtime.</span></span>  

<span data-ttu-id="7a3d5-111">[in] `pILHeader`  </span><span class="sxs-lookup"><span data-stu-id="7a3d5-111">[in] `pILHeader`  </span></span>  
<span data-ttu-id="7a3d5-112">Pointeur vers le premier octet de l’en-tête de la méthode IL.</span><span class="sxs-lookup"><span data-stu-id="7a3d5-112">A pointer to the first byte of the method's IL header.</span></span>   

<span data-ttu-id="7a3d5-113">[in] `cbILHeader`  </span><span class="sxs-lookup"><span data-stu-id="7a3d5-113">[in] `cbILHeader`  </span></span>  
<span data-ttu-id="7a3d5-114">Le nombre d’octets dans l’en-tête de langage intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="7a3d5-114">The number of bytes in the IL header.</span></span> 

## <a name="remarks"></a><span data-ttu-id="7a3d5-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7a3d5-115">Remarks</span></span>  

<span data-ttu-id="7a3d5-116">Ce rappel est déclenché chaque fois qu’une méthode dynamique est compilé par JIT.</span><span class="sxs-lookup"><span data-stu-id="7a3d5-116">This callback is triggered whenever a dynamic method is JIT-compiled.</span></span> <span data-ttu-id="7a3d5-117">Cela inclut divers des stubs de code IL et les méthodes LCG.</span><span class="sxs-lookup"><span data-stu-id="7a3d5-117">This includes various IL stubs and LCG methods.</span></span> <span data-ttu-id="7a3d5-118">Son objectif est de fournir des auteurs de profileur avec suffisamment d’informations pour identifier la méthode compilée pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7a3d5-118">Its goal is to provide profiler writers with enough information to identify the compiled method to users.</span></span>

> [!NOTE]
> <span data-ttu-id="7a3d5-119">`functionId` Impossible d’utiliser les valeurs pour résoudre leurs jetons de métadonnées, car les méthodes dynamiques ont pas de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="7a3d5-119">`functionId` values cannot be used to resolve to their metadata tokens, because dynamic methods have no metadata.</span></span>

<span data-ttu-id="7a3d5-120">Le `pILHeader` pointeur est uniquement valid pendant le rappel.</span><span class="sxs-lookup"><span data-stu-id="7a3d5-120">The `pILHeader` pointer is only valid during the callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a3d5-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7a3d5-121">Requirements</span></span>  
 <span data-ttu-id="7a3d5-122">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7a3d5-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a3d5-123">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7a3d5-123">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7a3d5-124">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7a3d5-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7a3d5-125">**Versions du .NET framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="7a3d5-125">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a3d5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a3d5-126">See Also</span></span>  
 [<span data-ttu-id="7a3d5-127">DynamicMethodJITCompilationFinished (méthode)</span><span class="sxs-lookup"><span data-stu-id="7a3d5-127">DynamicMethodJITCompilationFinished Method</span></span>](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)  
 [<span data-ttu-id="7a3d5-128">Interface de ICorProfilerCallback8</span><span class="sxs-lookup"><span data-stu-id="7a3d5-128">ICorProfilerCallback8 Interface</span></span>](icorprofilercallback8-interface.md)
