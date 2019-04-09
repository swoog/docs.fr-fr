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
ms.openlocfilehash: dd09ce27c0fea9dca8fd86afc563651d68542e13
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59173145"
---
# <a name="icordebuginitialize-method"></a><span data-ttu-id="daa3f-102">ICorDebug::Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="daa3f-102">ICorDebug::Initialize Method</span></span>
<span data-ttu-id="daa3f-103">Initialise le `ICorDebug` objet.</span><span class="sxs-lookup"><span data-stu-id="daa3f-103">Initializes the `ICorDebug` object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="daa3f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="daa3f-104">Syntax</span></span>  
  
```  
HRESULT Initialize ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="daa3f-105">Notes</span><span class="sxs-lookup"><span data-stu-id="daa3f-105">Remarks</span></span>  
 <span data-ttu-id="daa3f-106">Le débogueur doit appeler `Initialize` lors de la création de temps pour s’initialiser le débogage de services.</span><span class="sxs-lookup"><span data-stu-id="daa3f-106">The debugger must call `Initialize` at creation time to initialize the debugging services.</span></span> <span data-ttu-id="daa3f-107">Cette méthode doit être appelée avant toute autre méthode sur `ICorDebug` est appelée.</span><span class="sxs-lookup"><span data-stu-id="daa3f-107">This method must be called before any other method on `ICorDebug` is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="daa3f-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="daa3f-108">Requirements</span></span>  
 <span data-ttu-id="daa3f-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="daa3f-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="daa3f-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="daa3f-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="daa3f-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="daa3f-111">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="daa3f-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="daa3f-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="daa3f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daa3f-113">See also</span></span>

- [<span data-ttu-id="daa3f-114">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="daa3f-114">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
