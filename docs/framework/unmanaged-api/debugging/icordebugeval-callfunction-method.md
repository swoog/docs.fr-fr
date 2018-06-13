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
ms.openlocfilehash: 86d48461c601b53d4461331a11a0e0ac7ddc6e7c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33412544"
---
# <a name="icordebugevalcallfunction-method"></a><span data-ttu-id="55d7e-102">ICorDebugEval::CallFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="55d7e-102">ICorDebugEval::CallFunction Method</span></span>
<span data-ttu-id="55d7e-103">Définit un appel à la fonction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="55d7e-103">Sets up a call to the specified function.</span></span>  
  
 <span data-ttu-id="55d7e-104">Cette méthode est obsolète dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="55d7e-104">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="55d7e-105">Utilisez [ICorDebugEval2::CallParameterizedFunction](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="55d7e-105">Use [ICorDebugEval2::CallParameterizedFunction](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55d7e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55d7e-106">Syntax</span></span>  
  
```  
HRESULT CallFunction (  
    [in] ICorDebugFunction  *pFunction,  
    [in] ULONG32            nArgs,  
    [in, size_is(nArgs)] ICorDebugValue *ppArgs[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="55d7e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55d7e-107">Parameters</span></span>  
 `pFunction`  
 <span data-ttu-id="55d7e-108">[in] Pointeur vers un objet ICorDebugFunction qui spécifie la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="55d7e-108">[in] Pointer to an ICorDebugFunction object that specifies the function to be called.</span></span>  
  
 `nArgs`  
 <span data-ttu-id="55d7e-109">[in] Le nombre d’arguments pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="55d7e-109">[in] The number of arguments for the function.</span></span>  
  
 `ppArgs`  
 <span data-ttu-id="55d7e-110">[in] Tableau de pointeurs, chacun pointant vers un objet ICorDebugValue qui spécifie un argument à passer à la fonction.</span><span class="sxs-lookup"><span data-stu-id="55d7e-110">[in] An array of pointers, each of which points to an ICorDebugValue object that specifies an argument to be passed to the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="55d7e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="55d7e-111">Remarks</span></span>  
 <span data-ttu-id="55d7e-112">Si la fonction est virtuelle, `CallFunction` exécute une répartition virtuelle.</span><span class="sxs-lookup"><span data-stu-id="55d7e-112">If the function is virtual, `CallFunction` will perform virtual dispatch.</span></span> <span data-ttu-id="55d7e-113">Si la fonction est dans un domaine d’application différent, une transition se produit tant que tous les arguments sont également inclus dans ce domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="55d7e-113">If the function is in a different application domain, a transition will occur as long as all arguments are also in that application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="55d7e-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="55d7e-114">Requirements</span></span>  
 <span data-ttu-id="55d7e-115">**Plateformes :** WindowSee [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="55d7e-115">**Platforms:** WindowSee [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="55d7e-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="55d7e-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="55d7e-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="55d7e-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="55d7e-118">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="55d7e-118">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="55d7e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55d7e-119">See Also</span></span>  
 [<span data-ttu-id="55d7e-120">CallParameterizedFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="55d7e-120">CallParameterizedFunction Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md)
