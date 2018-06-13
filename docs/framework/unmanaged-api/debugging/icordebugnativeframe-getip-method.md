---
title: ICorDebugNativeFrame::GetIP, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetIP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetIP
helpviewer_keywords:
- GetIP method, ICorDebugNativeFrame interface [.NET Framework debugging]
- ICorDebugNativeFrame::GetIP method [.NET Framework debugging]
ms.assetid: 99f693f3-d3b9-4fd8-9d09-b8efd03f7b67
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7d17ac4230296674381c87851377fcb535837ad3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416817"
---
# <a name="icordebugnativeframegetip-method"></a><span data-ttu-id="bdbe9-102">ICorDebugNativeFrame::GetIP, méthode</span><span class="sxs-lookup"><span data-stu-id="bdbe9-102">ICorDebugNativeFrame::GetIP Method</span></span>
<span data-ttu-id="bdbe9-103">Obtient le code natif offset emplacement auquel le pointeur d’instruction est actuellement défini.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-103">Gets the native code offset location to which the instruction pointer is currently set.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdbe9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdbe9-104">Syntax</span></span>  
  
```  
HRESULT GetIP (  
    [out] ULONG32           *pnOffset  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bdbe9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdbe9-105">Parameters</span></span>  
 `pnOffset`  
 <span data-ttu-id="bdbe9-106">[out] Pointeur vers l’emplacement de décalage dans le code natif.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-106">[out] A pointer to the offset location in the native code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bdbe9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="bdbe9-107">Remarks</span></span>  
 <span data-ttu-id="bdbe9-108">Si le frame de pile qui est représenté par ce « ICorDebugNativeFrame » est actif, le décalage est l’adresse de l’instruction suivante à exécuter.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-108">If the stack frame that is represented by this "ICorDebugNativeFrame" is active, the offset is the address of the next instruction to be executed.</span></span> <span data-ttu-id="bdbe9-109">Si ce frame de pile n’est pas actif, le décalage est l’adresse de l’instruction suivante à exécuter lorsque le frame de pile est réactivé.</span><span class="sxs-lookup"><span data-stu-id="bdbe9-109">If this stack frame is not active, the offset is the address of the next instruction to be executed when the stack frame is reactivated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bdbe9-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bdbe9-110">Requirements</span></span>  
 <span data-ttu-id="bdbe9-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bdbe9-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bdbe9-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bdbe9-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bdbe9-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bdbe9-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bdbe9-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bdbe9-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bdbe9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdbe9-115">See Also</span></span>  
 
