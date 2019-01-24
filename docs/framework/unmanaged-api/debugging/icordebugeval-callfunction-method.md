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
ms.openlocfilehash: 493b4850436b3724287210878992d1d8ce8fe168
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54589397"
---
# <a name="icordebugevalcallfunction-method"></a><span data-ttu-id="86f6d-102">ICorDebugEval::CallFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="86f6d-102">ICorDebugEval::CallFunction Method</span></span>
<span data-ttu-id="86f6d-103">Définit un appel à la fonction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="86f6d-103">Sets up a call to the specified function.</span></span>  
  
 <span data-ttu-id="86f6d-104">Cette méthode est obsolète dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="86f6d-104">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="86f6d-105">Utilisez [ICorDebugEval2::CallParameterizedFunction](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="86f6d-105">Use [ICorDebugEval2::CallParameterizedFunction](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86f6d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86f6d-106">Syntax</span></span>  
  
```  
HRESULT CallFunction (  
    [in] ICorDebugFunction  *pFunction,  
    [in] ULONG32            nArgs,  
    [in, size_is(nArgs)] ICorDebugValue *ppArgs[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="86f6d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86f6d-107">Parameters</span></span>  
 `pFunction`  
 <span data-ttu-id="86f6d-108">[in] Pointeur vers un objet ICorDebugFunction qui spécifie la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="86f6d-108">[in] Pointer to an ICorDebugFunction object that specifies the function to be called.</span></span>  
  
 `nArgs`  
 <span data-ttu-id="86f6d-109">[in] Le nombre d’arguments pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="86f6d-109">[in] The number of arguments for the function.</span></span>  
  
 `ppArgs`  
 <span data-ttu-id="86f6d-110">[in] Tableau de pointeurs, chacun d’eux pointe vers un objet ICorDebugValue qui spécifie un argument à passer à la fonction.</span><span class="sxs-lookup"><span data-stu-id="86f6d-110">[in] An array of pointers, each of which points to an ICorDebugValue object that specifies an argument to be passed to the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="86f6d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="86f6d-111">Remarks</span></span>  
 <span data-ttu-id="86f6d-112">Si la fonction est virtuelle, `CallFunction` effectuera dispatch virtuel.</span><span class="sxs-lookup"><span data-stu-id="86f6d-112">If the function is virtual, `CallFunction` will perform virtual dispatch.</span></span> <span data-ttu-id="86f6d-113">Si la fonction est dans un domaine d’application différent, une transition se produit tant que tous les arguments sont également dans ce domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="86f6d-113">If the function is in a different application domain, a transition will occur as long as all arguments are also in that application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86f6d-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="86f6d-114">Requirements</span></span>  
 <span data-ttu-id="86f6d-115">**Plateformes :** WindowSee [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="86f6d-115">**Platforms:** WindowSee [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86f6d-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="86f6d-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="86f6d-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="86f6d-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="86f6d-118">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="86f6d-118">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86f6d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86f6d-119">See also</span></span>
- [<span data-ttu-id="86f6d-120">CallParameterizedFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="86f6d-120">CallParameterizedFunction Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md)
