---
title: ICorDebugLoadedModule::GetBaseAddress (méthode)
ms.date: 03/30/2017
ms.assetid: 7c036772-d58a-47f1-a5fa-31779898ef0d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e84d6deca0cd09cc547636007208c70ab91c1ab1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946281"
---
# <a name="icordebugloadedmodulegetbaseaddress-method"></a><span data-ttu-id="5cd1f-102">ICorDebugLoadedModule::GetBaseAddress (méthode)</span><span class="sxs-lookup"><span data-stu-id="5cd1f-102">ICorDebugLoadedModule::GetBaseAddress Method</span></span>
<span data-ttu-id="5cd1f-103">Obtient l'adresse de base du module chargé.</span><span class="sxs-lookup"><span data-stu-id="5cd1f-103">Gets the base address of the loaded module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5cd1f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5cd1f-104">Syntax</span></span>  
  
```  
HRESULT GetBaseAddress(  
   [out] CORDB_ADDRESS *pAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5cd1f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5cd1f-105">Parameters</span></span>  
 `pAddress`  
 <span data-ttu-id="5cd1f-106">[out] Pointeur vers l'adresse de base du module chargé.</span><span class="sxs-lookup"><span data-stu-id="5cd1f-106">[out] A pointer to the base address of the loaded module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5cd1f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5cd1f-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5cd1f-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="5cd1f-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5cd1f-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cd1f-109">Requirements</span></span>  
 <span data-ttu-id="5cd1f-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5cd1f-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5cd1f-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5cd1f-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5cd1f-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5cd1f-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5cd1f-113">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5cd1f-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5cd1f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cd1f-114">See also</span></span>

- [<span data-ttu-id="5cd1f-115">ICorDebugLoadedModule, interface</span><span class="sxs-lookup"><span data-stu-id="5cd1f-115">ICorDebugLoadedModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-interface.md)
- [<span data-ttu-id="5cd1f-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="5cd1f-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
