---
title: ICorDebugAppDomain::EnumerateBreakpoints, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.EnumerateBreakpoints
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::EnumerateBreakpoints
helpviewer_keywords:
- ICorDebugAppDomain::EnumerateBreakpoints method [.NET Framework debugging]
- EnumerateBreakpoints method [.NET Framework debugging]
ms.assetid: 206069c5-25cb-4794-9d69-67c5aa7ed0af
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b00afc900a27aea94389ee81065ea22ae359440d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61996266"
---
# <a name="icordebugappdomainenumeratebreakpoints-method"></a><span data-ttu-id="b7c82-102">ICorDebugAppDomain::EnumerateBreakpoints, méthode</span><span class="sxs-lookup"><span data-stu-id="b7c82-102">ICorDebugAppDomain::EnumerateBreakpoints Method</span></span>
<span data-ttu-id="b7c82-103">Obtient un énumérateur pour tous les points d’arrêt actifs dans le domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="b7c82-103">Gets an enumerator for all active breakpoints in the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7c82-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7c82-104">Syntax</span></span>  
  
```  
HRESULT EnumerateBreakpoints (  
    [out] ICorDebugBreakpointEnum   **ppBreakpoints  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b7c82-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7c82-105">Parameters</span></span>  
 `ppBreakpoints`  
 <span data-ttu-id="b7c82-106">[out] Pointeur vers l’adresse d’un objet ICorDebugBreakpointEnum qui est l’énumérateur pour tous les points d’arrêt actifs dans le domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="b7c82-106">[out] A pointer to the address of an ICorDebugBreakpointEnum object that is the enumerator for all active breakpoints in the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b7c82-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b7c82-107">Remarks</span></span>  
 <span data-ttu-id="b7c82-108">L’énumérateur inclut tous les types de points d’arrêt, y compris les points d’arrêt de la fonction et les points d’arrêt de données.</span><span class="sxs-lookup"><span data-stu-id="b7c82-108">The enumerator includes all types of breakpoints, including function breakpoints and data breakpoints.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7c82-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7c82-109">Requirements</span></span>  
 <span data-ttu-id="b7c82-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b7c82-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7c82-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b7c82-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b7c82-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b7c82-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b7c82-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7c82-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
