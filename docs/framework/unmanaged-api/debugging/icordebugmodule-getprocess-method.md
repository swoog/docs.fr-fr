---
title: ICorDebugModule::GetProcess, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetProcess
helpviewer_keywords:
- GetProcess method, ICorDebugModule interface [.NET Framework debugging]
- ICorDebugModule::GetProcess method [.NET Framework debugging]
ms.assetid: 5e13446c-0271-446c-924a-9072c0e6eeae
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 97cecd66462cf6a88012b13dec82dbf617891dd5
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57493841"
---
# <a name="icordebugmodulegetprocess-method"></a><span data-ttu-id="fbd10-102">ICorDebugModule::GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="fbd10-102">ICorDebugModule::GetProcess Method</span></span>
<span data-ttu-id="fbd10-103">Obtient le processus contenant de ce module.</span><span class="sxs-lookup"><span data-stu-id="fbd10-103">Gets the containing process of this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fbd10-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbd10-104">Syntax</span></span>  
  
```  
HRESULT GetProcess (  
    [out] ICorDebugProcess **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fbd10-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbd10-105">Parameters</span></span>  
 `ppProcess`  
 <span data-ttu-id="fbd10-106">[out] Pointeur vers l’adresse d’un objet ICorDebugProcess qui représente le processus qui contient ce module.</span><span class="sxs-lookup"><span data-stu-id="fbd10-106">[out] A pointer to the address of an ICorDebugProcess object that represents the process containing this module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fbd10-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fbd10-107">Requirements</span></span>  
 <span data-ttu-id="fbd10-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fbd10-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fbd10-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fbd10-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fbd10-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fbd10-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fbd10-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fbd10-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
