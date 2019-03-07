---
title: ICorDebugFunction2::GetVersionNumber, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFunction2.GetVersionNumber
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction2::GetVersionNumber
helpviewer_keywords:
- ICorDebugFunction2::GetVersionNumber method [.NET Framework debugging]
- GetVersionNumber method, ICorDebugFunction2 interface [.NET Framework debugging]
ms.assetid: e3a1ce48-9bb9-4ed6-a5fe-5e1819a6333f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6cc9c2af62184c83857b82445941f6087a05c2c3
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57497169"
---
# <a name="icordebugfunction2getversionnumber-method"></a><span data-ttu-id="0abb0-102">ICorDebugFunction2::GetVersionNumber, méthode</span><span class="sxs-lookup"><span data-stu-id="0abb0-102">ICorDebugFunction2::GetVersionNumber Method</span></span>
<span data-ttu-id="0abb0-103">Obtient la version Modifier & Continuer de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="0abb0-103">Gets the Edit and Continue version of this function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0abb0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0abb0-104">Syntax</span></span>  
  
```  
HRESULT GetVersionNumber (  
    [out] ULONG32   *pnVersion  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0abb0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0abb0-105">Parameters</span></span>  
 `pnVersion`  
 <span data-ttu-id="0abb0-106">[out] Pointeur vers un entier qui représente le numéro de version de la fonction qui est représentée par cet objet ICorDebugFunction2.</span><span class="sxs-lookup"><span data-stu-id="0abb0-106">[out] A pointer to an integer that is the version number of the function that is represented by this ICorDebugFunction2 object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0abb0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0abb0-107">Remarks</span></span>  
 <span data-ttu-id="0abb0-108">Le runtime conserve une trace du nombre de modifications qui ont eu lieu pour chaque module pendant une session de débogage.</span><span class="sxs-lookup"><span data-stu-id="0abb0-108">The runtime keeps track of the number of edits that have taken place to each module during a debug session.</span></span> <span data-ttu-id="0abb0-109">Le numéro de version d’une fonction est un supérieur au nombre de la modification qui a introduit la fonction.</span><span class="sxs-lookup"><span data-stu-id="0abb0-109">The version number of a function is one more than the number of the edit that introduced the function.</span></span> <span data-ttu-id="0abb0-110">Version d’origine de la fonction est 1.</span><span class="sxs-lookup"><span data-stu-id="0abb0-110">The function's original version is version 1.</span></span> <span data-ttu-id="0abb0-111">Le nombre est incrémenté chaque fois pour un module [ICorDebugModule2::ApplyChanges](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-applychanges-method.md) est appelée sur ce module.</span><span class="sxs-lookup"><span data-stu-id="0abb0-111">The number is incremented for a module every time [ICorDebugModule2::ApplyChanges](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-applychanges-method.md) is called on that module.</span></span> <span data-ttu-id="0abb0-112">Par conséquent, si le corps d’une fonction a été remplacé dans le premier et le troisième appel à `ICorDebugModule2::ApplyChanges`, `GetVersionNumber` peut retourner la version 1, 2 ou 4 de cette fonction, mais pas la version 3.</span><span class="sxs-lookup"><span data-stu-id="0abb0-112">Thus, if a function’s body was replaced in the first and third call to `ICorDebugModule2::ApplyChanges`, `GetVersionNumber` may return version 1, 2, or 4 for that function, but not version 3.</span></span> <span data-ttu-id="0abb0-113">(Cette fonction n’aurait aucune version 3).</span><span class="sxs-lookup"><span data-stu-id="0abb0-113">(That function would have no version 3.)</span></span>  
  
 <span data-ttu-id="0abb0-114">Le numéro de version est suivi séparément pour chaque module.</span><span class="sxs-lookup"><span data-stu-id="0abb0-114">The version number is tracked separately for each module.</span></span> <span data-ttu-id="0abb0-115">Par conséquent, si vous effectuez quatre modifications sur le Module 1 et aucune sur le Module 2, votre modification suivante sur le Module 1 affecte un numéro de version 6 à toutes les fonctions modifiées dans le Module 1.</span><span class="sxs-lookup"><span data-stu-id="0abb0-115">So, if you perform four edits on Module 1, and none on Module 2, your next edit on Module 1 will assign a version number of 6 to all the edited functions in Module 1.</span></span> <span data-ttu-id="0abb0-116">Si la même modification affecte le Module 2, les fonctions du Module 2 obtiendra un numéro de version 2.</span><span class="sxs-lookup"><span data-stu-id="0abb0-116">If the same edit touches Module 2, the functions in Module 2 will get a version number of 2.</span></span>  
  
 <span data-ttu-id="0abb0-117">Le numéro de version obtenu par le `GetVersionNumber` méthode peut être inférieur à celui obtenu par [ICorDebugFunction::GetCurrentVersionNumber](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getcurrentversionnumber-method.md).</span><span class="sxs-lookup"><span data-stu-id="0abb0-117">The version number obtained by the `GetVersionNumber` method may be lower than that obtained by [ICorDebugFunction::GetCurrentVersionNumber](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getcurrentversionnumber-method.md).</span></span>  
  
 <span data-ttu-id="0abb0-118">Le [ICorDebugCode::GetVersionNumber](../../../../docs/framework/unmanaged-api/debugging/icordebugcode-getversionnumber-method.md) méthode effectue la même opération que `ICorDebugFunction2::GetVersionNumber`.</span><span class="sxs-lookup"><span data-stu-id="0abb0-118">The [ICorDebugCode::GetVersionNumber](../../../../docs/framework/unmanaged-api/debugging/icordebugcode-getversionnumber-method.md) method performs the same operation as `ICorDebugFunction2::GetVersionNumber`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0abb0-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0abb0-119">Requirements</span></span>  
 <span data-ttu-id="0abb0-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0abb0-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0abb0-121">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0abb0-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0abb0-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0abb0-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0abb0-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0abb0-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
