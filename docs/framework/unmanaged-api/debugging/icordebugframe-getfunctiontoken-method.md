---
title: ICorDebugFrame::GetFunctionToken, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetFunctionToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetFunctionToken
helpviewer_keywords:
- ICorDebugFrame::GetFunctionToken method [.NET Framework debugging]
- GetFunctionToken method [.NET Framework debugging]
ms.assetid: a46925b3-3bf8-404f-9f30-a86ae41032c1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 156c16f73916d2b4efa1c1b3541a772fb43dd470
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61988765"
---
# <a name="icordebugframegetfunctiontoken-method"></a><span data-ttu-id="15a77-102">ICorDebugFrame::GetFunctionToken, méthode</span><span class="sxs-lookup"><span data-stu-id="15a77-102">ICorDebugFrame::GetFunctionToken Method</span></span>
<span data-ttu-id="15a77-103">Obtient le jeton de métadonnées pour la fonction qui contient le code associé à ce frame de pile.</span><span class="sxs-lookup"><span data-stu-id="15a77-103">Gets the metadata token for the function that contains the code associated with this stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="15a77-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15a77-104">Syntax</span></span>  
  
```  
HRESULT GetFunctionToken (  
    [out] mdMethodDef        *pToken  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="15a77-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15a77-105">Parameters</span></span>  
 `pToken`  
 <span data-ttu-id="15a77-106">[out] Un pointeur vers un `mdMethodDef` jeton qui référence les métadonnées pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="15a77-106">[out] A pointer to an `mdMethodDef` token that references the metadata for the function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="15a77-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15a77-107">Requirements</span></span>  
 <span data-ttu-id="15a77-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="15a77-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="15a77-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="15a77-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="15a77-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="15a77-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="15a77-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="15a77-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
