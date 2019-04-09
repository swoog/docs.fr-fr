---
title: ICorDebugNativeFrame::CanSetIP, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.CanSetIP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::CanSetIP
helpviewer_keywords:
- ICorDebugNativeFrame::CanSetIP method [.NET Framework debugging]
- CanSetIP method, ICorDebugNativeFrame interface [.NET Framework debugging]
ms.assetid: 13258ac6-f4e4-4f66-8fc3-f1244417a3c3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bd16db8c009fe81f2674a8bf9c7ad3a2a4827777
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59092849"
---
# <a name="icordebugnativeframecansetip-method"></a><span data-ttu-id="985bd-102">ICorDebugNativeFrame::CanSetIP, méthode</span><span class="sxs-lookup"><span data-stu-id="985bd-102">ICorDebugNativeFrame::CanSetIP Method</span></span>
<span data-ttu-id="985bd-103">Obtient une valeur HRESULT qui indique s’il est sans risque de définir le pointeur d’instruction (IP) à l’emplacement de décalage spécifié dans le code natif.</span><span class="sxs-lookup"><span data-stu-id="985bd-103">Gets an HRESULT that indicates whether it is safe to set the instruction pointer (IP) to the specified offset location in native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="985bd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="985bd-104">Syntax</span></span>  
  
```  
HRESULT CanSetIP (  
    [in] ULONG32            nOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="985bd-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="985bd-105">Parameters</span></span>  
 `nOffset`  
 <span data-ttu-id="985bd-106">[in] Le paramètre souhaité pour le pointeur d’instruction.</span><span class="sxs-lookup"><span data-stu-id="985bd-106">[in] The desired setting for the instruction pointer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="985bd-107">Notes</span><span class="sxs-lookup"><span data-stu-id="985bd-107">Remarks</span></span>  
 <span data-ttu-id="985bd-108">Utilisez le `CanSetIP` méthode avant d’appeler le [ICorDebugNativeFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-setip-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="985bd-108">Use the `CanSetIP` method prior to calling the [ICorDebugNativeFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-setip-method.md) method.</span></span> <span data-ttu-id="985bd-109">Si `CanSetIP` retourne un HRESULT autre que S_OK, vous pouvez toujours appeler `ICorDebugNativeFrame::SetIP`, mais il n’existe aucune garantie que le débogueur continue l’exécution sécurisée et correcte du code en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="985bd-109">If `CanSetIP` returns any HRESULT other than S_OK, you can still invoke `ICorDebugNativeFrame::SetIP`, but there is no guarantee that the debugger will continue the safe and correct execution of the code being debugged.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="985bd-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="985bd-110">Requirements</span></span>  
 <span data-ttu-id="985bd-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="985bd-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="985bd-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="985bd-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="985bd-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="985bd-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="985bd-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="985bd-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="985bd-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="985bd-115">See also</span></span>
