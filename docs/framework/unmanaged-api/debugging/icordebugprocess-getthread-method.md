---
title: ICorDebugProcess::GetThread, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.GetThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::GetThread
helpviewer_keywords:
- ICorDebugProcess::GetThread method [.NET Framework debugging]
- GetThread method, ICorDebugProcess interface [.NET Framework debugging]
ms.assetid: a48261ed-700b-41c9-8cb4-18c526546603
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 36070d5374a11daf4b7800481c86d61057989631
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57470074"
---
# <a name="icordebugprocessgetthread-method"></a><span data-ttu-id="d8b78-102">ICorDebugProcess::GetThread, méthode</span><span class="sxs-lookup"><span data-stu-id="d8b78-102">ICorDebugProcess::GetThread Method</span></span>
<span data-ttu-id="d8b78-103">Obtient le thread du processus ayant l’ID de thread de système d’exploitation spécifié (système d’exploitation).</span><span class="sxs-lookup"><span data-stu-id="d8b78-103">Gets this process's thread that has the specified operating system (OS) thread ID.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8b78-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8b78-104">Syntax</span></span>  
  
```  
HRESULT GetThread(  
    [in] DWORD dwThreadId,  
    [out] ICorDebugThread **ppThread);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d8b78-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8b78-105">Parameters</span></span>  
 `dwThreadId`  
 <span data-ttu-id="d8b78-106">[in] Le système d’exploitation de thread ID du thread à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d8b78-106">[in] The OS thread ID of the thread to be retrieved.</span></span>  
  
 `ppThread`  
 <span data-ttu-id="d8b78-107">[out] Pointeur vers l’adresse d’un objet ICorDebugThread qui représente le thread.</span><span class="sxs-lookup"><span data-stu-id="d8b78-107">[out] A pointer to the address of an ICorDebugThread object that represents the thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8b78-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d8b78-108">Requirements</span></span>  
 <span data-ttu-id="d8b78-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d8b78-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8b78-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d8b78-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d8b78-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d8b78-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d8b78-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8b78-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
