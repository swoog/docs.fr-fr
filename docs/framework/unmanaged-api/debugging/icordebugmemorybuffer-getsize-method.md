---
title: ICorDebugMemoryBuffer::GetSize, méthode
ms.date: 03/30/2017
ms.assetid: 9ffd5482-268e-4680-9fd1-bfb0b7d66450
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: caf95e0b5c8d4ae942bb428f53d4e58313e0e78e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33414750"
---
# <a name="icordebugmemorybuffergetsize-method"></a><span data-ttu-id="69960-102">ICorDebugMemoryBuffer::GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="69960-102">ICorDebugMemoryBuffer::GetSize Method</span></span>
<span data-ttu-id="69960-103">Obtient la taille de la mémoire tampon en octets.</span><span class="sxs-lookup"><span data-stu-id="69960-103">Gets the size of the memory buffer in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="69960-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69960-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbBufferLength  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="69960-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69960-105">Parameters</span></span>  
 `pcbBufferLength`  
 <span data-ttu-id="69960-106">[out] Pointeur vers la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="69960-106">[out] A pointer to the size of the memory buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="69960-107">Notes</span><span class="sxs-lookup"><span data-stu-id="69960-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="69960-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="69960-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="69960-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="69960-109">Requirements</span></span>  
 <span data-ttu-id="69960-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="69960-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="69960-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="69960-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="69960-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="69960-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="69960-113">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="69960-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="69960-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69960-114">See Also</span></span>  
 [<span data-ttu-id="69960-115">ICorDebugMemoryBuffer, interface</span><span class="sxs-lookup"><span data-stu-id="69960-115">ICorDebugMemoryBuffer Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md)  
 [<span data-ttu-id="69960-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="69960-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
