---
title: ICorDebugMemoryBuffer::GetSize, méthode
ms.date: 03/30/2017
ms.assetid: 9ffd5482-268e-4680-9fd1-bfb0b7d66450
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d687f2bbd3c20564368d4246961b56382ea14cf5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59099675"
---
# <a name="icordebugmemorybuffergetsize-method"></a><span data-ttu-id="977eb-102">ICorDebugMemoryBuffer::GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="977eb-102">ICorDebugMemoryBuffer::GetSize Method</span></span>
<span data-ttu-id="977eb-103">Obtient la taille de la mémoire tampon en octets.</span><span class="sxs-lookup"><span data-stu-id="977eb-103">Gets the size of the memory buffer in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="977eb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="977eb-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbBufferLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="977eb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="977eb-105">Parameters</span></span>  
 `pcbBufferLength`  
 <span data-ttu-id="977eb-106">[out] Pointeur vers la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="977eb-106">[out] A pointer to the size of the memory buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="977eb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="977eb-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="977eb-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="977eb-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="977eb-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="977eb-109">Requirements</span></span>  
 <span data-ttu-id="977eb-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="977eb-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="977eb-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="977eb-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="977eb-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="977eb-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="977eb-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="977eb-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="977eb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="977eb-114">See also</span></span>

- [<span data-ttu-id="977eb-115">ICorDebugMemoryBuffer, interface</span><span class="sxs-lookup"><span data-stu-id="977eb-115">ICorDebugMemoryBuffer Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md)
- [<span data-ttu-id="977eb-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="977eb-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
