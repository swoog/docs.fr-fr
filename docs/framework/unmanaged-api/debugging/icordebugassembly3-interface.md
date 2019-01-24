---
title: ICorDebugAssembly3, interface
ms.date: 03/30/2017
ms.assetid: 17fc5d76-75a9-4933-83f0-594de7f973f3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 66d3024c0bb2c0014cbec2b24deb7b0d5845fe88
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54627523"
---
# <a name="icordebugassembly3-interface"></a><span data-ttu-id="76e13-102">ICorDebugAssembly3, interface</span><span class="sxs-lookup"><span data-stu-id="76e13-102">ICorDebugAssembly3 Interface</span></span>
<span data-ttu-id="76e13-103">Étend logiquement l’interface ICorDebugAssembly pour prendre en charge pour les assemblys conteneurs et leurs assemblys de relation contenant-contenus.</span><span class="sxs-lookup"><span data-stu-id="76e13-103">Logically extends the ICorDebugAssembly interface to provide support for container assemblies and their contained assemblies.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="76e13-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="76e13-104">Methods</span></span>  
  
|<span data-ttu-id="76e13-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="76e13-105">Method</span></span>|<span data-ttu-id="76e13-106">Description</span><span class="sxs-lookup"><span data-stu-id="76e13-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="76e13-107">EnumerateContainedAssemblies, méthode</span><span class="sxs-lookup"><span data-stu-id="76e13-107">EnumerateContainedAssemblies Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly3-enumeratecontainedassemblies-method.md)|<span data-ttu-id="76e13-108">Obtient un énumérateur pour les assemblys contenus dans cet assembly.</span><span class="sxs-lookup"><span data-stu-id="76e13-108">Gets an enumerator for the assemblies contained in this assembly.</span></span>|  
|[<span data-ttu-id="76e13-109">GetContainerAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="76e13-109">GetContainerAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly3-getcontainerassembly-method.md)|<span data-ttu-id="76e13-110">Retourne l'assembly conteneur de cet objet `ICorDebugAssembly3`.</span><span class="sxs-lookup"><span data-stu-id="76e13-110">Returns the container assembly of this `ICorDebugAssembly3` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="76e13-111">Notes</span><span class="sxs-lookup"><span data-stu-id="76e13-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="76e13-112">L'interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="76e13-112">The interface is available with .NET Native only.</span></span> <span data-ttu-id="76e13-113">Une tentative d'appel à `QueryInterface` pour récupérer un pointeur d'interface retourne `E_NOINTERFACE` pour les scénarios ICorDebug en dehors de .NET Native.</span><span class="sxs-lookup"><span data-stu-id="76e13-113">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="76e13-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="76e13-114">Requirements</span></span>  
 <span data-ttu-id="76e13-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="76e13-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="76e13-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="76e13-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="76e13-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="76e13-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="76e13-118">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="76e13-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76e13-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76e13-119">See also</span></span>
- [<span data-ttu-id="76e13-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="76e13-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="76e13-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="76e13-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
