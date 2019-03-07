---
title: ICorDebugRegisterSet::GetRegisters, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.GetRegisters
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::GetRegisters
helpviewer_keywords:
- GetRegisters method, ICorDebugRegisterSet interface [.NET Framework debugging]
- ICorDebugRegisterSet::GetRegisters method [.NET Framework debugging]
ms.assetid: fdf91864-48ea-4aa6-b70c-361b7a3184c7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c4887d44f0ac5603280efa0abdbd7e65c71fc3ca
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57485450"
---
# <a name="icordebugregistersetgetregisters-method"></a><span data-ttu-id="97131-102">ICorDebugRegisterSet::GetRegisters, méthode</span><span class="sxs-lookup"><span data-stu-id="97131-102">ICorDebugRegisterSet::GetRegisters Method</span></span>
<span data-ttu-id="97131-103">Obtient la valeur de chaque registre (sur l’ordinateur qui exécute actuellement le code) qui est spécifié par le masque de bits.</span><span class="sxs-lookup"><span data-stu-id="97131-103">Gets the value of each register (on the computer that is currently executing code) that is specified by the bit mask.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97131-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97131-104">Syntax</span></span>  
  
```  
HRESULT GetRegisters (  
    [in] ULONG64       mask,   
    [in] ULONG32       regCount,  
    [out, size_is(regCount), length_is(regCount)]  
        CORDB_REGISTER regBuffer[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="97131-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97131-105">Parameters</span></span>  
 `mask`  
 <span data-ttu-id="97131-106">[in] Un masque de bits qui spécifie les valeurs de registres à récupérer.</span><span class="sxs-lookup"><span data-stu-id="97131-106">[in] A bit mask that specifies which register values are to be retrieved.</span></span> <span data-ttu-id="97131-107">Chaque bit correspond à un Registre.</span><span class="sxs-lookup"><span data-stu-id="97131-107">Each bit corresponds to a register.</span></span> <span data-ttu-id="97131-108">Si un bit est défini sur 1, la valeur de Registre est récupérée ; Sinon, la valeur de Registre n’est pas récupérée.</span><span class="sxs-lookup"><span data-stu-id="97131-108">If a bit is set to one, the register's value is retrieved; otherwise, the register's value is not retrieved.</span></span>  
  
 `regCount`  
 <span data-ttu-id="97131-109">[in] Le nombre de valeurs de registres à récupérer.</span><span class="sxs-lookup"><span data-stu-id="97131-109">[in] The number of register values to be retrieved.</span></span>  
  
 `regBuffer`  
 <span data-ttu-id="97131-110">[out] Un tableau de `CORDB_REGISTER` objets, chacun d’eux reçoit une valeur d’un Registre.</span><span class="sxs-lookup"><span data-stu-id="97131-110">[out] An array of `CORDB_REGISTER` objects, each of which receives a value of a register.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="97131-111">Notes</span><span class="sxs-lookup"><span data-stu-id="97131-111">Remarks</span></span>  
 <span data-ttu-id="97131-112">La taille du tableau doit être égale au nombre de bits définis à l’autre dans le masque de bits.</span><span class="sxs-lookup"><span data-stu-id="97131-112">The size of the array should be equal to the number of bits set to one in the bit mask.</span></span> <span data-ttu-id="97131-113">Le `regCount` paramètre spécifie le nombre d’éléments dans la mémoire tampon qui recevra les valeurs de Registre.</span><span class="sxs-lookup"><span data-stu-id="97131-113">The `regCount` parameter specifies the number of elements in the buffer that will receive the register values.</span></span> <span data-ttu-id="97131-114">Si le `regCount` valeur est trop petite pour le nombre de registres indiqué par le masque, les registres plus élevées seront tronquées à partir de l’ensemble.</span><span class="sxs-lookup"><span data-stu-id="97131-114">If the `regCount` value is too small for the number of registers indicated by the mask, the higher numbered registers will be truncated from the set.</span></span> <span data-ttu-id="97131-115">Si le `regCount` valeur est trop volumineux, l’inutilisé `regBuffer` éléments ne sont pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="97131-115">If the `regCount` value is too large, the unused `regBuffer` elements will be unmodified.</span></span>  
  
 <span data-ttu-id="97131-116">Si le masque de bits spécifie un Registre qui n’est pas disponible, `GetRegisters` retourne une valeur indéterminée pour ce Registre.</span><span class="sxs-lookup"><span data-stu-id="97131-116">If the bit mask specifies a register that is unavailable, `GetRegisters` returns an indeterminate value for that register.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="97131-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="97131-117">Requirements</span></span>  
 <span data-ttu-id="97131-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="97131-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="97131-119">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="97131-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="97131-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="97131-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="97131-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="97131-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97131-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97131-122">See also</span></span>
- [<span data-ttu-id="97131-123">ICorDebugRegisterSet, interface</span><span class="sxs-lookup"><span data-stu-id="97131-123">ICorDebugRegisterSet Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)
- [<span data-ttu-id="97131-124">ICorDebugRegisterSet2, interface</span><span class="sxs-lookup"><span data-stu-id="97131-124">ICorDebugRegisterSet2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
