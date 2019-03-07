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
ms.openlocfilehash: 051491173bbcef3d87d9a3dbe854eece46c49e0d
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57468778"
---
# <a name="icordebugthreadgetactiveframe-method"></a><span data-ttu-id="65f31-102">ICorDebugThread::GetActiveFrame, méthode</span><span class="sxs-lookup"><span data-stu-id="65f31-102">ICorDebugThread::GetActiveFrame Method</span></span>
<span data-ttu-id="65f31-103">Obtient un pointeur d’interface vers le frame actif (la plus récent) sur cet objet ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="65f31-103">Gets an interface pointer to the active (most recent) frame on this ICorDebugThread object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65f31-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65f31-104">Syntax</span></span>  
  
```  
HRESULT GetActiveFrame (  
    [out] ICorDebugFrame   **ppFrame  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="65f31-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65f31-105">Parameters</span></span>  
 `ppFrame`  
 <span data-ttu-id="65f31-106">[out] Pointeur vers l’adresse d’un objet d’interface ICorDebugFrame qui représente un frame.</span><span class="sxs-lookup"><span data-stu-id="65f31-106">[out] A pointer to the address of an ICorDebugFrame interface object that represents a frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="65f31-107">Notes</span><span class="sxs-lookup"><span data-stu-id="65f31-107">Remarks</span></span>  
 <span data-ttu-id="65f31-108">Le `ppFrame` paramètre a la valeur null si aucune image n’est actuellement actif.</span><span class="sxs-lookup"><span data-stu-id="65f31-108">The `ppFrame` parameter is null if no frame is currently active.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="65f31-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="65f31-109">Requirements</span></span>  
 <span data-ttu-id="65f31-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="65f31-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="65f31-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="65f31-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="65f31-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="65f31-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="65f31-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="65f31-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
