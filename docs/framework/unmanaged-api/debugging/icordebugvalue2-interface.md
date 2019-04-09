---
title: ICorDebugValue2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugValue2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue2
helpviewer_keywords:
- ICorDebugValue2 interface [.NET Framework debugging]
ms.assetid: 3ff2ad2a-da5a-461b-8627-1a8eba49df9c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6718bbfdb1825b9f01698d76deec3fab16cb2ac6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59091601"
---
# <a name="icordebugvalue2-interface"></a><span data-ttu-id="fce31-102">ICorDebugValue2, interface</span><span class="sxs-lookup"><span data-stu-id="fce31-102">ICorDebugValue2 Interface</span></span>
<span data-ttu-id="fce31-103">Étend l’interface « ICorDebugValue » pour prendre en charge des objets « ICorDebugType ».</span><span class="sxs-lookup"><span data-stu-id="fce31-103">Extends the "ICorDebugValue" interface to provide support for "ICorDebugType" objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fce31-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fce31-104">Methods</span></span>  
  
|<span data-ttu-id="fce31-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="fce31-105">Method</span></span>|<span data-ttu-id="fce31-106">Description</span><span class="sxs-lookup"><span data-stu-id="fce31-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fce31-107">GetExactType, méthode</span><span class="sxs-lookup"><span data-stu-id="fce31-107">GetExactType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue2-getexacttype-method.md)|<span data-ttu-id="fce31-108">Obtient un pointeur d’interface vers un `ICorDebugType` objet qui représente le <xref:System.Type> de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="fce31-108">Gets an interface pointer to an `ICorDebugType` object that represents the <xref:System.Type> of this value.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fce31-109">Notes</span><span class="sxs-lookup"><span data-stu-id="fce31-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fce31-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="fce31-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fce31-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fce31-111">Requirements</span></span>  
 <span data-ttu-id="fce31-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fce31-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fce31-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fce31-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fce31-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fce31-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="fce31-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="fce31-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="fce31-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fce31-116">See also</span></span>

- [<span data-ttu-id="fce31-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="fce31-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)

- [<span data-ttu-id="fce31-118">ICorDebugValue3, interface</span><span class="sxs-lookup"><span data-stu-id="fce31-118">ICorDebugValue3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md)
