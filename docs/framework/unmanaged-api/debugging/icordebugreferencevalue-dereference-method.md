---
title: ICorDebugReferenceValue::Dereference, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugReferenceValue.Dereference
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue::Dereference
helpviewer_keywords:
- ICorDebugReferenceValue::Dereference method [.NET Framework debugging]
- Dereference method [.NET Framework debugging]
ms.assetid: 5ec8cf76-3deb-4ce6-9a49-77a4c35d80b9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b436fa14322d444a6c8b515ba8e50698eecb95ba
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61783017"
---
# <a name="icordebugreferencevaluedereference-method"></a><span data-ttu-id="c6b27-102">ICorDebugReferenceValue::Dereference, méthode</span><span class="sxs-lookup"><span data-stu-id="c6b27-102">ICorDebugReferenceValue::Dereference Method</span></span>
<span data-ttu-id="c6b27-103">Obtient l’objet qui est référencé.</span><span class="sxs-lookup"><span data-stu-id="c6b27-103">Gets the object that is referenced.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c6b27-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6b27-104">Syntax</span></span>  
  
```  
HRESULT Dereference (  
    [out] ICorDebugValue  **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c6b27-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6b27-105">Parameters</span></span>  
 `ppValue`  
 <span data-ttu-id="c6b27-106">[out] Pointeur vers l’adresse d’un ICorDebugValue qui représente l’objet vers lequel pointe cet objet ICorDebugReferenceValue.</span><span class="sxs-lookup"><span data-stu-id="c6b27-106">[out] A pointer to the address of an ICorDebugValue that represents the object to which this ICorDebugReferenceValue object points.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c6b27-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c6b27-107">Remarks</span></span>  
 <span data-ttu-id="c6b27-108">Le `ICorDebugValue` objet est valide uniquement lorsque sa référence n’a pas encore été désactivé.</span><span class="sxs-lookup"><span data-stu-id="c6b27-108">The `ICorDebugValue` object is valid only while its reference has not yet been disabled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c6b27-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6b27-109">Requirements</span></span>  
 <span data-ttu-id="c6b27-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c6b27-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c6b27-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c6b27-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c6b27-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c6b27-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c6b27-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c6b27-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
