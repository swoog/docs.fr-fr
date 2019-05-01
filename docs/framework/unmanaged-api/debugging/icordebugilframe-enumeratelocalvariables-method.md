---
title: ICorDebugILFrame::EnumerateLocalVariables, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.EnumerateLocalVariables
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::EnumerateLocalVariables
helpviewer_keywords:
- EnumerateLocalVariables method [.NET Framework debugging]
- ICorDebugILFrame::EnumerateLocalVariables method [.NET Framework debugging]
ms.assetid: 1a67fa1b-2419-4cd0-aad4-6f46a0719b4b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3cc9601105d05740e6db0a41bae521bd9a276d74
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61988648"
---
# <a name="icordebugilframeenumeratelocalvariables-method"></a><span data-ttu-id="eae43-102">ICorDebugILFrame::EnumerateLocalVariables, méthode</span><span class="sxs-lookup"><span data-stu-id="eae43-102">ICorDebugILFrame::EnumerateLocalVariables Method</span></span>
<span data-ttu-id="eae43-103">Obtient un énumérateur pour les variables locales dans ce frame.</span><span class="sxs-lookup"><span data-stu-id="eae43-103">Gets an enumerator for the local variables in this frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eae43-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eae43-104">Syntax</span></span>  
  
```  
HRESULT EnumerateLocalVariables(   
    [out] ICorDebugValueEnum    **ppValueEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eae43-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eae43-105">Parameters</span></span>  
 `ppValueEnum`  
 <span data-ttu-id="eae43-106">[out] Pointeur vers l’adresse d’un objet ICorDebugValueEnum qui est l’énumérateur pour les variables locales de ce frame.</span><span class="sxs-lookup"><span data-stu-id="eae43-106">[out] A pointer to the address of an ICorDebugValueEnum object that is the enumerator for the local variables in this frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eae43-107">Notes</span><span class="sxs-lookup"><span data-stu-id="eae43-107">Remarks</span></span>  
 <span data-ttu-id="eae43-108">`EnumerateLocalVariables` Obtient un énumérateur qui peut répertorier les variables locales disponibles dans le frame d’appel représenté par cet objet ICorDebugILFrame.</span><span class="sxs-lookup"><span data-stu-id="eae43-108">`EnumerateLocalVariables` gets an enumerator that can list the local variables available in the call frame that is represented by this ICorDebugILFrame object.</span></span> <span data-ttu-id="eae43-109">La liste ne peut-être pas inclure toutes les variables locales dans la fonction en cours d’exécution, car certains d'entre eux ne peuvent pas être actif.</span><span class="sxs-lookup"><span data-stu-id="eae43-109">The list may not include all of the local variables in the running function, because some of them may not be active.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eae43-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eae43-110">Requirements</span></span>  
 <span data-ttu-id="eae43-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eae43-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eae43-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="eae43-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="eae43-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eae43-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eae43-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eae43-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
