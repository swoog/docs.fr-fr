---
title: FunctionEnter (fonction)
ms.date: 03/30/2017
api_name:
- FunctionEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionEnter
helpviewer_keywords:
- FunctionEnter function [.NET Framework profiling]
ms.assetid: bf4ffa50-4506-4dd4-aa13-a0457b47ca74
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 77de59de8fcf3797237245ce42c7f0eaa96d3d24
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33451780"
---
# <a name="functionenter-function"></a><span data-ttu-id="1ab18-102">FunctionEnter (fonction)</span><span class="sxs-lookup"><span data-stu-id="1ab18-102">FunctionEnter Function</span></span>
<span data-ttu-id="1ab18-103">Notifie le profileur que le contrôle est passé à une fonction.</span><span class="sxs-lookup"><span data-stu-id="1ab18-103">Notifies the profiler that control is being passed to a function.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1ab18-104">Le `FunctionEnter` fonction est déconseillée dans le .NET Framework version 2.0, et son utilisation peut entraîner une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="1ab18-104">The `FunctionEnter` function is deprecated in the .NET Framework version 2.0, and its use will incur a performance penalty.</span></span> <span data-ttu-id="1ab18-105">Utilisez le [FunctionEnter2](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md) de fonction à la place.</span><span class="sxs-lookup"><span data-stu-id="1ab18-105">Use the [FunctionEnter2](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md) function instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ab18-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ab18-106">Syntax</span></span>  
  
```  
void __stdcall FunctionEnter (  
    [in]  FunctionID funcID  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1ab18-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ab18-107">Parameters</span></span>  
 `funcID`  
 <span data-ttu-id="1ab18-108">[in] Identificateur de la fonction à laquelle le contrôle est passé.</span><span class="sxs-lookup"><span data-stu-id="1ab18-108">[in] The identifier of the function to which control is passed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1ab18-109">Notes</span><span class="sxs-lookup"><span data-stu-id="1ab18-109">Remarks</span></span>  
 <span data-ttu-id="1ab18-110">Le `FunctionEnter` fonction est un rappel ; vous devez l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="1ab18-110">The `FunctionEnter` function is a callback; you must implement it.</span></span> <span data-ttu-id="1ab18-111">L’implémentation doit utiliser le `__declspec`(`naked`) attribut de classe de stockage.</span><span class="sxs-lookup"><span data-stu-id="1ab18-111">The implementation must use the `__declspec`(`naked`) storage-class attribute.</span></span>  
  
 <span data-ttu-id="1ab18-112">Le moteur d’exécution n’enregistre pas les registres avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="1ab18-112">The execution engine does not save any registers before calling this function.</span></span>  
  
-   <span data-ttu-id="1ab18-113">À l’entrée, vous devez enregistrer tous les registres que vous utilisez, y compris ceux de l’unité à virgule flottante (FPU).</span><span class="sxs-lookup"><span data-stu-id="1ab18-113">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
-   <span data-ttu-id="1ab18-114">À la sortie, vous devez restaurer la pile par extraire tous les paramètres qui ont été envoyées par son appelant.</span><span class="sxs-lookup"><span data-stu-id="1ab18-114">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
 <span data-ttu-id="1ab18-115">L’implémentation de `FunctionEnter` ne doivent pas bloquer, car il sera retarder le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="1ab18-115">The implementation of `FunctionEnter` should not block because it will delay garbage collection.</span></span> <span data-ttu-id="1ab18-116">L’implémentation ne doit pas tenter une opération garbage collection, car la pile est peut-être pas dans un état de nom convivial de la collection garbage.</span><span class="sxs-lookup"><span data-stu-id="1ab18-116">The implementation should not attempt a garbage collection because the stack may not be in a garbage collection-friendly state.</span></span> <span data-ttu-id="1ab18-117">Si un garbage collection est tenté, le runtime bloque jusqu'à ce que `FunctionEnter` retourne.</span><span class="sxs-lookup"><span data-stu-id="1ab18-117">If a garbage collection is attempted, the runtime will block until `FunctionEnter` returns.</span></span>  
  
 <span data-ttu-id="1ab18-118">En outre, le `FunctionEnter` (fonction) ne doit pas appeler dans du code managé ou de quelque manière qu’une allocation de mémoire managée.</span><span class="sxs-lookup"><span data-stu-id="1ab18-118">Also, the `FunctionEnter` function must not call into managed code or in any way cause a managed memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1ab18-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1ab18-119">Requirements</span></span>  
 <span data-ttu-id="1ab18-120">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1ab18-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1ab18-121">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="1ab18-121">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="1ab18-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1ab18-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1ab18-123">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="1ab18-123">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ab18-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ab18-124">See Also</span></span>  
 [<span data-ttu-id="1ab18-125">FunctionEnter2, fonction</span><span class="sxs-lookup"><span data-stu-id="1ab18-125">FunctionEnter2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md)  
 [<span data-ttu-id="1ab18-126">FunctionLeave2, fonction</span><span class="sxs-lookup"><span data-stu-id="1ab18-126">FunctionLeave2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md)  
 [<span data-ttu-id="1ab18-127">FunctionTailcall2, fonction</span><span class="sxs-lookup"><span data-stu-id="1ab18-127">FunctionTailcall2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md)  
 [<span data-ttu-id="1ab18-128">SetEnterLeaveFunctionHooks2, méthode</span><span class="sxs-lookup"><span data-stu-id="1ab18-128">SetEnterLeaveFunctionHooks2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md)  
 [<span data-ttu-id="1ab18-129">Fonctions statiques globales de profilage</span><span class="sxs-lookup"><span data-stu-id="1ab18-129">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
