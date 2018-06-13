---
title: ICorDebug::Initialize, méthode
ms.date: 03/30/2017
api_name:
- ICorDebug.Initialize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::Initialize
helpviewer_keywords:
- Initialize method, ICorDebug interface [.NET Framework debugging]
- ICorDebug::Initialize method [.NET Framework debugging]
ms.assetid: 6fae3b23-5c9f-47c0-85d8-6bb75e050786
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fa79382d597d303d492e3a441c15a422697be279
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405965"
---
# <a name="icordebuginitialize-method"></a><span data-ttu-id="0c0bd-102">ICorDebug::Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="0c0bd-102">ICorDebug::Initialize Method</span></span>
<span data-ttu-id="0c0bd-103">Initialise le `ICorDebug` objet.</span><span class="sxs-lookup"><span data-stu-id="0c0bd-103">Initializes the `ICorDebug` object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c0bd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c0bd-104">Syntax</span></span>  
  
```  
HRESULT Initialize ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="0c0bd-105">Notes</span><span class="sxs-lookup"><span data-stu-id="0c0bd-105">Remarks</span></span>  
 <span data-ttu-id="0c0bd-106">Le débogueur doit appeler `Initialize` lors de la création de services moment pour initialiser le débogage.</span><span class="sxs-lookup"><span data-stu-id="0c0bd-106">The debugger must call `Initialize` at creation time to initialize the debugging services.</span></span> <span data-ttu-id="0c0bd-107">Cette méthode doit être appelée avant toute autre méthode sur `ICorDebug` est appelée.</span><span class="sxs-lookup"><span data-stu-id="0c0bd-107">This method must be called before any other method on `ICorDebug` is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c0bd-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0c0bd-108">Requirements</span></span>  
 <span data-ttu-id="0c0bd-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0c0bd-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c0bd-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0c0bd-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0c0bd-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0c0bd-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0c0bd-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c0bd-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c0bd-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c0bd-113">See Also</span></span>  
 [<span data-ttu-id="0c0bd-114">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="0c0bd-114">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
