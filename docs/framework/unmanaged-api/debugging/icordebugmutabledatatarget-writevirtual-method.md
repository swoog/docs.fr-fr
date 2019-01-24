---
title: ICorDebugMutableDataTarget::WriteVirtual, méthode
ms.date: 03/30/2017
ms.assetid: 80833648-58a7-491a-8dc8-9a48e9bb3adc
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1c0f07e02ee92fda772a44fe235c3dcb414882bc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54495966"
---
# <a name="icordebugmutabledatatargetwritevirtual-method"></a><span data-ttu-id="16181-102">ICorDebugMutableDataTarget::WriteVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="16181-102">ICorDebugMutableDataTarget::WriteVirtual Method</span></span>
<span data-ttu-id="16181-103">Écrit la mémoire dans l'espace d'adressage du processus cible.</span><span class="sxs-lookup"><span data-stu-id="16181-103">Writes memory into the target process address space.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="16181-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16181-104">Syntax</span></span>  
  
```  
HRESULT WriteVirtual(  
   [in] CORDB_ADDRESS address,  
   [in, size_is(bytesRequested)] const BYTE * pBuffer,  
   [in] ULONG32 bytesRequested);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="16181-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16181-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="16181-106">[in] Adresse à laquelle le contenu de `pBuffer` doit être écrit.</span><span class="sxs-lookup"><span data-stu-id="16181-106">[in] The address at which to write the contents of `pBuffer`.</span></span>  
  
 `pBuffer`  
 <span data-ttu-id="16181-107">[in] Pointeur vers un tableau d'octets contenant les octets à écrire.</span><span class="sxs-lookup"><span data-stu-id="16181-107">[in] A pointer to a byte array that contains the bytes to be written.</span></span>  
  
 `address`  
 <span data-ttu-id="16181-108">[in] Nombre d'octets dans `pBuffer`.</span><span class="sxs-lookup"><span data-stu-id="16181-108">[in] The number of bytes in `pBuffer`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="16181-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="16181-109">Return Value</span></span>  
 <span data-ttu-id="16181-110">`S_OK` en cas de réussite ou tout autre `HRESULT` en cas d'échec.</span><span class="sxs-lookup"><span data-stu-id="16181-110">`S_OK` on success, or any other `HRESULT` on failure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="16181-111">Notes</span><span class="sxs-lookup"><span data-stu-id="16181-111">Remarks</span></span>  
 <span data-ttu-id="16181-112">Si des octets ne peuvent pas être écrits, l'appel de méthode échoue sans aucune modification des octets dans l'espace d'adressage cible.</span><span class="sxs-lookup"><span data-stu-id="16181-112">If any bytes cannot be written, the method call fails without changing any bytes in the target address space.</span></span> <span data-ttu-id="16181-113">(Sinon, la cible se retrouve dans un état incohérent qui rend toute opération de débogage supplémentaire peu fiable.)</span><span class="sxs-lookup"><span data-stu-id="16181-113">(Otherwise, the target would be in an inconsistent state that makes further debugging unreliable.)</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="16181-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="16181-114">Requirements</span></span>  
 <span data-ttu-id="16181-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="16181-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="16181-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="16181-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="16181-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="16181-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="16181-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="16181-118">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="16181-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16181-119">See also</span></span>
- [<span data-ttu-id="16181-120">ICorDebugMutableDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="16181-120">ICorDebugMutableDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmutabledatatarget-interface.md)
- [<span data-ttu-id="16181-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="16181-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
