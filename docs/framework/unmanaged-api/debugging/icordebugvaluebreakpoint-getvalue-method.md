---
title: ICorDebugValueBreakpoint::GetValue, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugValueBreakpoint.GetValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValueBreakpoint::GetValue
helpviewer_keywords:
- GetValue method, ICorDebugValueBreakpoint interface [.NET Framework debugging]
- ICorDebugValueBreakpoint::GetValue method [.NET Framework debugging]
ms.assetid: 52a73654-bc47-48b6-b2b1-a4456b10140c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: acdfddd015013215bba9039d871837a60ead1405
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59175087"
---
# <a name="icordebugvaluebreakpointgetvalue-method"></a><span data-ttu-id="7af92-102">ICorDebugValueBreakpoint::GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="7af92-102">ICorDebugValueBreakpoint::GetValue Method</span></span>
<span data-ttu-id="7af92-103">Obtient un pointeur d’interface vers un objet « ICorDebugValue » qui représente la valeur de l’objet sur lequel le point d’arrêt est défini.</span><span class="sxs-lookup"><span data-stu-id="7af92-103">Gets an interface pointer to an "ICorDebugValue" object that represents the value of the object on which the breakpoint is set.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7af92-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7af92-104">Syntax</span></span>  
  
```  
HRESULT GetValue (  
    [out] ICorDebugValue   **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7af92-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7af92-105">Parameters</span></span>  
 `ppValue`  
 <span data-ttu-id="7af92-106">[out] Un pointeur vers l’adresse d’un `ICorDebugValue` objet.</span><span class="sxs-lookup"><span data-stu-id="7af92-106">[out] A pointer to the address of an `ICorDebugValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7af92-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7af92-107">Requirements</span></span>  
 <span data-ttu-id="7af92-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7af92-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7af92-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7af92-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7af92-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7af92-110">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="7af92-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="7af92-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="7af92-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7af92-112">See also</span></span>
