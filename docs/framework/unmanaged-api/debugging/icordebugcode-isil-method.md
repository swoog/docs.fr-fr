---
title: ICorDebugCode::IsIL, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCode.IsIL
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::IsIL
helpviewer_keywords:
- ICorDebugCode::IsIL method [.NET Framework debugging]
- IsIL method [.NET Framework debugging]
ms.assetid: 132ef8cc-d938-43f3-b8f2-e3b97c0ceb33
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a82606d90444c2d543065287780e42da4f8b4943
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59180685"
---
# <a name="icordebugcodeisil-method"></a><span data-ttu-id="b7895-102">ICorDebugCode::IsIL, méthode</span><span class="sxs-lookup"><span data-stu-id="b7895-102">ICorDebugCode::IsIL Method</span></span>
<span data-ttu-id="b7895-103">Obtient une valeur qui indique si ce « ICorDebugCode » représente le code qui a été compilé en langage intermédiaire Microsoft (MSIL).</span><span class="sxs-lookup"><span data-stu-id="b7895-103">Gets a value that indicates whether this "ICorDebugCode" represents code that was compiled in Microsoft intermediate language (MSIL).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7895-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7895-104">Syntax</span></span>  
  
```  
HRESULT IsIL (  
    [out] BOOL       *pbIL  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b7895-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7895-105">Parameters</span></span>  
 `pbIL`  
 <span data-ttu-id="b7895-106">[out] `true` si ce `ICorDebugCode` représente le code qui a été compilé dans le langage MSIL ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="b7895-106">[out] `true` if this `ICorDebugCode` represents code that was compiled in MSIL; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7895-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7895-107">Requirements</span></span>  
 <span data-ttu-id="b7895-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b7895-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7895-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b7895-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b7895-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b7895-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b7895-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7895-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7895-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7895-112">See also</span></span>
