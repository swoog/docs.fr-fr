---
title: Méthode ICorDebugVariableSymbol::GetSize
ms.date: 03/30/2017
ms.assetid: add0cd9d-9a29-49b1-ae07-d9d3786b4ccd
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 800c19574b24a4ab6135b53567515b23eae4dc8a
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57494894"
---
# <a name="icordebugvariablesymbolgetsize-method"></a><span data-ttu-id="657d7-102">Méthode ICorDebugVariableSymbol::GetSize</span><span class="sxs-lookup"><span data-stu-id="657d7-102">ICorDebugVariableSymbol::GetSize Method</span></span>
<span data-ttu-id="657d7-103">Obtient la taille d'une variable en octets.</span><span class="sxs-lookup"><span data-stu-id="657d7-103">Gets the size of a variable in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="657d7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="657d7-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="657d7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="657d7-105">Parameters</span></span>  
 `pcbValue`  
 <span data-ttu-id="657d7-106">Pointeur vers un entier non signé 32 bits contenant la taille de la variable.</span><span class="sxs-lookup"><span data-stu-id="657d7-106">A pointer to a 32-bit unsigned integer containing the size of the variable.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="657d7-107">Notes</span><span class="sxs-lookup"><span data-stu-id="657d7-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="657d7-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="657d7-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="657d7-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="657d7-109">Requirements</span></span>  
 <span data-ttu-id="657d7-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="657d7-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="657d7-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="657d7-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="657d7-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="657d7-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="657d7-113">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="657d7-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="657d7-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="657d7-114">See also</span></span>
- [<span data-ttu-id="657d7-115">ICorDebugVariableSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="657d7-115">ICorDebugVariableSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="657d7-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="657d7-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
