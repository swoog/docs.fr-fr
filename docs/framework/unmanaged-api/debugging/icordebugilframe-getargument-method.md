---
title: ICorDebugILFrame::GetArgument, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.GetArgument
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::GetArgument
helpviewer_keywords:
- GetArgument method [.NET Framework debugging]
- ICorDebugILFrame::GetArgument method [.NET Framework debugging]
ms.assetid: 4e2fd423-f643-4c27-ba5f-41b5ebc3b416
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 46852ed8ac53c3a7720edff4833f3dc3cce42bbb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61995525"
---
# <a name="icordebugilframegetargument-method"></a><span data-ttu-id="ac681-102">ICorDebugILFrame::GetArgument, méthode</span><span class="sxs-lookup"><span data-stu-id="ac681-102">ICorDebugILFrame::GetArgument Method</span></span>
<span data-ttu-id="ac681-103">Obtient la valeur de l’argument spécifié dans ce frame de pile Microsoft intermediate language (MSIL).</span><span class="sxs-lookup"><span data-stu-id="ac681-103">Gets the value of the specified argument in this Microsoft intermediate language (MSIL) stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac681-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac681-104">Syntax</span></span>  
  
```  
HRESULT GetArgument (  
    [in] DWORD                  dwIndex,  
    [out] ICorDebugValue        **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ac681-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac681-105">Parameters</span></span>  
 `dwIndex`  
 <span data-ttu-id="ac681-106">[in] L’index de l’argument dans ce frame de pile MSIL.</span><span class="sxs-lookup"><span data-stu-id="ac681-106">[in] The index of the argument in this MSIL stack frame.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="ac681-107">[out] Pointeur vers l’adresse d’un objet ICorDebugValue qui représente la valeur récupérée.</span><span class="sxs-lookup"><span data-stu-id="ac681-107">[out] A pointer to the address of an ICorDebugValue object that represents the retrieved value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ac681-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ac681-108">Remarks</span></span>  
 <span data-ttu-id="ac681-109">Le `GetArgument` méthode peut être utilisée dans un frame de pile MSIL ou dans un frame compilé juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="ac681-109">The `GetArgument` method can be used either in an MSIL stack frame or in a just-in-time (JIT) compiled frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ac681-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac681-110">Requirements</span></span>  
 <span data-ttu-id="ac681-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ac681-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ac681-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ac681-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ac681-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ac681-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ac681-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ac681-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
