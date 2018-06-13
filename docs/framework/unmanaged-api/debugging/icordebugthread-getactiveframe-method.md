---
title: ICorDebugThread::GetActiveFrame, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetActiveFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetActiveFrame
helpviewer_keywords:
- ICorDebugThread::GetActiveFrame method [.NET Framework debugging]
- GetActiveFrame method, ICorDebugThread interface [.NET Framework debugging]
ms.assetid: 8d6d3a1a-fef6-4f2f-a22c-3bdd30d70e07
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6a1bbe5674ba11b5ee6033c65f229d698eff15ae
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420639"
---
# <a name="icordebugthreadgetactiveframe-method"></a><span data-ttu-id="96fc8-102">ICorDebugThread::GetActiveFrame, méthode</span><span class="sxs-lookup"><span data-stu-id="96fc8-102">ICorDebugThread::GetActiveFrame Method</span></span>
<span data-ttu-id="96fc8-103">Obtient un pointeur d’interface vers le frame actif (plus récent) sur cet objet ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="96fc8-103">Gets an interface pointer to the active (most recent) frame on this ICorDebugThread object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96fc8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96fc8-104">Syntax</span></span>  
  
```  
HRESULT GetActiveFrame (  
    [out] ICorDebugFrame   **ppFrame  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="96fc8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96fc8-105">Parameters</span></span>  
 `ppFrame`  
 <span data-ttu-id="96fc8-106">[out] Pointeur vers l’adresse d’un objet d’interface ICorDebugFrame qui représente un frame.</span><span class="sxs-lookup"><span data-stu-id="96fc8-106">[out] A pointer to the address of an ICorDebugFrame interface object that represents a frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="96fc8-107">Notes</span><span class="sxs-lookup"><span data-stu-id="96fc8-107">Remarks</span></span>  
 <span data-ttu-id="96fc8-108">Le `ppFrame` paramètre est null si aucune image n’est actuellement actif.</span><span class="sxs-lookup"><span data-stu-id="96fc8-108">The `ppFrame` parameter is null if no frame is currently active.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="96fc8-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="96fc8-109">Requirements</span></span>  
 <span data-ttu-id="96fc8-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="96fc8-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="96fc8-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="96fc8-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="96fc8-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="96fc8-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="96fc8-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="96fc8-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
