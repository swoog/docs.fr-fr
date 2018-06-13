---
title: ICorDebugThread::GetUserState, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetUserState
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetUserState
helpviewer_keywords:
- GetUserState method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetUserState method [.NET Framework debugging]
ms.assetid: ae0cfd73-8ead-4d36-9310-dccaac9db0bd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 06ff8f0f13d7710d2d3d59aac4b5fdcadfe707be
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33418390"
---
# <a name="icordebugthreadgetuserstate-method"></a><span data-ttu-id="e2484-102">ICorDebugThread::GetUserState, méthode</span><span class="sxs-lookup"><span data-stu-id="e2484-102">ICorDebugThread::GetUserState Method</span></span>
<span data-ttu-id="e2484-103">Obtient l’état de l’utilisateur actuel de ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="e2484-103">Gets the current user state of this ICorDebugThread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2484-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2484-104">Syntax</span></span>  
  
```  
HRESULT GetUserState (  
    [out] CorDebugUserState   *pState  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e2484-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2484-105">Parameters</span></span>  
 `pState`  
 <span data-ttu-id="e2484-106">[out] Pointeur vers une combinaison d’opérations de bits des valeurs d’énumération CorDebugUserState qui décrivent l’état utilisateur actuel de ce thread.</span><span class="sxs-lookup"><span data-stu-id="e2484-106">[out] A pointer to a bitwise combination of CorDebugUserState enumeration values that describe the current user state of this thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e2484-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e2484-107">Remarks</span></span>  
 <span data-ttu-id="e2484-108">L’état utilisateur du thread est l’état du thread lorsqu’il est examiné par le programme est en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="e2484-108">The user state of the thread is the state of the thread when it is examined by the program that is being debugged.</span></span> <span data-ttu-id="e2484-109">Un thread peut avoir plusieurs bits d’état à définir.</span><span class="sxs-lookup"><span data-stu-id="e2484-109">A thread may have multiple state bits set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e2484-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e2484-110">Requirements</span></span>  
 <span data-ttu-id="e2484-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e2484-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e2484-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e2484-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e2484-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e2484-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e2484-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e2484-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
