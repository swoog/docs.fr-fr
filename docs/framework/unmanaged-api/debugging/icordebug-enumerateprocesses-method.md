---
title: ICorDebug::EnumerateProcesses, méthode
ms.date: 03/30/2017
api_name:
- ICorDebug.EnumerateProcesses
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- EnumerateProcesses
helpviewer_keywords:
- EnumerateProcesses method [.NET Framework debugging]
- ICorDebug::EnumerateProcesses method [.NET Framework debugging]
ms.assetid: ba25d166-1d28-4f1d-aca2-de298bbca669
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 10741ef9d329986d869665ef3aae14196946bb22
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54724419"
---
# <a name="icordebugenumerateprocesses-method"></a><span data-ttu-id="8c7e2-102">ICorDebug::EnumerateProcesses, méthode</span><span class="sxs-lookup"><span data-stu-id="8c7e2-102">ICorDebug::EnumerateProcesses Method</span></span>
<span data-ttu-id="8c7e2-103">Obtient un énumérateur pour les processus en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="8c7e2-103">Gets an enumerator for the processes that are being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8c7e2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c7e2-104">Syntax</span></span>  
  
```  
HRESULT EnumerateProcesses (  
    [out] ICorDebugProcessEnum      **ppProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8c7e2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c7e2-105">Parameters</span></span>  
 `ppProcess`  
 <span data-ttu-id="8c7e2-106">Pointeur vers l’adresse d’un objet ICorDebugProcessEnum qui est l’énumérateur pour les processus en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="8c7e2-106">A pointer to the address of an ICorDebugProcessEnum object that is the enumerator for the processes being debugged.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8c7e2-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8c7e2-107">Requirements</span></span>  
 <span data-ttu-id="8c7e2-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8c7e2-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8c7e2-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8c7e2-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8c7e2-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8c7e2-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8c7e2-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8c7e2-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8c7e2-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c7e2-112">See also</span></span>
- [<span data-ttu-id="8c7e2-113">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="8c7e2-113">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
