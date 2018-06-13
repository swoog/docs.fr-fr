---
title: ICorDebugModule::GetAssembly, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetAssembly
helpviewer_keywords:
- ICorDebugModule::GetAssembly method [.NET Framework debugging]
- GetAssembly method [.NET Framework debugging]
ms.assetid: 989762c4-3d15-4485-b8ee-69e0fa8ec895
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 78bfc91bdd0f9fa68252c6a07e1362807eb507b4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416021"
---
# <a name="icordebugmodulegetassembly-method"></a><span data-ttu-id="8ad31-102">ICorDebugModule::GetAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="8ad31-102">ICorDebugModule::GetAssembly Method</span></span>
<span data-ttu-id="8ad31-103">Obtient l’assembly contenant de ce module.</span><span class="sxs-lookup"><span data-stu-id="8ad31-103">Gets the containing assembly for this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ad31-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ad31-104">Syntax</span></span>  
  
```  
HRESULT GetAssembly(  
    [out] ICorDebugAssembly **ppAssembly  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8ad31-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ad31-105">Parameters</span></span>  
 `ppAssembly`  
 <span data-ttu-id="8ad31-106">[out] Pointeur vers un objet ICorDebugAssembly qui représente l’assembly qui contient ce module.</span><span class="sxs-lookup"><span data-stu-id="8ad31-106">[out] A pointer to an ICorDebugAssembly object that represents the assembly containing this module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ad31-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8ad31-107">Requirements</span></span>  
 <span data-ttu-id="8ad31-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8ad31-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ad31-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8ad31-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8ad31-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8ad31-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8ad31-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ad31-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
