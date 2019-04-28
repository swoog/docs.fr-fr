---
title: ICorDebugAppDomain::IsAttached, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.IsAttached
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::IsAttached
helpviewer_keywords:
- IsAttached method [.NET Framework debugging]
- ICorDebugAppDomain::IsAttached method [.NET Framework debugging]
ms.assetid: af0c67c7-f53e-47c9-b84b-be50bd04903e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fa9576f568ef1f6da3eef812abb9674aa0d81dfb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61996162"
---
# <a name="icordebugappdomainisattached-method"></a><span data-ttu-id="08a35-102">ICorDebugAppDomain::IsAttached, méthode</span><span class="sxs-lookup"><span data-stu-id="08a35-102">ICorDebugAppDomain::IsAttached Method</span></span>
<span data-ttu-id="08a35-103">Obtient une valeur qui indique si le débogueur est attaché au domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="08a35-103">Gets a value that indicates whether the debugger is attached to the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08a35-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08a35-104">Syntax</span></span>  
  
```  
HRESULT IsAttached (  
    [out] BOOL  *pbAttached  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="08a35-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08a35-105">Parameters</span></span>  
 `pbAttached`  
 <span data-ttu-id="08a35-106">[out] `true` si le débogueur est attaché au domaine d’application ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="08a35-106">[out] `true` if the debugger is attached to the application domain; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="08a35-107">Notes</span><span class="sxs-lookup"><span data-stu-id="08a35-107">Remarks</span></span>  
 <span data-ttu-id="08a35-108">Les méthodes ICorDebugController ne peut pas être utilisés jusqu'à ce que le débogueur est attaché au domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="08a35-108">The ICorDebugController methods cannot be used until the debugger attaches to the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08a35-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08a35-109">Requirements</span></span>  
 <span data-ttu-id="08a35-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="08a35-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="08a35-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="08a35-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="08a35-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="08a35-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="08a35-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="08a35-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
