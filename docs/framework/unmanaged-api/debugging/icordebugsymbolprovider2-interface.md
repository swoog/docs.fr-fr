---
title: ICorDebugSymbolProvider2, interface
ms.date: 03/30/2017
ms.assetid: 1c9c3d92-f0de-4d4d-87f1-0c702a4808af
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5b787302902779695c48df6e02e2ee00b28f44cb
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59142465"
---
# <a name="icordebugsymbolprovider2-interface"></a><span data-ttu-id="046fd-102">ICorDebugSymbolProvider2, interface</span><span class="sxs-lookup"><span data-stu-id="046fd-102">ICorDebugSymbolProvider2 Interface</span></span>
<span data-ttu-id="046fd-103">Étend logiquement le [ICorDebugSymbolProvider](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md) interface pour récupérer des informations symboliques de débogage supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="046fd-103">Logically extends the [ICorDebugSymbolProvider](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md) interface to retrieve additional debug symbol information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="046fd-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="046fd-104">Methods</span></span>  
  
|<span data-ttu-id="046fd-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="046fd-105">Method</span></span>|<span data-ttu-id="046fd-106">Description</span><span class="sxs-lookup"><span data-stu-id="046fd-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="046fd-107">GetFrameProps, méthode</span><span class="sxs-lookup"><span data-stu-id="046fd-107">GetFrameProps Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider2-getframeprops-method.md)|<span data-ttu-id="046fd-108">Retourne l'adresse virtuelle relative de départ d'une méthode et le frame parent en fonction d'une adresse virtuelle relative de code.</span><span class="sxs-lookup"><span data-stu-id="046fd-108">Returns the method starting relative virtual address of a method and the parent frame given a code relative virtual address.</span></span>|  
|[<span data-ttu-id="046fd-109">GetGenericDictionaryInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="046fd-109">GetGenericDictionaryInfo Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider2-getgenericdictionaryinfo-method.md)|<span data-ttu-id="046fd-110">Récupère un mappage de dictionnaire générique.</span><span class="sxs-lookup"><span data-stu-id="046fd-110">Retrieves a generic dictionary map.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="046fd-111">Notes</span><span class="sxs-lookup"><span data-stu-id="046fd-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="046fd-112">Cette interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="046fd-112">This interface is available with .NET Native only.</span></span> <span data-ttu-id="046fd-113">Si vous implémentez cette interface pour des scénarios ICorDebug en dehors de .NET Native, le Common Language Runtime ignore cette interface.</span><span class="sxs-lookup"><span data-stu-id="046fd-113">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="046fd-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="046fd-114">Requirements</span></span>  
 <span data-ttu-id="046fd-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="046fd-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="046fd-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="046fd-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="046fd-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="046fd-117">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="046fd-118">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="046fd-118">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="046fd-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="046fd-119">See also</span></span>

- [<span data-ttu-id="046fd-120">ICorDebugSymbolProvider, interface</span><span class="sxs-lookup"><span data-stu-id="046fd-120">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="046fd-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="046fd-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="046fd-122">Débogage</span><span class="sxs-lookup"><span data-stu-id="046fd-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
