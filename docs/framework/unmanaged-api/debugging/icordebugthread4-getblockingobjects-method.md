---
title: ICorDebugThread4::GetBlockingObjects, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread4.GetBlockingObjects Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread4::GetBlockingObjects
helpviewer_keywords:
- GetBlockingObjects method [.NET Framework debugging]
- ICorDebugThread4::GetBlockingObjects method [.NET Framework debugging]
ms.assetid: a7e6c54e-7be9-4e52-bbb4-95f52458e8e4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 93cae803b42d80dc0f868e2189de442eedea43f0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59186366"
---
# <a name="icordebugthread4getblockingobjects-method"></a><span data-ttu-id="d858a-102">ICorDebugThread4::GetBlockingObjects, méthode</span><span class="sxs-lookup"><span data-stu-id="d858a-102">ICorDebugThread4::GetBlockingObjects Method</span></span>
<span data-ttu-id="d858a-103">Fournit une énumération ordonnée de [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures qui fournissent des informations de blocage de thread.</span><span class="sxs-lookup"><span data-stu-id="d858a-103">Provides an ordered enumeration of [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures that provide thread blocking information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d858a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d858a-104">Syntax</span></span>  
  
```  
HRESULT GetBlockingObjects (  
    [out] ICorDebugBlockingObjectEnum **ppBlockingObjectEnum  
```  
  
## <a name="parameters"></a><span data-ttu-id="d858a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d858a-105">Parameters</span></span>  
 `ppBlockingObjectEnum`  
 <span data-ttu-id="d858a-106">[out] Un pointeur vers une énumération ordonnée de [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures.</span><span class="sxs-lookup"><span data-stu-id="d858a-106">[out] A pointer to an ordered enumeration of [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d858a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d858a-107">Remarks</span></span>  
 <span data-ttu-id="d858a-108">Le premier élément dans l’énumération retournée correspond à la première structure qui bloque le thread.</span><span class="sxs-lookup"><span data-stu-id="d858a-108">The first element in the returned enumeration corresponds to the first structure that is blocking the thread.</span></span> <span data-ttu-id="d858a-109">Le deuxième élément correspond à un élément de blocage rencontré lors de l’exécution d’un appel de procédure asynchrone (APC) lorsque bloquée sur le premier et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="d858a-109">The second element corresponds to a blocking item that is encountered while running an asynchronous procedure call (APC) when blocked on the first, and so on.</span></span>  
  
 <span data-ttu-id="d858a-110">L’énumération est valide uniquement pour la durée de l’état synchronisé actuel.</span><span class="sxs-lookup"><span data-stu-id="d858a-110">The enumeration is valid only for the duration of the current synchronized state.</span></span>  
  
 <span data-ttu-id="d858a-111">Cette méthode doit être appelée pendant que le programme débogué est dans un état synchronisé.</span><span class="sxs-lookup"><span data-stu-id="d858a-111">This method must be called while the debuggee is in a synchronized state.</span></span>  
  
 <span data-ttu-id="d858a-112">Si `ppBlockingObjectEnum` n’est pas un pointeur valide, le résultat est indéfini.</span><span class="sxs-lookup"><span data-stu-id="d858a-112">If `ppBlockingObjectEnum` is not a valid pointer, the result is undefined.</span></span>  
  
 <span data-ttu-id="d858a-113">Si un thread est bloqué et l’erreur ne peut pas être déterminée, la méthode retourne un HRESULT qui indique un échec ; Sinon, elle retourne S_OK.</span><span class="sxs-lookup"><span data-stu-id="d858a-113">If a thread is blocked and the error cannot be determined, the method returns an HRESULT that indicates failure; otherwise, it returns S_OK.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d858a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d858a-114">Requirements</span></span>  
 <span data-ttu-id="d858a-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d858a-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d858a-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d858a-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d858a-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d858a-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d858a-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d858a-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d858a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d858a-119">See also</span></span>

- [<span data-ttu-id="d858a-120">ICorDebugThread4, interface</span><span class="sxs-lookup"><span data-stu-id="d858a-120">ICorDebugThread4 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread4-interface.md)
- [<span data-ttu-id="d858a-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d858a-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="d858a-122">Débogage</span><span class="sxs-lookup"><span data-stu-id="d858a-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
