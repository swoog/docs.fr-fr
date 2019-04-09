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
ms.openlocfilehash: 38f913b742f7ece2f136454f801ae780124aed87
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59073531"
---
# <a name="icordebugnativeframegetip-method"></a><span data-ttu-id="9e6a1-102">ICorDebugNativeFrame::GetIP, méthode</span><span class="sxs-lookup"><span data-stu-id="9e6a1-102">ICorDebugNativeFrame::GetIP Method</span></span>
<span data-ttu-id="9e6a1-103">Obtient le code natif décalage emplacement auquel le pointeur d’instruction est actuellement défini.</span><span class="sxs-lookup"><span data-stu-id="9e6a1-103">Gets the native code offset location to which the instruction pointer is currently set.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9e6a1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e6a1-104">Syntax</span></span>  
  
```  
HRESULT GetIP (  
    [out] ULONG32           *pnOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9e6a1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e6a1-105">Parameters</span></span>  
 `pnOffset`  
 <span data-ttu-id="9e6a1-106">[out] Pointeur vers l’emplacement de décalage dans le code natif.</span><span class="sxs-lookup"><span data-stu-id="9e6a1-106">[out] A pointer to the offset location in the native code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9e6a1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="9e6a1-107">Remarks</span></span>  
 <span data-ttu-id="9e6a1-108">Si le frame de pile est représenté par ce « ICorDebugNativeFrame » est actif, le décalage est l’adresse de la prochaine instruction à exécuter.</span><span class="sxs-lookup"><span data-stu-id="9e6a1-108">If the stack frame that is represented by this "ICorDebugNativeFrame" is active, the offset is the address of the next instruction to be executed.</span></span> <span data-ttu-id="9e6a1-109">Si ce frame de pile n’est pas actif, le décalage est l’adresse de l’instruction suivante à exécuter lorsque le frame de pile est réactivé.</span><span class="sxs-lookup"><span data-stu-id="9e6a1-109">If this stack frame is not active, the offset is the address of the next instruction to be executed when the stack frame is reactivated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9e6a1-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e6a1-110">Requirements</span></span>  
 <span data-ttu-id="9e6a1-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9e6a1-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9e6a1-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9e6a1-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9e6a1-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9e6a1-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="9e6a1-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="9e6a1-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="9e6a1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e6a1-115">See also</span></span>
