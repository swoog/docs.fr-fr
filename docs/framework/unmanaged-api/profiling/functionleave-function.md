---
title: FunctionLeave (fonction)
ms.date: 03/30/2017
api_name:
- FunctionLeave
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionLeave
helpviewer_keywords:
- FunctionLeave function [.NET Framework profiling]
ms.assetid: 18e89f45-e068-426a-be16-9f53a4346860
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2614ad988496a22f0e6234c2f3300e22ef548308
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452440"
---
# <a name="functionleave-function"></a><span data-ttu-id="90b6f-102">FunctionLeave (fonction)</span><span class="sxs-lookup"><span data-stu-id="90b6f-102">FunctionLeave Function</span></span>
<span data-ttu-id="90b6f-103">Notifie le profileur qu’une fonction est sur le point de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="90b6f-103">Notifies the profiler that a function is about to return to the caller.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="90b6f-104">Le `FunctionLeave` fonction est déconseillée dans le .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="90b6f-104">The `FunctionLeave` function is deprecated in the .NET Framework 2.0.</span></span> <span data-ttu-id="90b6f-105">Il continue de fonctionner, mais entraîne une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="90b6f-105">It will continue to work, but will incur a performance penalty.</span></span> <span data-ttu-id="90b6f-106">Utilisez le [FunctionLeave2](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md) de fonction à la place.</span><span class="sxs-lookup"><span data-stu-id="90b6f-106">Use the [FunctionLeave2](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md) function instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="90b6f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90b6f-107">Syntax</span></span>  
  
```  
void __stdcall FunctionLeave (  
    [in] FunctionID funcID  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="90b6f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90b6f-108">Parameters</span></span>  
 `funcID`  
 <span data-ttu-id="90b6f-109">[in] Identificateur de la fonction qui retourne.</span><span class="sxs-lookup"><span data-stu-id="90b6f-109">[in] The identifier of the function that is returning.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="90b6f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="90b6f-110">Remarks</span></span>  
 <span data-ttu-id="90b6f-111">Le `FunctionLeave` fonction est un rappel ; vous devez l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="90b6f-111">The `FunctionLeave` function is a callback; you must implement it.</span></span> <span data-ttu-id="90b6f-112">L’implémentation doit utiliser le `__declspec`(`naked`) attribut de classe de stockage.</span><span class="sxs-lookup"><span data-stu-id="90b6f-112">The implementation must use the `__declspec`(`naked`) storage-class attribute.</span></span>  
  
 <span data-ttu-id="90b6f-113">Le moteur d’exécution n’enregistre pas les registres avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="90b6f-113">The execution engine does not save any registers before calling this function.</span></span>  
  
-   <span data-ttu-id="90b6f-114">À l’entrée, vous devez enregistrer tous les registres que vous utilisez, y compris ceux de l’unité à virgule flottante (FPU).</span><span class="sxs-lookup"><span data-stu-id="90b6f-114">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
-   <span data-ttu-id="90b6f-115">À la sortie, vous devez restaurer la pile par extraire tous les paramètres qui ont été envoyées par son appelant.</span><span class="sxs-lookup"><span data-stu-id="90b6f-115">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
 <span data-ttu-id="90b6f-116">L’implémentation de `FunctionLeave` ne doivent pas bloquer, car il sera retarder le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="90b6f-116">The implementation of `FunctionLeave` should not block because it will delay garbage collection.</span></span> <span data-ttu-id="90b6f-117">L’implémentation ne doit pas tenter une opération garbage collection, car la pile est peut-être pas dans un état de nom convivial de la collection garbage.</span><span class="sxs-lookup"><span data-stu-id="90b6f-117">The implementation should not attempt a garbage collection because the stack may not be in a garbage collection-friendly state.</span></span> <span data-ttu-id="90b6f-118">Si un garbage collection est tenté, le runtime bloque jusqu'à ce que `FunctionLeave` retourne.</span><span class="sxs-lookup"><span data-stu-id="90b6f-118">If a garbage collection is attempted, the runtime will block until `FunctionLeave` returns.</span></span>  
  
 <span data-ttu-id="90b6f-119">En outre, le `FunctionLeave` (fonction) ne doit pas appeler dans du code managé ou de quelque manière qu’une allocation de mémoire managée.</span><span class="sxs-lookup"><span data-stu-id="90b6f-119">Also, the `FunctionLeave` function must not call into managed code or in any way cause a managed memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="90b6f-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="90b6f-120">Requirements</span></span>  
 <span data-ttu-id="90b6f-121">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="90b6f-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="90b6f-122">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="90b6f-122">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="90b6f-123">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="90b6f-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="90b6f-124">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="90b6f-124">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="90b6f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90b6f-125">See Also</span></span>  
 [<span data-ttu-id="90b6f-126">FunctionEnter2, fonction</span><span class="sxs-lookup"><span data-stu-id="90b6f-126">FunctionEnter2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md)  
 [<span data-ttu-id="90b6f-127">FunctionLeave2, fonction</span><span class="sxs-lookup"><span data-stu-id="90b6f-127">FunctionLeave2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md)  
 [<span data-ttu-id="90b6f-128">FunctionTailcall2, fonction</span><span class="sxs-lookup"><span data-stu-id="90b6f-128">FunctionTailcall2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md)  
 [<span data-ttu-id="90b6f-129">SetEnterLeaveFunctionHooks2, méthode</span><span class="sxs-lookup"><span data-stu-id="90b6f-129">SetEnterLeaveFunctionHooks2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md)  
 [<span data-ttu-id="90b6f-130">Fonctions statiques globales de profilage</span><span class="sxs-lookup"><span data-stu-id="90b6f-130">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
