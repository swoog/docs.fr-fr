---
title: ICorDebugDebugEvent::GetEventKind, méthode
ms.date: 03/30/2017
ms.assetid: c37aaceb-c948-46bd-a943-08be4cbb76f4
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 62eede48eea01563dbc3e170720694a24343d0a5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59150525"
---
# <a name="icordebugdebugeventgeteventkind-method"></a><span data-ttu-id="cda2c-102">ICorDebugDebugEvent::GetEventKind, méthode</span><span class="sxs-lookup"><span data-stu-id="cda2c-102">ICorDebugDebugEvent::GetEventKind Method</span></span>
<span data-ttu-id="cda2c-103">Indique le type d'événement représenté par cet objet `ICorDebugDebugEvent`.</span><span class="sxs-lookup"><span data-stu-id="cda2c-103">Indicates what kind of event this `ICorDebugDebugEvent` object represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cda2c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cda2c-104">Syntax</span></span>  
  
```  
HRESULT GetEventKind(  
    [out]CorDebugDebugEventKind *pDebugEventKind  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cda2c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cda2c-105">Parameters</span></span>  
 <span data-ttu-id="cda2c-106">pDebugEventKind</span><span class="sxs-lookup"><span data-stu-id="cda2c-106">pDebugEventKind</span></span>  
 <span data-ttu-id="cda2c-107">Un pointeur vers un [CorDebugDebugEventKind](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md) membre d’énumération qui indique le type d’événement.</span><span class="sxs-lookup"><span data-stu-id="cda2c-107">A pointer to a [CorDebugDebugEventKind](../../../../docs/framework/unmanaged-api/debugging/cordebugdebugeventkind-enumeration.md) enumeration member that indicates the type of event.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cda2c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="cda2c-108">Remarks</span></span>  
 <span data-ttu-id="cda2c-109">En fonction de la valeur de `pDebugEventKind`, vous pouvez appeler `QueryInterface` pour obtenir une interface d'événement de débogage plus précise qui fournit des données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="cda2c-109">Based on the value of `pDebugEventKind`, you can call `QueryInterface` to get a more precise debug event interface that has additional data.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cda2c-110">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="cda2c-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cda2c-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cda2c-111">Requirements</span></span>  
 <span data-ttu-id="cda2c-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cda2c-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cda2c-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cda2c-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cda2c-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cda2c-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cda2c-115">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cda2c-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cda2c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cda2c-116">See also</span></span>

- [<span data-ttu-id="cda2c-117">ICorDebugDebugEvent, interface</span><span class="sxs-lookup"><span data-stu-id="cda2c-117">ICorDebugDebugEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md)
- [<span data-ttu-id="cda2c-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="cda2c-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
