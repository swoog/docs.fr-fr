---
title: ICorDebugThread::GetObject, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetObject
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetObject
helpviewer_keywords:
- GetObject method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetObject method [.NET Framework debugging]
ms.assetid: 1590febe-96c2-4046-97db-d81d81d67e01
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4a188963273555e8b93b68c168260fd619136c00
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54544534"
---
# <a name="icordebugthreadgetobject-method"></a><span data-ttu-id="cd604-102">ICorDebugThread::GetObject, méthode</span><span class="sxs-lookup"><span data-stu-id="cd604-102">ICorDebugThread::GetObject Method</span></span>
<span data-ttu-id="cd604-103">Obtient un pointeur d’interface vers le thread de common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="cd604-103">Gets an interface pointer to the common language runtime (CLR) thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd604-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd604-104">Syntax</span></span>  
  
```  
HRESULT GetObject (  
    [out] ICorDebugValue   **ppObject  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cd604-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd604-105">Parameters</span></span>  
 `ppObject`  
 <span data-ttu-id="cd604-106">[out] Pointeur vers l’adresse d’un objet d’interface ICorDebugValue qui représente le thread de CLR.</span><span class="sxs-lookup"><span data-stu-id="cd604-106">[out] A pointer to the address of an ICorDebugValue interface object that represents the CLR thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd604-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cd604-107">Requirements</span></span>  
 <span data-ttu-id="cd604-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cd604-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cd604-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cd604-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cd604-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cd604-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cd604-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cd604-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd604-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd604-112">See also</span></span>
- <xref:System.Threading.Thread>
