---
title: Méthode ICorDebugVariableSymbol::GetSize
ms.date: 03/30/2017
ms.assetid: add0cd9d-9a29-49b1-ae07-d9d3786b4ccd
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 027b3f773ff0ed0ca7bf9d193f97a3b060ea8494
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59211840"
---
# <a name="icordebugvariablesymbolgetsize-method"></a><span data-ttu-id="b9d60-102">Méthode ICorDebugVariableSymbol::GetSize</span><span class="sxs-lookup"><span data-stu-id="b9d60-102">ICorDebugVariableSymbol::GetSize Method</span></span>
<span data-ttu-id="b9d60-103">Obtient la taille d'une variable en octets.</span><span class="sxs-lookup"><span data-stu-id="b9d60-103">Gets the size of a variable in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9d60-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9d60-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b9d60-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9d60-105">Parameters</span></span>  
 `pcbValue`  
 <span data-ttu-id="b9d60-106">Pointeur vers un entier non signé 32 bits contenant la taille de la variable.</span><span class="sxs-lookup"><span data-stu-id="b9d60-106">A pointer to a 32-bit unsigned integer containing the size of the variable.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b9d60-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b9d60-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b9d60-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="b9d60-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b9d60-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9d60-109">Requirements</span></span>  
 <span data-ttu-id="b9d60-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b9d60-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9d60-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b9d60-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b9d60-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b9d60-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="b9d60-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b9d60-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b9d60-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9d60-114">See also</span></span>

- [<span data-ttu-id="b9d60-115">ICorDebugVariableSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="b9d60-115">ICorDebugVariableSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="b9d60-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="b9d60-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
