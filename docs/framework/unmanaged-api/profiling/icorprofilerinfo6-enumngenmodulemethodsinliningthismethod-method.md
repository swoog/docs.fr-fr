---
title: ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod (méthode)
ms.date: 03/30/2017
ms.assetid: b933dfe6-7833-40cb-aad8-40842dc3034f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 564f3b1cdfab2a3020b6bb5ac8d9af03c6532c8b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33459669"
---
# <a name="icorprofilerinfo6enumngenmodulemethodsinliningthismethod-method"></a><span data-ttu-id="c8b72-102">ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod (méthode)</span><span class="sxs-lookup"><span data-stu-id="c8b72-102">ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod Method</span></span>
<span data-ttu-id="c8b72-103">[Pris en charge dans le .NET Framework 4.6 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="c8b72-103">[Supported in the .NET Framework 4.6 and later versions]</span></span>  
  
 <span data-ttu-id="c8b72-104">Retourne un énumérateur pour toutes les méthodes qui sont définis dans un module NGen donné et l’inline une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="c8b72-104">Returns an enumerator to all the methods that          are defined in  a given NGen module and          inline a given method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8b72-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8b72-105">Syntax</span></span>  
  
```  
HRESULT EnumNgenModuleMethodsInliningThisMethod(  
        [in] ModuleID inlinersModuleId,  
        [in] ModuleID inlineeModuleId,  
        [in] mdMethodDef inlineeMethodId,  
        [out] BOOL *incompleteData,  
        [out] ICorProfilerMethodEnum** ppEnum  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c8b72-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8b72-106">Parameters</span></span>  
 `inlinersModuleId`  
 <span data-ttu-id="c8b72-107">[in] L’identificateur d’un module NGen.</span><span class="sxs-lookup"><span data-stu-id="c8b72-107">[in] The identifier of an NGen module.</span></span>  
  
 `inlineeModuleId`  
 <span data-ttu-id="c8b72-108">[in] L’identificateur d’un module qui définit `inlineeMethodId`.</span><span class="sxs-lookup"><span data-stu-id="c8b72-108">[in] The identifier of a module that defines `inlineeMethodId`.</span></span> <span data-ttu-id="c8b72-109">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c8b72-109">See the Remarks section for more information.</span></span>  
  
 `inlineeMethodId`  
 <span data-ttu-id="c8b72-110">[in] L’identificateur d’une méthode inline.</span><span class="sxs-lookup"><span data-stu-id="c8b72-110">[in] The identifier of an inlined method.</span></span> <span data-ttu-id="c8b72-111">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c8b72-111">See the Remarks section for more information.</span></span>  
  
 `incompleteData`  
 <span data-ttu-id="c8b72-112">[out] Un indicateur qui indique si `ppEnum` contient toutes les méthodes d’incorporation (inlining) une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="c8b72-112">[out] A flag that indicates whether `ppEnum` contains all methods inlining a given method.</span></span>  <span data-ttu-id="c8b72-113">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c8b72-113">See the Remarks section for more information.</span></span>  
  
 `ppEnum`  
 <span data-ttu-id="c8b72-114">[out] Un pointeur vers l’adresse d’un énumérateur</span><span class="sxs-lookup"><span data-stu-id="c8b72-114">[out] A pointer to the address of an enumerator</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c8b72-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c8b72-115">Remarks</span></span>  
 <span data-ttu-id="c8b72-116">`inlineeModuleId` et `inlineeMethodId` forment l’identificateur complet de la méthode qui peut être inline.</span><span class="sxs-lookup"><span data-stu-id="c8b72-116">`inlineeModuleId` and `inlineeMethodId` together form the full identifier for the method that might be inlined.</span></span> <span data-ttu-id="c8b72-117">Par exemple, supposons que le module `A` définit une méthode `Simple.Add`:</span><span class="sxs-lookup"><span data-stu-id="c8b72-117">For example, assume module `A` defines a method `Simple.Add`:</span></span>  
  
```csharp  
Simple.Add(int a, int b)   
{ return a + b; }  
```  
  
 <span data-ttu-id="c8b72-118">module Bdefines et `Fancy.AddTwice`:</span><span class="sxs-lookup"><span data-stu-id="c8b72-118">and module Bdefines `Fancy.AddTwice`:</span></span>  
  
```csharp  
Fancy.AddTwice(int a, int b)   
{ return Simple.Add(a,b) + Simple.Add(a,b); }  
```  
  
 <span data-ttu-id="c8b72-119">Nous supposons également que `Fancy.AddTwice` intègre l’appel à `SimpleAdd`.</span><span class="sxs-lookup"><span data-stu-id="c8b72-119">Lets also assume that `Fancy.AddTwice` inlines the call to `SimpleAdd`.</span></span> <span data-ttu-id="c8b72-120">Un profileur peut utiliser cet énumérateur pour rechercher toutes les méthodes définies dans le module B qui inline `Simple.Add`, et le résultat serait énumérer `AddTwice`.</span><span class="sxs-lookup"><span data-stu-id="c8b72-120">A profiler could use this enumerator to find all methods defined in module B which inline `Simple.Add`, and the result would enumerate `AddTwice`.</span></span>  <span data-ttu-id="c8b72-121">`inlineeModuleId` est l’identificateur de module `A`, et `inlineeeMethodId` est l’identificateur de `Simple.Add(int a, int b)`.</span><span class="sxs-lookup"><span data-stu-id="c8b72-121">`inlineeModuleId` is the identifier of module `A`,   and `inlineeeMethodId` is the identifier of `Simple.Add(int a, int b)`.</span></span>  
  
 <span data-ttu-id="c8b72-122">Si `incompleteData` a la valeur true après la fonction retourne une valeur, l’énumérateur ne contient pas toutes les méthodes d’incorporation (inlining) une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="c8b72-122">If `incompleteData` is true after the function returns, the enumerator does not contain all methods inlining a given method.</span></span> <span data-ttu-id="c8b72-123">Cela peut se produire lorsqu’un ou plus de dépendances du module de personnes directes ou indirectes n’ont pas encore été chargés.</span><span class="sxs-lookup"><span data-stu-id="c8b72-123">This can happen when one or more direct or indirect dependencies of inliners module haven't been loaded yet.</span></span> <span data-ttu-id="c8b72-124">Si un profileur doit obtenir les données précises, il doit réessayer plus tard lorsque plusieurs modules sont chargés, de préférence à chaque chargement de module.</span><span class="sxs-lookup"><span data-stu-id="c8b72-124">If a profiler needs accurate data, it should retry later when more modules are loaded, preferably on each module load.</span></span>  
  
 <span data-ttu-id="c8b72-125">Le `EnumNgenModuleMethodsInliningThisMethod` méthode peut être utilisée pour contourner les limites sur incorporation (inlining) pour ReJIT.</span><span class="sxs-lookup"><span data-stu-id="c8b72-125">The `EnumNgenModuleMethodsInliningThisMethod` method can be used to work around limitations on inlining for ReJIT.</span></span> <span data-ttu-id="c8b72-126">ReJIT permet à un profileur modifier l’implémentation d’une méthode et puis créer un nouveau code pour celui-ci à la volée.</span><span class="sxs-lookup"><span data-stu-id="c8b72-126">ReJIT lets a profiler change the implementation of a method and then create new code for it on the fly.</span></span> <span data-ttu-id="c8b72-127">Par exemple, nous pouvons modifier `Simple.Add` comme suit :</span><span class="sxs-lookup"><span data-stu-id="c8b72-127">For example, we could change `Simple.Add` as follows:</span></span>  
  
```csharp  
Simple.Add(int a, int b)   
{ return 42; }  
```  
  
 <span data-ttu-id="c8b72-128">Toutefois, car `Fancy.AddTwice` a déjà inline `Simple.Add`, il continue à avoir le même comportement qu’avant.</span><span class="sxs-lookup"><span data-stu-id="c8b72-128">However because `Fancy.AddTwice` has already inlined `Simple.Add`, it continues to have the same behavior as before.</span></span> <span data-ttu-id="c8b72-129">Pour contourner cette limitation, l’appelant doit rechercher toutes les méthodes dans tous les modules dont inline `Simple.Add` et utiliser `ICorProfilerInfo5::RequestRejit` sur chacune de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c8b72-129">To work around that limitation, the caller has to search for all methods in all modules that inline `Simple.Add` and use `ICorProfilerInfo5::RequestRejit` on each of those methods.</span></span> <span data-ttu-id="c8b72-130">Lorsque les méthodes sont recompilés, ils ont le nouveau comportement de `Simple.Add` au lieu de l’ancien comportement.</span><span class="sxs-lookup"><span data-stu-id="c8b72-130">When the methods are re-compiled, they will have the new behavior of `Simple.Add` instead of the old behavior.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c8b72-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c8b72-131">Requirements</span></span>  
 <span data-ttu-id="c8b72-132">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c8b72-132">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c8b72-133">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c8b72-133">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c8b72-134">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c8b72-134">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c8b72-135">**Versions du .NET framework :** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c8b72-135">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c8b72-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8b72-136">See Also</span></span>  
 [<span data-ttu-id="c8b72-137">ICorProfilerInfo6, interface</span><span class="sxs-lookup"><span data-stu-id="c8b72-137">ICorProfilerInfo6 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo6-interface.md)
