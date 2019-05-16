---
title: ICorDebugEval::CallFunction, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval.CallFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::CallFunction
helpviewer_keywords:
- ICorDebugEval::CallFunction method [.NET Framework debugging]
- CallFunction method [.NET Framework debugging]
ms.assetid: 7f470c5c-e1c0-4d8d-aad8-830f113ae751
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 65225281fe3abaa20e69e96f4cd4d2a4b03a87ce
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65629943"
---
# <a name="icordebugevalcallfunction-method"></a><span data-ttu-id="9b397-102">ICorDebugEval::CallFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="9b397-102">ICorDebugEval::CallFunction Method</span></span>

<span data-ttu-id="9b397-103">Définit un appel à la fonction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9b397-103">Sets up a call to the specified function.</span></span>

<span data-ttu-id="9b397-104">Cette méthode est obsolète dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="9b397-104">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="9b397-105">Utilisez [ICorDebugEval2::CallParameterizedFunction](icordebugeval2-callparameterizedfunction-method.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="9b397-105">Use [ICorDebugEval2::CallParameterizedFunction](icordebugeval2-callparameterizedfunction-method.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b397-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b397-106">Syntax</span></span>

```cpp
HRESULT CallFunction (
    [in] ICorDebugFunction  *pFunction,
    [in] ULONG32            nArgs,
    [in, size_is(nArgs)] ICorDebugValue *ppArgs[]
);
```

## <a name="parameters"></a><span data-ttu-id="9b397-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b397-107">Parameters</span></span>

`pFunction`\
<span data-ttu-id="9b397-108">[in] Pointeur vers un objet ICorDebugFunction qui spécifie la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="9b397-108">[in] Pointer to an ICorDebugFunction object that specifies the function to be called.</span></span>

`nArgs`\
<span data-ttu-id="9b397-109">[in] Le nombre d’arguments pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="9b397-109">[in] The number of arguments for the function.</span></span>

`ppArgs`\
<span data-ttu-id="9b397-110">[in] Tableau de pointeurs, chacun d’eux pointe vers un objet ICorDebugValue qui spécifie un argument à passer à la fonction.</span><span class="sxs-lookup"><span data-stu-id="9b397-110">[in] An array of pointers, each of which points to an ICorDebugValue object that specifies an argument to be passed to the function.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b397-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9b397-111">Remarks</span></span>

<span data-ttu-id="9b397-112">Si la fonction est virtuelle, `CallFunction` effectuera dispatch virtuel.</span><span class="sxs-lookup"><span data-stu-id="9b397-112">If the function is virtual, `CallFunction` will perform virtual dispatch.</span></span> <span data-ttu-id="9b397-113">Si la fonction est dans un domaine d’application différent, une transition se produit tant que tous les arguments sont également dans ce domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="9b397-113">If the function is in a different application domain, a transition will occur as long as all arguments are also in that application domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b397-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b397-114">Requirements</span></span>

<span data-ttu-id="9b397-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9b397-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="9b397-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9b397-116">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="9b397-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9b397-117">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="9b397-118">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="9b397-118">**.NET Framework Versions:** 1.1, 1.0</span></span>

## <a name="see-also"></a><span data-ttu-id="9b397-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b397-119">See also</span></span>

- [<span data-ttu-id="9b397-120">CallParameterizedFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="9b397-120">CallParameterizedFunction Method</span></span>](icordebugeval2-callparameterizedfunction-method.md)
