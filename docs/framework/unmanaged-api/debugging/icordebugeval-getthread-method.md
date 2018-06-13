---
title: ICorDebugEval::GetThread, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval.GetThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::GetThread
helpviewer_keywords:
- GetThread method, ICorDebugEval interface [.NET Framework debugging]
- ICorDebugEval::GetThread method [.NET Framework debugging]
ms.assetid: 57163b0d-c8a7-44af-9078-e7a895d29f9a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e64bc173717c3121d6c2b101f734ee325a0ced53
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33413759"
---
# <a name="icordebugevalgetthread-method"></a><span data-ttu-id="df495-102">ICorDebugEval::GetThread, méthode</span><span class="sxs-lookup"><span data-stu-id="df495-102">ICorDebugEval::GetThread Method</span></span>
<span data-ttu-id="df495-103">Obtient le thread dans lequel cette évaluation s’exécute ou s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="df495-103">Gets the thread in which this evaluation is executing or will execute.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df495-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df495-104">Syntax</span></span>  
  
```  
HRESULT GetThread (  
    [out] ICorDebugThread   **ppThread  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="df495-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df495-105">Parameters</span></span>  
 `ppThread`  
 <span data-ttu-id="df495-106">[out] Pointeur vers l’adresse d’un objet ICorDebugThread qui représente le thread.</span><span class="sxs-lookup"><span data-stu-id="df495-106">[out] A pointer to the address of an ICorDebugThread object that represents the thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="df495-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="df495-107">Requirements</span></span>  
 <span data-ttu-id="df495-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="df495-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="df495-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="df495-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="df495-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="df495-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="df495-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="df495-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
