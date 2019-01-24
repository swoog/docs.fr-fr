---
title: Icorprofilerinfo6::enumngenmodulemethodsinliningthismethod, méthode
ms.date: 03/30/2017
ms.assetid: b933dfe6-7833-40cb-aad8-40842dc3034f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 07b1c905e587708336ce690bbf3d187b2d21e5b9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54568151"
---
# <a name="icorprofilerinfo6enumngenmodulemethodsinliningthismethod-method"></a><span data-ttu-id="16014-102">Icorprofilerinfo6::enumngenmodulemethodsinliningthismethod, méthode</span><span class="sxs-lookup"><span data-stu-id="16014-102">ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod Method</span></span>
<span data-ttu-id="16014-103">[Pris en charge dans le .NET Framework 4.6 et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="16014-103">[Supported in the .NET Framework 4.6 and later versions]</span></span>  
  
 <span data-ttu-id="16014-104">Retourne un énumérateur pour toutes les méthodes qui sont définis dans un module NGen donné et un inline une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="16014-104">Returns an enumerator to all the methods that          are defined in  a given NGen module and          inline a given method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="16014-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16014-105">Syntax</span></span>  
  
```  
HRESULT EnumNgenModuleMethodsInliningThisMethod(  
        [in] ModuleID inlinersModuleId,  
        [in] ModuleID inlineeModuleId,  
        [in] mdMethodDef inlineeMethodId,  
        [out] BOOL *incompleteData,  
        [out] ICorProfilerMethodEnum** ppEnum  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="16014-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16014-106">Parameters</span></span>  
 `inlinersModuleId`  
 <span data-ttu-id="16014-107">[in] L’identificateur d’un module NGen.</span><span class="sxs-lookup"><span data-stu-id="16014-107">[in] The identifier of an NGen module.</span></span>  
  
 `inlineeModuleId`  
 <span data-ttu-id="16014-108">[in] L’identificateur d’un module qui définit `inlineeMethodId`.</span><span class="sxs-lookup"><span data-stu-id="16014-108">[in] The identifier of a module that defines `inlineeMethodId`.</span></span> <span data-ttu-id="16014-109">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="16014-109">See the Remarks section for more information.</span></span>  
  
 `inlineeMethodId`  
 <span data-ttu-id="16014-110">[in] L’identificateur d’une méthode inline.</span><span class="sxs-lookup"><span data-stu-id="16014-110">[in] The identifier of an inlined method.</span></span> <span data-ttu-id="16014-111">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="16014-111">See the Remarks section for more information.</span></span>  
  
 `incompleteData`  
 <span data-ttu-id="16014-112">[out] Un indicateur qui indique si `ppEnum` contient toutes les méthodes d’incorporation (inlining) une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="16014-112">[out] A flag that indicates whether `ppEnum` contains all methods inlining a given method.</span></span>  <span data-ttu-id="16014-113">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="16014-113">See the Remarks section for more information.</span></span>  
  
 `ppEnum`  
 <span data-ttu-id="16014-114">[out] Un pointeur vers l’adresse d’un énumérateur</span><span class="sxs-lookup"><span data-stu-id="16014-114">[out] A pointer to the address of an enumerator</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="16014-115">Notes</span><span class="sxs-lookup"><span data-stu-id="16014-115">Remarks</span></span>  
 <span data-ttu-id="16014-116">`inlineeModuleId` et `inlineeMethodId` forment l’identificateur complet de la méthode qui peut être inline.</span><span class="sxs-lookup"><span data-stu-id="16014-116">`inlineeModuleId` and `inlineeMethodId` together form the full identifier for the method that might be inlined.</span></span> <span data-ttu-id="16014-117">Par exemple, supposons que le module `A` définit une méthode `Simple.Add`:</span><span class="sxs-lookup"><span data-stu-id="16014-117">For example, assume module `A` defines a method `Simple.Add`:</span></span>  
  
```csharp  
Simple.Add(int a, int b)   
{ return a + b; }  
```  
  
 <span data-ttu-id="16014-118">module Bdefines et `Fancy.AddTwice`:</span><span class="sxs-lookup"><span data-stu-id="16014-118">and module Bdefines `Fancy.AddTwice`:</span></span>  
  
```csharp  
Fancy.AddTwice(int a, int b)   
{ return Simple.Add(a,b) + Simple.Add(a,b); }  
```  
  
 <span data-ttu-id="16014-119">Supposons également que `Fancy.AddTwice` inlines l’appel à `SimpleAdd`.</span><span class="sxs-lookup"><span data-stu-id="16014-119">Lets also assume that `Fancy.AddTwice` inlines the call to `SimpleAdd`.</span></span> <span data-ttu-id="16014-120">Un profileur peut utiliser cet énumérateur pour rechercher toutes les méthodes définies dans le module B qui inline `Simple.Add`, et le résultat serait énumérer `AddTwice`.</span><span class="sxs-lookup"><span data-stu-id="16014-120">A profiler could use this enumerator to find all methods defined in module B which inline `Simple.Add`, and the result would enumerate `AddTwice`.</span></span>  <span data-ttu-id="16014-121">`inlineeModuleId` est l’identificateur de module `A`, et `inlineeeMethodId` est l’identificateur de `Simple.Add(int a, int b)`.</span><span class="sxs-lookup"><span data-stu-id="16014-121">`inlineeModuleId` is the identifier of module `A`,   and `inlineeeMethodId` is the identifier of `Simple.Add(int a, int b)`.</span></span>  
  
 <span data-ttu-id="16014-122">Si `incompleteData` a la valeur true après la fonction est retournée, l’énumérateur ne contient pas toutes les méthodes d’incorporation (inlining) une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="16014-122">If `incompleteData` is true after the function returns, the enumerator does not contain all methods inlining a given method.</span></span> <span data-ttu-id="16014-123">Cela peut se produire lorsque l’une ou des dépendances plus directes ou indirectes du module de personnes n’ont pas encore été chargés.</span><span class="sxs-lookup"><span data-stu-id="16014-123">This can happen when one or more direct or indirect dependencies of inliners module haven't been loaded yet.</span></span> <span data-ttu-id="16014-124">Si un profileur doit obtenir les données précises, il doit réessayer plus tard lorsque plusieurs modules sont chargés, de préférence à chaque chargement de module.</span><span class="sxs-lookup"><span data-stu-id="16014-124">If a profiler needs accurate data, it should retry later when more modules are loaded, preferably on each module load.</span></span>  
  
 <span data-ttu-id="16014-125">Le `EnumNgenModuleMethodsInliningThisMethod` méthode peut être utilisée pour contourner les limitations sur incorporation (inlining) pour ReJIT.</span><span class="sxs-lookup"><span data-stu-id="16014-125">The `EnumNgenModuleMethodsInliningThisMethod` method can be used to work around limitations on inlining for ReJIT.</span></span> <span data-ttu-id="16014-126">ReJIT permet un profileur de modifier l’implémentation d’une méthode et puis créez un nouveau code pour celui-ci à la volée.</span><span class="sxs-lookup"><span data-stu-id="16014-126">ReJIT lets a profiler change the implementation of a method and then create new code for it on the fly.</span></span> <span data-ttu-id="16014-127">Par exemple, nous pourrions modifier `Simple.Add` comme suit :</span><span class="sxs-lookup"><span data-stu-id="16014-127">For example, we could change `Simple.Add` as follows:</span></span>  
  
```csharp  
Simple.Add(int a, int b)   
{ return 42; }  
```  
  
 <span data-ttu-id="16014-128">Toutefois, car `Fancy.AddTwice` a déjà inline `Simple.Add`, il continue à avoir le même comportement qu’avant.</span><span class="sxs-lookup"><span data-stu-id="16014-128">However because `Fancy.AddTwice` has already inlined `Simple.Add`, it continues to have the same behavior as before.</span></span> <span data-ttu-id="16014-129">Pour contourner cette limitation, l’appelant doit rechercher toutes les méthodes dans tous les modules en ligne `Simple.Add` et utiliser `ICorProfilerInfo5::RequestRejit` sur chacune de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="16014-129">To work around that limitation, the caller has to search for all methods in all modules that inline `Simple.Add` and use `ICorProfilerInfo5::RequestRejit` on each of those methods.</span></span> <span data-ttu-id="16014-130">Lorsque les méthodes sont recompilés, ils ont le nouveau comportement `Simple.Add` au lieu de l’ancien comportement.</span><span class="sxs-lookup"><span data-stu-id="16014-130">When the methods are re-compiled, they will have the new behavior of `Simple.Add` instead of the old behavior.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="16014-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="16014-131">Requirements</span></span>  
 <span data-ttu-id="16014-132">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="16014-132">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="16014-133">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="16014-133">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="16014-134">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="16014-134">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="16014-135">**Versions du .NET Framework :** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="16014-135">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="16014-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16014-136">See also</span></span>
- [<span data-ttu-id="16014-137">ICorProfilerInfo6, interface</span><span class="sxs-lookup"><span data-stu-id="16014-137">ICorProfilerInfo6 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo6-interface.md)
