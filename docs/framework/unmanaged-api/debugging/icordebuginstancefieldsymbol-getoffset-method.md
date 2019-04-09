---
title: ICorDebugInstanceFieldSymbol::GetOffset, méthode
ms.date: 03/30/2017
ms.assetid: 7e470150-2b92-4425-989c-315f48964fd2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e8ea777755aebb59f3e865df26c38c74ef68ae31
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59203871"
---
# <a name="icordebuginstancefieldsymbolgetoffset-method"></a><span data-ttu-id="fb586-102">ICorDebugInstanceFieldSymbol::GetOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="fb586-102">ICorDebugInstanceFieldSymbol::GetOffset Method</span></span>
<span data-ttu-id="fb586-103">Obtient l'offset en octets de ce champ d'instance dans sa classe parente.</span><span class="sxs-lookup"><span data-stu-id="fb586-103">Gets the offset in bytes of this instance field in its parent class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fb586-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb586-104">Syntax</span></span>  
  
```  
HRESULT GetOffset(  
   [out] ULONG32 *pcbOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fb586-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb586-105">Parameters</span></span>  
 `pcbOffset`  
 <span data-ttu-id="fb586-106">Pointeur vers le nombre d'octets correspondant à l'offset de ce champ d'instance dans sa classe parente.</span><span class="sxs-lookup"><span data-stu-id="fb586-106">A pointer to the number of bytes that this instance field is offset in its parent class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fb586-107">Notes</span><span class="sxs-lookup"><span data-stu-id="fb586-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fb586-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="fb586-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fb586-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb586-109">Requirements</span></span>  
 <span data-ttu-id="fb586-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fb586-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fb586-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fb586-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fb586-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fb586-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="fb586-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="fb586-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="fb586-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb586-114">See also</span></span>

- [<span data-ttu-id="fb586-115">ICorDebugInstanceFieldSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="fb586-115">ICorDebugInstanceFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginstancefieldsymbol-interface.md)
- [<span data-ttu-id="fb586-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="fb586-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
