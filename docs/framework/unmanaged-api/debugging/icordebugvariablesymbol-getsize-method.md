---
title: Méthode ICorDebugVariableSymbol::GetSize
ms.date: 03/30/2017
ms.assetid: add0cd9d-9a29-49b1-ae07-d9d3786b4ccd
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 01349b6418008db51c432d5c49f8491a44ab60d2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33419404"
---
# <a name="icordebugvariablesymbolgetsize-method"></a><span data-ttu-id="e7a45-102">Méthode ICorDebugVariableSymbol::GetSize</span><span class="sxs-lookup"><span data-stu-id="e7a45-102">ICorDebugVariableSymbol::GetSize Method</span></span>
<span data-ttu-id="e7a45-103">Obtient la taille d'une variable en octets.</span><span class="sxs-lookup"><span data-stu-id="e7a45-103">Gets the size of a variable in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e7a45-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7a45-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e7a45-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7a45-105">Parameters</span></span>  
 `pcbValue`  
 <span data-ttu-id="e7a45-106">Pointeur vers un entier non signé 32 bits contenant la taille de la variable.</span><span class="sxs-lookup"><span data-stu-id="e7a45-106">A pointer to a 32-bit unsigned integer containing the size of the variable.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e7a45-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e7a45-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e7a45-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="e7a45-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e7a45-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e7a45-109">Requirements</span></span>  
 <span data-ttu-id="e7a45-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e7a45-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7a45-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e7a45-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e7a45-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e7a45-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e7a45-113">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7a45-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7a45-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7a45-114">See Also</span></span>  
 [<span data-ttu-id="e7a45-115">ICorDebugVariableSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="e7a45-115">ICorDebugVariableSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)  
 [<span data-ttu-id="e7a45-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="e7a45-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
