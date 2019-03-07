---
title: ICorDebugThread::CreateEval, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread.CreateEval
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::CreateEval
helpviewer_keywords:
- CreateEval method [.NET Framework debugging]
- ICorDebugThread::CreateEval method [.NET Framework debugging]
ms.assetid: 36605067-33d3-4579-9c72-fb0e551ab0f1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2016795e7b2c0588e2bd69e764fb96f7f90b24d0
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57480661"
---
# <a name="icordebugthreadcreateeval-method"></a><span data-ttu-id="a5bb4-102">ICorDebugThread::CreateEval, méthode</span><span class="sxs-lookup"><span data-stu-id="a5bb4-102">ICorDebugThread::CreateEval Method</span></span>
<span data-ttu-id="a5bb4-103">Crée un objet ICorDebugEval qui recueille et expose les fonctionnalités de ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-103">Creates an ICorDebugEval object that collects and exposes the functionality of this ICorDebugThread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a5bb4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5bb4-104">Syntax</span></span>  
  
```  
HRESULT CreateEval (  
    [out] ICorDebugEval   **ppEval  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a5bb4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5bb4-105">Parameters</span></span>  
 `ppEval`  
 <span data-ttu-id="a5bb4-106">[out] Un pointeur vers l’adresse d’un `ICorDebugEval` objet qui recueille et expose les fonctionnalités de ce thread.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-106">[out] A pointer to the address of an `ICorDebugEval` object that collects and exposes the functionality of this thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a5bb4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a5bb4-107">Remarks</span></span>  
 <span data-ttu-id="a5bb4-108">L’objet d’évaluation envoie une nouvelle chaîne sur le thread avant de procéder à son calcul.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-108">The evaluation object will push a new chain on the thread before doing its computation.</span></span> <span data-ttu-id="a5bb4-109">Cela interrompt le calcul en cours d’exécution sur le thread jusqu'à ce que la version d’évaluation se termine.</span><span class="sxs-lookup"><span data-stu-id="a5bb4-109">This interrupts the computation currently being performed on the thread until the evaluation completes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a5bb4-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a5bb4-110">Requirements</span></span>  
 <span data-ttu-id="a5bb4-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a5bb4-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a5bb4-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a5bb4-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a5bb4-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a5bb4-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a5bb4-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a5bb4-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
