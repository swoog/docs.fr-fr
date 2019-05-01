---
title: ICorDebugProcess::GetID, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.GetID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::GetID
helpviewer_keywords:
- GetID method, ICorDebugProcess interface [.NET Framework debugging]
- ICorDebugProcess::GetID method [.NET Framework debugging]
ms.assetid: b0ba8453-fa7e-4c14-93e5-335409cd4a47
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7d9239ccfe8ce08e5b50b762a6fede11ab8a439b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994489"
---
# <a name="icordebugprocessgetid-method"></a><span data-ttu-id="568ee-102">ICorDebugProcess::GetID, méthode</span><span class="sxs-lookup"><span data-stu-id="568ee-102">ICorDebugProcess::GetID Method</span></span>
<span data-ttu-id="568ee-103">Obtient l’ID de système d’exploitation (se) du processus.</span><span class="sxs-lookup"><span data-stu-id="568ee-103">Gets the operating system (OS) ID of the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="568ee-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="568ee-104">Syntax</span></span>  
  
```  
HRESULT GetID([out] DWORD *pdwProcessId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="568ee-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="568ee-105">Parameters</span></span>  
 `pdwProcessId`  
 <span data-ttu-id="568ee-106">[out] ID unique du processus.</span><span class="sxs-lookup"><span data-stu-id="568ee-106">[out] The unique ID of the process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="568ee-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="568ee-107">Requirements</span></span>  
 <span data-ttu-id="568ee-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="568ee-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="568ee-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="568ee-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="568ee-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="568ee-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="568ee-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="568ee-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
