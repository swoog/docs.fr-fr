---
title: ICorDebugSymbolProvider2, interface
ms.date: 03/30/2017
ms.assetid: 1c9c3d92-f0de-4d4d-87f1-0c702a4808af
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5b787302902779695c48df6e02e2ee00b28f44cb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59142465"
---
# <a name="icordebugsymbolprovider2-interface"></a><span data-ttu-id="1a56f-102">ICorDebugSymbolProvider2, interface</span><span class="sxs-lookup"><span data-stu-id="1a56f-102">ICorDebugSymbolProvider2 Interface</span></span>
<span data-ttu-id="1a56f-103">Étend logiquement le [ICorDebugSymbolProvider](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md) interface pour récupérer des informations symboliques de débogage supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="1a56f-103">Logically extends the [ICorDebugSymbolProvider](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md) interface to retrieve additional debug symbol information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1a56f-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1a56f-104">Methods</span></span>  
  
|<span data-ttu-id="1a56f-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="1a56f-105">Method</span></span>|<span data-ttu-id="1a56f-106">Description</span><span class="sxs-lookup"><span data-stu-id="1a56f-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1a56f-107">GetFrameProps, méthode</span><span class="sxs-lookup"><span data-stu-id="1a56f-107">GetFrameProps Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider2-getframeprops-method.md)|<span data-ttu-id="1a56f-108">Retourne l'adresse virtuelle relative de départ d'une méthode et le frame parent en fonction d'une adresse virtuelle relative de code.</span><span class="sxs-lookup"><span data-stu-id="1a56f-108">Returns the method starting relative virtual address of a method and the parent frame given a code relative virtual address.</span></span>|  
|[<span data-ttu-id="1a56f-109">GetGenericDictionaryInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="1a56f-109">GetGenericDictionaryInfo Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider2-getgenericdictionaryinfo-method.md)|<span data-ttu-id="1a56f-110">Récupère un mappage de dictionnaire générique.</span><span class="sxs-lookup"><span data-stu-id="1a56f-110">Retrieves a generic dictionary map.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1a56f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1a56f-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1a56f-112">Cette interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="1a56f-112">This interface is available with .NET Native only.</span></span> <span data-ttu-id="1a56f-113">Si vous implémentez cette interface pour des scénarios ICorDebug en dehors de .NET Native, le Common Language Runtime ignore cette interface.</span><span class="sxs-lookup"><span data-stu-id="1a56f-113">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1a56f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a56f-114">Requirements</span></span>  
 <span data-ttu-id="1a56f-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1a56f-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1a56f-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1a56f-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1a56f-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1a56f-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1a56f-118">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1a56f-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a56f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a56f-119">See also</span></span>

- [<span data-ttu-id="1a56f-120">ICorDebugSymbolProvider, interface</span><span class="sxs-lookup"><span data-stu-id="1a56f-120">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="1a56f-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="1a56f-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="1a56f-122">Débogage</span><span class="sxs-lookup"><span data-stu-id="1a56f-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
