---
title: Méthode ICorDebugVariableSymbol::GetSize
ms.date: 03/30/2017
ms.assetid: add0cd9d-9a29-49b1-ae07-d9d3786b4ccd
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 027b3f773ff0ed0ca7bf9d193f97a3b060ea8494
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768834"
---
# <a name="icordebugvariablesymbolgetsize-method"></a><span data-ttu-id="05494-102">Méthode ICorDebugVariableSymbol::GetSize</span><span class="sxs-lookup"><span data-stu-id="05494-102">ICorDebugVariableSymbol::GetSize Method</span></span>
<span data-ttu-id="05494-103">Obtient la taille d'une variable en octets.</span><span class="sxs-lookup"><span data-stu-id="05494-103">Gets the size of a variable in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05494-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05494-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="05494-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05494-105">Parameters</span></span>  
 `pcbValue`  
 <span data-ttu-id="05494-106">Pointeur vers un entier non signé 32 bits contenant la taille de la variable.</span><span class="sxs-lookup"><span data-stu-id="05494-106">A pointer to a 32-bit unsigned integer containing the size of the variable.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="05494-107">Notes</span><span class="sxs-lookup"><span data-stu-id="05494-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="05494-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="05494-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="05494-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05494-109">Requirements</span></span>  
 <span data-ttu-id="05494-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="05494-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="05494-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="05494-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="05494-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="05494-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="05494-113">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="05494-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05494-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05494-114">See also</span></span>

- [<span data-ttu-id="05494-115">ICorDebugVariableSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="05494-115">ICorDebugVariableSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="05494-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="05494-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
