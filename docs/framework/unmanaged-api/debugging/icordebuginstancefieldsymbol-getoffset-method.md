---
title: ICorDebugInstanceFieldSymbol::GetOffset, méthode
ms.date: 03/30/2017
ms.assetid: 7e470150-2b92-4425-989c-315f48964fd2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c77ac2eac1022fa591066901f48eaf609b5367af
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33413561"
---
# <a name="icordebuginstancefieldsymbolgetoffset-method"></a><span data-ttu-id="a9e89-102">ICorDebugInstanceFieldSymbol::GetOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="a9e89-102">ICorDebugInstanceFieldSymbol::GetOffset Method</span></span>
<span data-ttu-id="a9e89-103">Obtient l'offset en octets de ce champ d'instance dans sa classe parente.</span><span class="sxs-lookup"><span data-stu-id="a9e89-103">Gets the offset in bytes of this instance field in its parent class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9e89-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9e89-104">Syntax</span></span>  
  
```  
HRESULT GetOffset(  
   [out] ULONG32 *pcbOffset  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a9e89-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9e89-105">Parameters</span></span>  
 `pcbOffset`  
 <span data-ttu-id="a9e89-106">Pointeur vers le nombre d'octets correspondant à l'offset de ce champ d'instance dans sa classe parente.</span><span class="sxs-lookup"><span data-stu-id="a9e89-106">A pointer to the number of bytes that this instance field is offset in its parent class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a9e89-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a9e89-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a9e89-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="a9e89-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9e89-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a9e89-109">Requirements</span></span>  
 <span data-ttu-id="a9e89-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a9e89-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9e89-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a9e89-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a9e89-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a9e89-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a9e89-113">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9e89-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9e89-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9e89-114">See Also</span></span>  
 [<span data-ttu-id="a9e89-115">ICorDebugInstanceFieldSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="a9e89-115">ICorDebugInstanceFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginstancefieldsymbol-interface.md)  
 [<span data-ttu-id="a9e89-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="a9e89-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
