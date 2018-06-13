---
title: ICorDebugFrame::GetChain, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetChain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetChain
helpviewer_keywords:
- ICorDebugFrame::GetChain method [.NET Framework debugging]
- GetChain method [.NET Framework debugging]
ms.assetid: e28e51d3-8f73-494f-bcd4-48bac239fbe1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 06c020b9f6c074be11e3433939ce6898586123cd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33412605"
---
# <a name="icordebugframegetchain-method"></a><span data-ttu-id="ca1d4-102">ICorDebugFrame::GetChain, méthode</span><span class="sxs-lookup"><span data-stu-id="ca1d4-102">ICorDebugFrame::GetChain Method</span></span>
<span data-ttu-id="ca1d4-103">Obtient un pointeur vers la chaîne de que cette image fait partie.</span><span class="sxs-lookup"><span data-stu-id="ca1d4-103">Gets a pointer to the chain this frame is a part of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca1d4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca1d4-104">Syntax</span></span>  
  
```  
HRESULT GetChain (  
    [out] ICorDebugChain     **ppChain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ca1d4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca1d4-105">Parameters</span></span>  
 `ppChain`  
 <span data-ttu-id="ca1d4-106">[out] Pointeur vers l’adresse d’un objet ICorDebugChain qui représente la chaîne contenant ce frame.</span><span class="sxs-lookup"><span data-stu-id="ca1d4-106">[out] A pointer to the address of an ICorDebugChain object that represents the chain containing this frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca1d4-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ca1d4-107">Requirements</span></span>  
 <span data-ttu-id="ca1d4-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ca1d4-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca1d4-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ca1d4-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ca1d4-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ca1d4-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ca1d4-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca1d4-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
