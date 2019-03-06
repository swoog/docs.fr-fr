---
title: IMethodMalloc::Alloc, méthode
ms.date: 03/30/2017
api_name:
- IMethodMalloc.Alloc
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- IMethodMalloc::Alloc
helpviewer_keywords:
- IMethodMalloc::Alloc method [.NET Framework profiling]
- Alloc method, IMethodMalloc interface [.NET Framework profiling]
ms.assetid: 8653bd4c-2290-43d2-a3e1-cbbd50033f4f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9a676989bdc6866f85fabe3e15b1e6b7b8b5a9a9
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57351253"
---
# <a name="imethodmallocalloc-method"></a><span data-ttu-id="fa9db-102">IMethodMalloc::Alloc, méthode</span><span class="sxs-lookup"><span data-stu-id="fa9db-102">IMethodMalloc::Alloc Method</span></span>

<span data-ttu-id="fa9db-103">Tente d’allouer une quantité de mémoire spécifiée pour un nouveau corps de fonction Microsoft intermediate language (MSIL).</span><span class="sxs-lookup"><span data-stu-id="fa9db-103">Attempts to allocate a specified amount of memory for a new Microsoft intermediate language (MSIL) function body.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa9db-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa9db-104">Syntax</span></span>

```cpp
PVOID Alloc (
    [in] ULONG   cb
);
```

## <a name="parameters"></a><span data-ttu-id="fa9db-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa9db-105">Parameters</span></span>

`cb`\
<span data-ttu-id="fa9db-106">[in] Le nombre d’octets à allouer pour le corps de méthode.</span><span class="sxs-lookup"><span data-stu-id="fa9db-106">[in] The number of bytes to allocate for the method body.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa9db-107">Notes</span><span class="sxs-lookup"><span data-stu-id="fa9db-107">Remarks</span></span>

 <span data-ttu-id="fa9db-108">La mémoire allouée commencera à une adresse supérieure à l’adresse de base du module qui est associé à cet allocateur.</span><span class="sxs-lookup"><span data-stu-id="fa9db-108">The allocated memory will begin at an address greater than the base address of the module that is associated with this allocator.</span></span> <span data-ttu-id="fa9db-109">En d’autres termes, chaque allocateur est créé pour un module particulier et tentera d’allouer de mémoire à un décalage positif à partir de son adresse de base.</span><span class="sxs-lookup"><span data-stu-id="fa9db-109">In other words, each allocator is created for a particular module, and will attempt to allocate memory at a positive offset from its base address.</span></span> <span data-ttu-id="fa9db-110">Si `Alloc` ne parvient pas à allouer le nombre requis d’octets à une adresse supérieure à l’adresse de base du module, il retourne E_OUTOFMEMORY, quelle que soit la quantité réelle d’espace mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="fa9db-110">If `Alloc` fails to allocate the requested number of bytes at an address greater than the base address of the module, it returns E_OUTOFMEMORY, regardless of the actual amount of memory space available.</span></span>

 <span data-ttu-id="fa9db-111">Le `Alloc` méthode doit être utilisée conjointement avec la [ICorProfilerInfo::SetILFunctionBody](icorprofilerinfo-setilfunctionbody-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="fa9db-111">The `Alloc` method should be used in conjunction with the [ICorProfilerInfo::SetILFunctionBody](icorprofilerinfo-setilfunctionbody-method.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa9db-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fa9db-112">Requirements</span></span>
 <span data-ttu-id="fa9db-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fa9db-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

 <span data-ttu-id="fa9db-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="fa9db-114">**Header:** CorProf.idl, CorProf.h</span></span>

 <span data-ttu-id="fa9db-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fa9db-115">**Library:** CorGuids.lib</span></span>

 <span data-ttu-id="fa9db-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fa9db-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="fa9db-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa9db-117">See also</span></span>

- [<span data-ttu-id="fa9db-118">IMethodMalloc, interface</span><span class="sxs-lookup"><span data-stu-id="fa9db-118">IMethodMalloc Interface</span></span>](imethodmalloc-interface.md)