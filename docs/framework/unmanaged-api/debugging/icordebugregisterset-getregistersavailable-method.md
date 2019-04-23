---
title: ICorDebugRegisterSet::GetRegistersAvailable, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.GetRegistersAvailable
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::GetRegistersAvailable
helpviewer_keywords:
- ICorDebugRegisterSet::GetRegistersAvailable method [.NET Framework debugging]
- GetRegistersAvailable method, ICorDebugRegisterSet interface [.NET Framework debugging]
ms.assetid: 4ba08ffa-55a2-4662-9d6d-4738f1db60c9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f341098268f735a576bdbc5f0cea52f1a7e14f90
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59156037"
---
# <a name="icordebugregistersetgetregistersavailable-method"></a><span data-ttu-id="c138a-102">ICorDebugRegisterSet::GetRegistersAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="c138a-102">ICorDebugRegisterSet::GetRegistersAvailable Method</span></span>
<span data-ttu-id="c138a-103">Obtient un masque de bits indiquant les registres dans ce [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) sont actuellement disponibles.</span><span class="sxs-lookup"><span data-stu-id="c138a-103">Gets a bit mask indicating which registers in this [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) are currently available.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c138a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c138a-104">Syntax</span></span>  
  
```  
HRESULT GetRegistersAvailable (  
    [out] ULONG64   *pAvailable  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c138a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c138a-105">Parameters</span></span>  
 `pAvailable`  
 <span data-ttu-id="c138a-106">[out] Un masque de bits qui indique quels registres sont actuellement disponibles.</span><span class="sxs-lookup"><span data-stu-id="c138a-106">[out] A bit mask that indicates which registers are currently available.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c138a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c138a-107">Remarks</span></span>  
 <span data-ttu-id="c138a-108">Un Registre est peut-être indisponible si sa valeur ne peut pas être déterminée pour la situation donnée.</span><span class="sxs-lookup"><span data-stu-id="c138a-108">A register may be unavailable if its value cannot be determined for the given situation.</span></span>  
  
 <span data-ttu-id="c138a-109">Le masque retourné contient un bit pour chaque registre (1 << l’index du Registre).</span><span class="sxs-lookup"><span data-stu-id="c138a-109">The returned mask contains a bit for each register (1 << the register index).</span></span> <span data-ttu-id="c138a-110">La valeur de bit est 1 si le Registre est disponible, ou 0 s’il n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c138a-110">The bit value is 1 if the register is available, or 0 if it is not available.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c138a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c138a-111">Requirements</span></span>  
 <span data-ttu-id="c138a-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c138a-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c138a-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c138a-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c138a-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c138a-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c138a-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c138a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c138a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c138a-116">See also</span></span>

- [<span data-ttu-id="c138a-117">ICorDebugRegisterSet, interface</span><span class="sxs-lookup"><span data-stu-id="c138a-117">ICorDebugRegisterSet Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)
- [<span data-ttu-id="c138a-118">ICorDebugRegisterSet2, interface</span><span class="sxs-lookup"><span data-stu-id="c138a-118">ICorDebugRegisterSet2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
