---
title: ICorDebugCode::CreateBreakpoint, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCode.CreateBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::CreateBreakpoint
helpviewer_keywords:
- ICorDebugCode::CreateBreakpoint method [.NET Framework debugging]
- CreateBreakpoint method, ICorDebugCode interface [.NET Framework debugging]
ms.assetid: 46842618-0fe4-480b-871c-82fba82d23d9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d193f9aa4d051baa73944545d28a455495aeda40
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59185768"
---
# <a name="icordebugcodecreatebreakpoint-method"></a><span data-ttu-id="2cf24-102">ICorDebugCode::CreateBreakpoint, méthode</span><span class="sxs-lookup"><span data-stu-id="2cf24-102">ICorDebugCode::CreateBreakpoint Method</span></span>
<span data-ttu-id="2cf24-103">Crée un point d’arrêt dans ce segment de code à l’offset spécifié.</span><span class="sxs-lookup"><span data-stu-id="2cf24-103">Creates a breakpoint in this code segment at the specified offset.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2cf24-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2cf24-104">Syntax</span></span>  
  
```  
HRESULT CreateBreakpoint (  
    [in] ULONG32     offset,  
    [out] ICorDebugFunctionBreakpoint **ppBreakpoint  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2cf24-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2cf24-105">Parameters</span></span>  
 `offset`  
 <span data-ttu-id="2cf24-106">[in] Le décalage à partir duquel créer le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="2cf24-106">[in] The offset at which to create the breakpoint.</span></span>  
  
 `ppBreakpoint`  
 <span data-ttu-id="2cf24-107">[out] Pointeur vers l’adresse d’un objet « ICorDebugFunctionBreakpoint » qui représente le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="2cf24-107">[out] A pointer to the address of an "ICorDebugFunctionBreakpoint" object that represents the breakpoint.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2cf24-108">Notes</span><span class="sxs-lookup"><span data-stu-id="2cf24-108">Remarks</span></span>  
 <span data-ttu-id="2cf24-109">Avant le point d’arrêt est actif, il doit être ajouté à l’objet de processus.</span><span class="sxs-lookup"><span data-stu-id="2cf24-109">Before the breakpoint is active, it must be added to the process object.</span></span>  
  
 <span data-ttu-id="2cf24-110">Si ce code est le code Microsoft intermediate language (MSIL), et il existe un juste-à-temps (JIT)-version native compilée du code, le point d’arrêt sera appliquée dans le code compilé par JIT.</span><span class="sxs-lookup"><span data-stu-id="2cf24-110">If this code is Microsoft intermediate language (MSIL) code, and there is a just-in-time (JIT)-compiled, native version of the code, the breakpoint will be applied in the JIT-compiled code as well.</span></span> <span data-ttu-id="2cf24-111">(Le même est vrai si le code est compilé par JIT ultérieurement).</span><span class="sxs-lookup"><span data-stu-id="2cf24-111">(The same is true if the code is JIT-compiled later.)</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2cf24-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2cf24-112">Requirements</span></span>  
 <span data-ttu-id="2cf24-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2cf24-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2cf24-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2cf24-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2cf24-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2cf24-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="2cf24-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="2cf24-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="2cf24-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cf24-117">See also</span></span>
