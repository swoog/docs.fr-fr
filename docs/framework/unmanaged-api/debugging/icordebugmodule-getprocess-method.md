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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61987998"
---
# <a name="icordebugmodulegetprocess-method"></a><span data-ttu-id="b4c78-102">ICorDebugModule::GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="b4c78-102">ICorDebugModule::GetProcess Method</span></span>
<span data-ttu-id="b4c78-103">Obtient le processus contenant de ce module.</span><span class="sxs-lookup"><span data-stu-id="b4c78-103">Gets the containing process of this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b4c78-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4c78-104">Syntax</span></span>  
  
```  
HRESULT GetProcess (  
    [out] ICorDebugProcess **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b4c78-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4c78-105">Parameters</span></span>  
 `ppProcess`  
 <span data-ttu-id="b4c78-106">[out] Pointeur vers l’adresse d’un objet ICorDebugProcess qui représente le processus qui contient ce module.</span><span class="sxs-lookup"><span data-stu-id="b4c78-106">[out] A pointer to the address of an ICorDebugProcess object that represents the process containing this module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b4c78-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4c78-107">Requirements</span></span>  
 <span data-ttu-id="b4c78-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b4c78-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b4c78-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b4c78-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b4c78-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b4c78-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b4c78-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b4c78-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
