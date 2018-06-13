---
title: ICorDebugChain::GetActiveFrame, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetActiveFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetActiveFrame
helpviewer_keywords:
- ICorDebugChain::GetActiveFrame method [.NET Framework debugging]
- GetActiveFrame method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: 36887017-670b-4f21-b406-8fab956f84a3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a104d4d3cc74a6c1cb343818c9b0b3e8978b97df
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402797"
---
# <a name="icordebugchaingetactiveframe-method"></a><span data-ttu-id="2548c-102">ICorDebugChain::GetActiveFrame, méthode</span><span class="sxs-lookup"><span data-stu-id="2548c-102">ICorDebugChain::GetActiveFrame Method</span></span>
<span data-ttu-id="2548c-103">Obtient l’active (autrement dit, la plus récente) frame sur la chaîne.</span><span class="sxs-lookup"><span data-stu-id="2548c-103">Gets the active (that is, most recent) frame on the chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2548c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2548c-104">Syntax</span></span>  
  
```  
HRESULT GetActiveFrame (  
    [out] ICorDebugFrame   **ppFrame  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2548c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2548c-105">Parameters</span></span>  
 `ppFrame`  
 <span data-ttu-id="2548c-106">[out] Un pointeur vers l’adresse d’un objet ICorDebugFrame qui représente l’actif (autrement dit, la plus récente) frame sur la chaîne.</span><span class="sxs-lookup"><span data-stu-id="2548c-106">[out] A pointer to the address of an ICorDebugFrame object that represents the active (that is, most recent) frame on the chain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2548c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="2548c-107">Remarks</span></span>  
 <span data-ttu-id="2548c-108">Si aucun frame de pile managé n’est disponible, `ppFrame` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="2548c-108">If no managed stack frame is available, `ppFrame` is set to null.</span></span>  
  
 <span data-ttu-id="2548c-109">Si le frame actif n’est pas disponible, l’appel réussi et `ppFrame` sera null.</span><span class="sxs-lookup"><span data-stu-id="2548c-109">If the active frame is not available, the call will succeed and `ppFrame` will be null.</span></span> <span data-ttu-id="2548c-110">Cadres active ne sera pas disponibles pour les chaînes initiées en raison de CHAIN_ENTER_UNMANAGED et pour certaines chaînes initiées en raison de CHAIN_CLASS_INIT.</span><span class="sxs-lookup"><span data-stu-id="2548c-110">Active frames will not be available for chains initiated due to CHAIN_ENTER_UNMANAGED, and for some chains initiated due to CHAIN_CLASS_INIT.</span></span> <span data-ttu-id="2548c-111">Consultez l’énumération CorDebugChainReason.</span><span class="sxs-lookup"><span data-stu-id="2548c-111">See the CorDebugChainReason enumeration.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2548c-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2548c-112">Requirements</span></span>  
 <span data-ttu-id="2548c-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2548c-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2548c-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2548c-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2548c-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2548c-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2548c-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2548c-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
