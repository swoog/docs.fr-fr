---
title: ICorDebugProcess::IsOSSuspended, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.IsOSSuspended
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::IsOSSuspended
helpviewer_keywords:
- IsOSSuspended method [.NET Framework debugging]
- ICorDebugProcess::IsOSSuspended method [.NET Framework debugging]
ms.assetid: 83406cb2-5797-4402-872d-89c9516aefec
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 039dc0d9befb038e643abc4e2524c133234f460b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775561"
---
# <a name="icordebugprocessisossuspended-method"></a><span data-ttu-id="1fd1f-102">ICorDebugProcess::IsOSSuspended, méthode</span><span class="sxs-lookup"><span data-stu-id="1fd1f-102">ICorDebugProcess::IsOSSuspended Method</span></span>
<span data-ttu-id="1fd1f-103">Obtient une valeur qui indique si le thread spécifié a été interrompu suite à l’arrêt de ce processus de débogueur.</span><span class="sxs-lookup"><span data-stu-id="1fd1f-103">Gets a value that indicates whether the specified thread has been suspended as a result of the debugger stopping this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1fd1f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fd1f-104">Syntax</span></span>  
  
```  
HRESULT IsOSSuspended(  
    [in]  DWORD threadID,  
    [out] BOOL  *pbSuspended);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1fd1f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fd1f-105">Parameters</span></span>  
 `threadID`  
 <span data-ttu-id="1fd1f-106">[in] L’ID du thread en question.</span><span class="sxs-lookup"><span data-stu-id="1fd1f-106">[in] The ID of thread in question.</span></span>  
  
 `pbSuspended`  
 <span data-ttu-id="1fd1f-107">[out] Un pointeur vers une valeur booléenne qui est `true` si le thread spécifié a été suspendue ; sinon \*`pbSuspended` est `false`.</span><span class="sxs-lookup"><span data-stu-id="1fd1f-107">[out] A pointer to a Boolean value that is `true` if the specified thread has been suspended; otherwise \*`pbSuspended` is `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1fd1f-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1fd1f-108">Remarks</span></span>  
 <span data-ttu-id="1fd1f-109">Quand le thread spécifié a été suspendu suite à l’arrêt de ce processus de débogueur, le compteur de suspension Win32 du thread spécifié est incrémenté d’un.</span><span class="sxs-lookup"><span data-stu-id="1fd1f-109">When the specified thread has been suspended as a result of the debugger stopping this process, the specified thread's Win32 suspend count is incremented by one.</span></span> <span data-ttu-id="1fd1f-110">L’interface utilisateur (IU) du débogueur souhaiterez peut-être prendre en compte ces informations si elle affiche le système d’exploitation (OS) compteur de suspension du thread à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1fd1f-110">The debugger user interface (UI) may want to take this information into account if it displays the operating system (OS) suspend count of the thread to the user.</span></span>  
  
 <span data-ttu-id="1fd1f-111">Le `IsOSSuspended` méthode est pertinent uniquement dans le contexte de débogage non managé.</span><span class="sxs-lookup"><span data-stu-id="1fd1f-111">The `IsOSSuspended` method makes sense only in the context of unmanaged debugging.</span></span> <span data-ttu-id="1fd1f-112">Pendant le débogage managé, les threads sont coopération suspendu plutôt que du système d’exploitation suspendu.</span><span class="sxs-lookup"><span data-stu-id="1fd1f-112">During managed debugging, threads are cooperatively suspended rather than OS-suspended.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1fd1f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fd1f-113">Requirements</span></span>  
 <span data-ttu-id="1fd1f-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1fd1f-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1fd1f-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1fd1f-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1fd1f-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1fd1f-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1fd1f-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1fd1f-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
