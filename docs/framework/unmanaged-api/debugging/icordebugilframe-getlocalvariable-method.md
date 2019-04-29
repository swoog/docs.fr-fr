---
title: ICorDebugILFrame::GetLocalVariable, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.GetLocalVariable
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::GetLocalVariable
helpviewer_keywords:
- ICorDebugILFrame::GetLocalVariable method [.NET Framework debugging]
- GetLocalVariable method [.NET Framework debugging]
ms.assetid: c8706356-d50b-4f87-a40c-39c3b7f4fd38
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ebd36f01297f24c050f84fb67e7673f8641fe206
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789712"
---
# <a name="icordebugilframegetlocalvariable-method"></a><span data-ttu-id="fca39-102">ICorDebugILFrame::GetLocalVariable, méthode</span><span class="sxs-lookup"><span data-stu-id="fca39-102">ICorDebugILFrame::GetLocalVariable Method</span></span>
<span data-ttu-id="fca39-103">Obtient la valeur de la variable locale spécifiée dans ce frame de pile Microsoft intermediate language (MSIL).</span><span class="sxs-lookup"><span data-stu-id="fca39-103">Gets the value of the specified local variable in this Microsoft intermediate language (MSIL) stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fca39-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fca39-104">Syntax</span></span>  
  
```  
HRESULT GetLocalVariable (  
    [in] DWORD                  dwIndex,  
    [out] ICorDebugValue        **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fca39-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fca39-105">Parameters</span></span>  
 `dwIndex`  
 <span data-ttu-id="fca39-106">[in] Index de la variable locale dans ce frame de pile MSIL.</span><span class="sxs-lookup"><span data-stu-id="fca39-106">[in] The index of the local variable in this MSIL stack frame.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="fca39-107">[out] Pointeur vers l’adresse d’un objet ICorDebugValue qui représente la valeur récupérée.</span><span class="sxs-lookup"><span data-stu-id="fca39-107">[out] A pointer to the address of an ICorDebugValue object that represents the retrieved value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fca39-108">Notes</span><span class="sxs-lookup"><span data-stu-id="fca39-108">Remarks</span></span>  
 <span data-ttu-id="fca39-109">Le `GetLocalVariable` méthode peut être utilisée dans un frame de pile MSIL ou dans un frame compilé juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="fca39-109">The `GetLocalVariable` method can be used either in an MSIL stack frame or in a just-in-time (JIT) compiled frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fca39-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fca39-110">Requirements</span></span>  
 <span data-ttu-id="fca39-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fca39-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fca39-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fca39-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fca39-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fca39-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fca39-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fca39-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
