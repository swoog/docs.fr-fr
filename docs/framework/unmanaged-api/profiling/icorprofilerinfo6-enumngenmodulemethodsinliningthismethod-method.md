---
title: Icorprofilerinfo6::enumngenmodulemethodsinliningthismethod, méthode
ms.date: 03/30/2017
ms.assetid: b933dfe6-7833-40cb-aad8-40842dc3034f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 67ae413ae8944757fc90bcde752b9a5fe53cc68f
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57365319"
---
# <a name="icorprofilerinfo6enumngenmodulemethodsinliningthismethod-method"></a><span data-ttu-id="ce0c7-102">Icorprofilerinfo6::enumngenmodulemethodsinliningthismethod, méthode</span><span class="sxs-lookup"><span data-stu-id="ce0c7-102">ICorProfilerInfo6::EnumNgenModuleMethodsInliningThisMethod Method</span></span>

<span data-ttu-id="ce0c7-103">Retourne un énumérateur pour toutes les méthodes qui sont définis dans un module NGen donné et un inline une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-103">Returns an enumerator to all the methods that are defined in a given NGen module and inline a given method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce0c7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce0c7-104">Syntax</span></span>

```cpp
HRESULT EnumNgenModuleMethodsInliningThisMethod(
        [in] ModuleID inlinersModuleId,
        [in] ModuleID inlineeModuleId,
        [in] mdMethodDef inlineeMethodId,
        [out] BOOL *incompleteData,
        [out] ICorProfilerMethodEnum** ppEnum
);
```

## <a name="parameters"></a><span data-ttu-id="ce0c7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce0c7-105">Parameters</span></span>

`inlinersModuleId`\
<span data-ttu-id="ce0c7-106">[in] L’identificateur d’un module NGen.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-106">[in] The identifier of an NGen module.</span></span>

`inlineeModuleId`\
<span data-ttu-id="ce0c7-107">[in] L’identificateur d’un module qui définit `inlineeMethodId`.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-107">[in] The identifier of a module that defines `inlineeMethodId`.</span></span> <span data-ttu-id="ce0c7-108">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-108">See the Remarks section for more information.</span></span>

`inlineeMethodId`\
<span data-ttu-id="ce0c7-109">[in] L’identificateur d’une méthode inline.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-109">[in] The identifier of an inlined method.</span></span> <span data-ttu-id="ce0c7-110">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-110">See the Remarks section for more information.</span></span>

`incompleteData`\
<span data-ttu-id="ce0c7-111">[out] Un indicateur qui indique si `ppEnum` contient toutes les méthodes d’incorporation (inlining) une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-111">[out] A flag that indicates whether `ppEnum` contains all methods inlining a given method.</span></span>  <span data-ttu-id="ce0c7-112">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-112">See the Remarks section for more information.</span></span>

`ppEnum`\
<span data-ttu-id="ce0c7-113">[out] Un pointeur vers l’adresse d’un énumérateur</span><span class="sxs-lookup"><span data-stu-id="ce0c7-113">[out] A pointer to the address of an enumerator</span></span>

## <a name="remarks"></a><span data-ttu-id="ce0c7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ce0c7-114">Remarks</span></span>

<span data-ttu-id="ce0c7-115">`inlineeModuleId` et `inlineeMethodId` forment l’identificateur complet de la méthode qui peut être inline.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-115">`inlineeModuleId` and `inlineeMethodId` together form the full identifier for the method that might be inlined.</span></span> <span data-ttu-id="ce0c7-116">Par exemple, supposons que le module `A` définit une méthode `Simple.Add`:</span><span class="sxs-lookup"><span data-stu-id="ce0c7-116">For example, assume module `A` defines a method `Simple.Add`:</span></span>

```csharp
Simple.Add(int a, int b)
{ return a + b; }
```

<span data-ttu-id="ce0c7-117">et le module B définit `Fancy.AddTwice`:</span><span class="sxs-lookup"><span data-stu-id="ce0c7-117">and module B defines `Fancy.AddTwice`:</span></span>

```csharp
Fancy.AddTwice(int a, int b)
{ return Simple.Add(a,b) + Simple.Add(a,b); }
```

<span data-ttu-id="ce0c7-118">Supposons également que `Fancy.AddTwice` inlines l’appel à `SimpleAdd`.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-118">Lets also assume that `Fancy.AddTwice` inlines the call to `SimpleAdd`.</span></span> <span data-ttu-id="ce0c7-119">Un profileur peut utiliser cet énumérateur pour rechercher toutes les méthodes définies dans le module B qui inline `Simple.Add`, et le résultat serait énumérer `AddTwice`.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-119">A profiler could use this enumerator to find all methods defined in module B which inline `Simple.Add`, and the result would enumerate `AddTwice`.</span></span>  <span data-ttu-id="ce0c7-120">`inlineeModuleId` est l’identificateur de module `A`, et `inlineeMethodId` est l’identificateur de `Simple.Add(int a, int b)`.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-120">`inlineeModuleId` is the identifier of module `A`, and `inlineeMethodId` is the identifier of `Simple.Add(int a, int b)`.</span></span>

<span data-ttu-id="ce0c7-121">Si `incompleteData` a la valeur true après la fonction est retournée, l’énumérateur ne contient pas toutes les méthodes d’incorporation (inlining) une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-121">If `incompleteData` is true after the function returns, the enumerator does not contain all methods inlining a given method.</span></span> <span data-ttu-id="ce0c7-122">Cela peut se produire lorsque l’une ou des dépendances plus directes ou indirectes du module de personnes n’ont pas encore été chargés.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-122">This can happen when one or more direct or indirect dependencies of inliners module haven't been loaded yet.</span></span> <span data-ttu-id="ce0c7-123">Si un profileur doit obtenir les données précises, il doit réessayer plus tard lorsque plusieurs modules sont chargés, de préférence à chaque chargement de module.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-123">If a profiler needs accurate data, it should retry later when more modules are loaded, preferably on each module load.</span></span>

<span data-ttu-id="ce0c7-124">Le `EnumNgenModuleMethodsInliningThisMethod` méthode peut être utilisée pour contourner les limitations sur incorporation (inlining) pour ReJIT.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-124">The `EnumNgenModuleMethodsInliningThisMethod` method can be used to work around limitations on inlining for ReJIT.</span></span> <span data-ttu-id="ce0c7-125">ReJIT permet un profileur de modifier l’implémentation d’une méthode et puis créez un nouveau code pour celui-ci à la volée.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-125">ReJIT lets a profiler change the implementation of a method and then create new code for it on the fly.</span></span> <span data-ttu-id="ce0c7-126">Par exemple, nous pourrions modifier `Simple.Add` comme suit :</span><span class="sxs-lookup"><span data-stu-id="ce0c7-126">For example, we could change `Simple.Add` as follows:</span></span>

```csharp
Simple.Add(int a, int b)
{ return 42; }
```

<span data-ttu-id="ce0c7-127">Toutefois, car `Fancy.AddTwice` a déjà inline `Simple.Add`, il continue à avoir le même comportement qu’avant.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-127">However because `Fancy.AddTwice` has already inlined `Simple.Add`, it continues to have the same behavior as before.</span></span> <span data-ttu-id="ce0c7-128">Pour contourner cette limitation, l’appelant doit rechercher toutes les méthodes dans tous les modules en ligne `Simple.Add` et utiliser `ICorProfilerInfo5::RequestRejit` sur chacune de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-128">To work around that limitation, the caller has to search for all methods in all modules that inline `Simple.Add` and use `ICorProfilerInfo5::RequestRejit` on each of those methods.</span></span> <span data-ttu-id="ce0c7-129">Lorsque les méthodes sont recompilés, ils ont le nouveau comportement `Simple.Add` au lieu de l’ancien comportement.</span><span class="sxs-lookup"><span data-stu-id="ce0c7-129">When the methods are re-compiled, they will have the new behavior of `Simple.Add` instead of the old behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce0c7-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ce0c7-130">Requirements</span></span>

<span data-ttu-id="ce0c7-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ce0c7-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="ce0c7-132">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ce0c7-132">**Header:** CorProf.idl, CorProf.h</span></span>

<span data-ttu-id="ce0c7-133">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ce0c7-133">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="ce0c7-134">**Versions du .NET Framework :** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ce0c7-134">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="ce0c7-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce0c7-135">See also</span></span>

- [<span data-ttu-id="ce0c7-136">ICorProfilerInfo6, interface</span><span class="sxs-lookup"><span data-stu-id="ce0c7-136">ICorProfilerInfo6 Interface</span></span>](icorprofilerinfo6-interface.md)