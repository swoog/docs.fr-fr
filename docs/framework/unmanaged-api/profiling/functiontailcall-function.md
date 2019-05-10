---
title: FunctionTailcall (fonction)
ms.date: 03/30/2017
api_name:
- FunctionTailcall
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionTailcall
helpviewer_keywords:
- FunctionTailcall function [.NET Framework profiling]
ms.assetid: 66347e03-9a97-41e8-8f9d-89b80803f7b5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4686710c105ef002fe30f8b6e167d760088913ce
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64586996"
---
# <a name="functiontailcall-function"></a><span data-ttu-id="150c9-102">FunctionTailcall (fonction)</span><span class="sxs-lookup"><span data-stu-id="150c9-102">FunctionTailcall Function</span></span>
<span data-ttu-id="150c9-103">Notifie le profileur que la fonction en cours d’exécution est sur le point d’effectuer un appel tail à une autre fonction.</span><span class="sxs-lookup"><span data-stu-id="150c9-103">Notifies the profiler that the currently executing function is about to perform a tail call to another function.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="150c9-104">Le `FunctionTailcall` fonction est déconseillée dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="150c9-104">The `FunctionTailcall` function is deprecated in the .NET Framework version 2.0.</span></span> <span data-ttu-id="150c9-105">Il continue de fonctionner, mais entraîne une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="150c9-105">It will continue to work, but will incur a performance penalty.</span></span> <span data-ttu-id="150c9-106">Utilisez le [FunctionTailcall2](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md) fonctionner à la place.</span><span class="sxs-lookup"><span data-stu-id="150c9-106">Use the [FunctionTailcall2](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md) function instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="150c9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="150c9-107">Syntax</span></span>  
  
```  
void __stdcall FunctionTailcall (  
    [in] FunctionID funcID  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="150c9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="150c9-108">Parameters</span></span>  
 `funcID`  
 <span data-ttu-id="150c9-109">[in] L’identificateur de la fonction en cours d’exécution qui doit faire un appel tail.</span><span class="sxs-lookup"><span data-stu-id="150c9-109">[in] The identifier of the currently executing function that is about to make a tail call.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="150c9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="150c9-110">Remarks</span></span>  
 <span data-ttu-id="150c9-111">La fonction de la cible de l’appel tail utilisera le frame de pile actuel et retournera directement à l’appelant de la fonction qui fait l’appel tail.</span><span class="sxs-lookup"><span data-stu-id="150c9-111">The target function of the tail call will use the current stack frame, and will return directly to the caller of the function that made the tail call.</span></span> <span data-ttu-id="150c9-112">Cela signifie qu’un [FunctionLeave](../../../../docs/framework/unmanaged-api/profiling/functionleave-function.md) rappel ne sera pas émis pour une fonction qui est la cible d’un appel tail.</span><span class="sxs-lookup"><span data-stu-id="150c9-112">This means that a [FunctionLeave](../../../../docs/framework/unmanaged-api/profiling/functionleave-function.md) callback will not be issued for a function that is the target of a tail call.</span></span>  
  
 <span data-ttu-id="150c9-113">Le `FunctionTailcall` fonction est un rappel ; vous devez l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="150c9-113">The `FunctionTailcall` function is a callback; you must implement it.</span></span> <span data-ttu-id="150c9-114">L’implémentation doit utiliser le `__declspec`(`naked`) attribut de classe de stockage.</span><span class="sxs-lookup"><span data-stu-id="150c9-114">The implementation must use the `__declspec`(`naked`) storage-class attribute.</span></span>  
  
 <span data-ttu-id="150c9-115">Le moteur d’exécution n’enregistre pas les registres avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="150c9-115">The execution engine does not save any registers before calling this function.</span></span>  
  
- <span data-ttu-id="150c9-116">À l’entrée, vous devez enregistrer tous les registres que vous utilisez, y compris celles dans l’unité de virgule flottante (FPU).</span><span class="sxs-lookup"><span data-stu-id="150c9-116">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
- <span data-ttu-id="150c9-117">À la sortie, vous devez restaurer la pile en dépilant tous les paramètres qui ont été envoyés par son appelant.</span><span class="sxs-lookup"><span data-stu-id="150c9-117">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
 <span data-ttu-id="150c9-118">L’implémentation de `FunctionTailcall` ne doivent pas bloquer, car il sera retarder le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="150c9-118">The implementation of `FunctionTailcall` should not block because it will delay garbage collection.</span></span> <span data-ttu-id="150c9-119">L’implémentation ne doit pas tenter un garbage collection, car la pile est peut-être pas à l’état garbage collection convivial.</span><span class="sxs-lookup"><span data-stu-id="150c9-119">The implementation should not attempt a garbage collection because the stack may not be in a garbage collection-friendly state.</span></span> <span data-ttu-id="150c9-120">Si un garbage collection est tenté, le runtime bloque jusqu'à ce que `FunctionTailcall` retourne.</span><span class="sxs-lookup"><span data-stu-id="150c9-120">If a garbage collection is attempted, the runtime will block until `FunctionTailcall` returns.</span></span>  
  
 <span data-ttu-id="150c9-121">En outre, le `FunctionTailcall` (fonction) ne doit pas appeler dans du code managé ou de quelque manière qu’une allocation de mémoire managée.</span><span class="sxs-lookup"><span data-stu-id="150c9-121">Also, the `FunctionTailcall` function must not call into managed code or in any way cause a managed memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="150c9-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="150c9-122">Requirements</span></span>  
 <span data-ttu-id="150c9-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="150c9-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="150c9-124">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="150c9-124">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="150c9-125">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="150c9-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="150c9-126">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="150c9-126">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="150c9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="150c9-127">See also</span></span>

- [<span data-ttu-id="150c9-128">FunctionEnter2, fonction</span><span class="sxs-lookup"><span data-stu-id="150c9-128">FunctionEnter2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md)
- [<span data-ttu-id="150c9-129">FunctionLeave2, fonction</span><span class="sxs-lookup"><span data-stu-id="150c9-129">FunctionLeave2 Function</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md)
- [<span data-ttu-id="150c9-130">SetEnterLeaveFunctionHooks2, méthode</span><span class="sxs-lookup"><span data-stu-id="150c9-130">SetEnterLeaveFunctionHooks2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md)
- [<span data-ttu-id="150c9-131">Fonctions statiques globales de profilage</span><span class="sxs-lookup"><span data-stu-id="150c9-131">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
