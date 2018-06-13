---
title: ICorDebugAssembly::EnumerateModules, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly.EnumerateModules
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly::EnumerateModules
helpviewer_keywords:
- ICorDebugAssembly::EnumerateModules method [.NET Framework debugging]
- EnumerateModules method [.NET Framework debugging]
ms.assetid: c7ba51a1-0dd5-4452-b471-232febe0f897
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ada2e0e81c9e022e152e01472839d5d506332fac
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402380"
---
# <a name="icordebugassemblyenumeratemodules-method"></a><span data-ttu-id="6c33d-102">ICorDebugAssembly::EnumerateModules, méthode</span><span class="sxs-lookup"><span data-stu-id="6c33d-102">ICorDebugAssembly::EnumerateModules Method</span></span>
<span data-ttu-id="6c33d-103">Obtient un énumérateur pour les modules contenus dans le `ICorDebugAssembly`.</span><span class="sxs-lookup"><span data-stu-id="6c33d-103">Gets an enumerator for the modules contained in the `ICorDebugAssembly`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c33d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c33d-104">Syntax</span></span>  
  
```  
HRESULT EnumerateModules (  
    [out] ICorDebugModuleEnum **ppModules  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6c33d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c33d-105">Parameters</span></span>  
 `ppModules`  
 <span data-ttu-id="6c33d-106">[out] Pointeur vers l’adresse de l’interface ICorDebugModuleEnum qui est l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="6c33d-106">[out] A pointer to the address of the ICorDebugModuleEnum interface that is the enumerator.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6c33d-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6c33d-107">Requirements</span></span>  
 <span data-ttu-id="6c33d-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6c33d-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c33d-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6c33d-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6c33d-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6c33d-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6c33d-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c33d-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
