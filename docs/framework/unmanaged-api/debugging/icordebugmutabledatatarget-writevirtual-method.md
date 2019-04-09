---
title: ICorDebugMutableDataTarget::WriteVirtual, méthode
ms.date: 03/30/2017
ms.assetid: 80833648-58a7-491a-8dc8-9a48e9bb3adc
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2fba970de6e5882d3cbe9be17b5b49be5a3e81aa
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59171650"
---
# <a name="icordebugmutabledatatargetwritevirtual-method"></a><span data-ttu-id="66948-102">ICorDebugMutableDataTarget::WriteVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="66948-102">ICorDebugMutableDataTarget::WriteVirtual Method</span></span>
<span data-ttu-id="66948-103">Écrit la mémoire dans l'espace d'adressage du processus cible.</span><span class="sxs-lookup"><span data-stu-id="66948-103">Writes memory into the target process address space.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="66948-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66948-104">Syntax</span></span>  
  
```  
HRESULT WriteVirtual(  
   [in] CORDB_ADDRESS address,  
   [in, size_is(bytesRequested)] const BYTE * pBuffer,  
   [in] ULONG32 bytesRequested);  
```  
  
## <a name="parameters"></a><span data-ttu-id="66948-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66948-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="66948-106">[in] Adresse à laquelle le contenu de `pBuffer` doit être écrit.</span><span class="sxs-lookup"><span data-stu-id="66948-106">[in] The address at which to write the contents of `pBuffer`.</span></span>  
  
 `pBuffer`  
 <span data-ttu-id="66948-107">[in] Pointeur vers un tableau d'octets contenant les octets à écrire.</span><span class="sxs-lookup"><span data-stu-id="66948-107">[in] A pointer to a byte array that contains the bytes to be written.</span></span>  
  
 `address`  
 <span data-ttu-id="66948-108">[in] Nombre d'octets dans `pBuffer`.</span><span class="sxs-lookup"><span data-stu-id="66948-108">[in] The number of bytes in `pBuffer`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="66948-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="66948-109">Return Value</span></span>  
 `S_OK` <span data-ttu-id="66948-110">sur la réussite ou tout autre `HRESULT` en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="66948-110">on success, or any other `HRESULT` on failure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="66948-111">Notes</span><span class="sxs-lookup"><span data-stu-id="66948-111">Remarks</span></span>  
 <span data-ttu-id="66948-112">Si des octets ne peuvent pas être écrits, l'appel de méthode échoue sans aucune modification des octets dans l'espace d'adressage cible.</span><span class="sxs-lookup"><span data-stu-id="66948-112">If any bytes cannot be written, the method call fails without changing any bytes in the target address space.</span></span> <span data-ttu-id="66948-113">(Sinon, la cible se retrouve dans un état incohérent qui rend toute opération de débogage supplémentaire peu fiable.)</span><span class="sxs-lookup"><span data-stu-id="66948-113">(Otherwise, the target would be in an inconsistent state that makes further debugging unreliable.)</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="66948-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66948-114">Requirements</span></span>  
 <span data-ttu-id="66948-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="66948-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="66948-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="66948-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="66948-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="66948-117">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="66948-118">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="66948-118">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="66948-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66948-119">See also</span></span>

- [<span data-ttu-id="66948-120">ICorDebugMutableDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="66948-120">ICorDebugMutableDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmutabledatatarget-interface.md)
- [<span data-ttu-id="66948-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="66948-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
