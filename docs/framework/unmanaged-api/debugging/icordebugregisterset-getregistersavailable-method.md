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
ms.openlocfilehash: 3174be7237bcdbd5a12f38f04d6e67d9eb9a573e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33421851"
---
# <a name="icordebugregistersetgetregistersavailable-method"></a><span data-ttu-id="13bb4-102">ICorDebugRegisterSet::GetRegistersAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="13bb4-102">ICorDebugRegisterSet::GetRegistersAvailable Method</span></span>
<span data-ttu-id="13bb4-103">Obtient un masque de bits indiquant les registres dans ce [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) sont actuellement disponibles.</span><span class="sxs-lookup"><span data-stu-id="13bb4-103">Gets a bit mask indicating which registers in this [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) are currently available.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13bb4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13bb4-104">Syntax</span></span>  
  
```  
HRESULT GetRegistersAvailable (  
    [out] ULONG64   *pAvailable  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="13bb4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13bb4-105">Parameters</span></span>  
 `pAvailable`  
 <span data-ttu-id="13bb4-106">[out] Un masque de bits qui indique les registres qui sont actuellement disponibles.</span><span class="sxs-lookup"><span data-stu-id="13bb4-106">[out] A bit mask that indicates which registers are currently available.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="13bb4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="13bb4-107">Remarks</span></span>  
 <span data-ttu-id="13bb4-108">Un Registre peut être indisponible si sa valeur ne peut pas être déterminée pour la situation donnée.</span><span class="sxs-lookup"><span data-stu-id="13bb4-108">A register may be unavailable if its value cannot be determined for the given situation.</span></span>  
  
 <span data-ttu-id="13bb4-109">Le masque retourné contient un bit pour chaque registre (1 << l’index du Registre).</span><span class="sxs-lookup"><span data-stu-id="13bb4-109">The returned mask contains a bit for each register (1 << the register index).</span></span> <span data-ttu-id="13bb4-110">La valeur du bit est 1 si le Registre est disponible, ou 0 s’il n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="13bb4-110">The bit value is 1 if the register is available, or 0 if it is not available.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="13bb4-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="13bb4-111">Requirements</span></span>  
 <span data-ttu-id="13bb4-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="13bb4-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="13bb4-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="13bb4-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="13bb4-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="13bb4-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="13bb4-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="13bb4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13bb4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13bb4-116">See Also</span></span>  
 [<span data-ttu-id="13bb4-117">ICorDebugRegisterSet, interface</span><span class="sxs-lookup"><span data-stu-id="13bb4-117">ICorDebugRegisterSet Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)  
 [<span data-ttu-id="13bb4-118">ICorDebugRegisterSet2, interface</span><span class="sxs-lookup"><span data-stu-id="13bb4-118">ICorDebugRegisterSet2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
