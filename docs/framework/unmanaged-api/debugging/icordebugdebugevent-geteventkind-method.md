---
title: ICorDebugDebugEvent::GetEventKind, méthode
ms.date: 03/30/2017
ms.assetid: c37aaceb-c948-46bd-a943-08be4cbb76f4
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9bbc9581db839d9c0a48362eac2108f43665b0fa
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33414854"
---
# <a name="icordebugdebugeventgeteventkind-method"></a><span data-ttu-id="6bedb-102">ICorDebugDebugEvent::GetEventKind, méthode</span><span class="sxs-lookup"><span data-stu-id="6bedb-102">ICorDebugDebugEvent::GetEventKind Method</span></span>
<span data-ttu-id="6bedb-103">Indique le type d'événement représenté par cet objet `ICorDebugDebugEvent`.</span><span class="sxs-lookup"><span data-stu-id="6bedb-103">Indicates what kind of event this `ICorDebugDebugEvent` object represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6bedb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bedb-104">Syntax</span></span>  
  
```  
HRESULT GetEventKind(  
    [out]CorDebugDebugEventKind *pDebugEventKind  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6bedb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bedb-105">Parameters</span></span>  
 <span data-ttu-id="6bedb-106">pDebugEventKind</span><span class="sxs-lookup"><span data-stu-id="6bedb-106">pDebugEventKind</span></span>  
 <span data-ttu-id="6bedb-107">Un pointeur vers un [CorDebugDebugEventKind](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md) membre d’énumération qui indique le type d’événement.</span><span class="sxs-lookup"><span data-stu-id="6bedb-107">A pointer to a [CorDebugDebugEventKind](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md) enumeration member that indicates the type of event.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6bedb-108">Notes</span><span class="sxs-lookup"><span data-stu-id="6bedb-108">Remarks</span></span>  
 <span data-ttu-id="6bedb-109">En fonction de la valeur de `pDebugEventKind`, vous pouvez appeler `QueryInterface` pour obtenir une interface d'événement de débogage plus précise qui fournit des données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6bedb-109">Based on the value of `pDebugEventKind`, you can call `QueryInterface` to get a more precise debug event interface that has additional data.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6bedb-110">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="6bedb-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6bedb-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6bedb-111">Requirements</span></span>  
 <span data-ttu-id="6bedb-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6bedb-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6bedb-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6bedb-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6bedb-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6bedb-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6bedb-115">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6bedb-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6bedb-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bedb-116">See Also</span></span>  
 [<span data-ttu-id="6bedb-117">ICorDebugDebugEvent, interface</span><span class="sxs-lookup"><span data-stu-id="6bedb-117">ICorDebugDebugEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md)  
 [<span data-ttu-id="6bedb-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="6bedb-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
