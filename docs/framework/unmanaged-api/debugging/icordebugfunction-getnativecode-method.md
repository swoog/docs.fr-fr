---
title: ICorDebugFunction::GetNativeCode, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetNativeCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetNativeCode
helpviewer_keywords:
- GetNativeCode method [.NET Framework debugging]
- ICorDebugFunction::GetNativeCode method [.NET Framework debugging]
ms.assetid: c8a34916-0eef-4987-8d29-c8bcb4be9cf6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e1cb073c1f93c6d60d86e5160dcfb0cbdaf1cd33
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33414569"
---
# <a name="icordebugfunctiongetnativecode-method"></a><span data-ttu-id="f394b-102">ICorDebugFunction::GetNativeCode, méthode</span><span class="sxs-lookup"><span data-stu-id="f394b-102">ICorDebugFunction::GetNativeCode Method</span></span>
<span data-ttu-id="f394b-103">Obtient le code natif pour la fonction qui est représentée par cette instance ICorDebugFunction.</span><span class="sxs-lookup"><span data-stu-id="f394b-103">Gets the native code for the function that is represented by this ICorDebugFunction instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f394b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f394b-104">Syntax</span></span>  
  
```  
HRESULT GetNativeCode (  
    [out] ICorDebugCode **ppCode  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f394b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f394b-105">Parameters</span></span>  
 `ppCode`  
 <span data-ttu-id="f394b-106">[out] Pointeur vers l’instance ICorDebugCode qui représente le code natif pour cette fonction, ou null, si cette fonction est le code Microsoft intermediate language (MSIL) qui n’a pas été compilé juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="f394b-106">[out] A pointer to the ICorDebugCode instance that represents the native code for this function, or null, if this function is Microsoft intermediate language (MSIL) code that has not been just-in-time (JIT) compiled.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f394b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f394b-107">Remarks</span></span>  
 <span data-ttu-id="f394b-108">Si la fonction qui est représentée par ce `ICorDebugFunction` instance a été compilé par JIT plusieurs fois, comme dans le cas des types génériques, `GetNativeCode` retourne un objet de code natif aléatoire.</span><span class="sxs-lookup"><span data-stu-id="f394b-108">If the function that is represented by this `ICorDebugFunction` instance has been JIT-compiled more than once, as in the case of generic types, `GetNativeCode` returns a random native code object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f394b-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f394b-109">Requirements</span></span>  
 <span data-ttu-id="f394b-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f394b-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f394b-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f394b-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f394b-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f394b-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f394b-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f394b-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
