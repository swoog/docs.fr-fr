---
title: ICorDebugProcess::GetHandle, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.GetHandle
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::GetHandle
helpviewer_keywords:
- GetHandle method, ICorDebugProcess interface [.NET Framework debugging]
- ICorDebugProcess::GetHandle method [.NET Framework debugging]
ms.assetid: e7d3ecf5-09d2-4d94-abb6-ff3483deebb6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 60bd7567f541a0bbaa3591d2f2905d13064dec3c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33423440"
---
# <a name="icordebugprocessgethandle-method"></a><span data-ttu-id="284ce-102">ICorDebugProcess::GetHandle, méthode</span><span class="sxs-lookup"><span data-stu-id="284ce-102">ICorDebugProcess::GetHandle Method</span></span>
<span data-ttu-id="284ce-103">Obtient un handle vers le processus.</span><span class="sxs-lookup"><span data-stu-id="284ce-103">Gets a handle to the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="284ce-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="284ce-104">Syntax</span></span>  
  
```  
HRESULT GetHandle([out] HPROCESS *phProcessHandle);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="284ce-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="284ce-105">Parameters</span></span>  
 `phProcessHandle`  
 <span data-ttu-id="284ce-106">[out] Un pointeur vers un `HPROCESS` qui est le handle du processus.</span><span class="sxs-lookup"><span data-stu-id="284ce-106">[out] A pointer to an `HPROCESS` that is the handle to the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="284ce-107">Notes</span><span class="sxs-lookup"><span data-stu-id="284ce-107">Remarks</span></span>  
 <span data-ttu-id="284ce-108">Le handle récupéré appartient à l’interface de débogage.</span><span class="sxs-lookup"><span data-stu-id="284ce-108">The retrieved handle is owned by the debugging interface.</span></span> <span data-ttu-id="284ce-109">Le débogueur doit dupliquer le handle avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="284ce-109">The debugger should duplicate the handle before using it.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="284ce-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="284ce-110">Requirements</span></span>  
 <span data-ttu-id="284ce-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="284ce-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="284ce-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="284ce-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="284ce-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="284ce-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="284ce-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="284ce-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
