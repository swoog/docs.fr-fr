---
title: ICorDebugChain::GetStackRange, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetStackRange
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetStackRange
helpviewer_keywords:
- ICorDebugChain::GetStackRange method [.NET Framework debugging]
- GetStackRange method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: 554284e7-3f6c-4d40-8da5-1c9317fbd484
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 226f8c431b90d53366aa5e504101e7de581ec570
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402468"
---
# <a name="icordebugchaingetstackrange-method"></a><span data-ttu-id="c7e04-102">ICorDebugChain::GetStackRange, méthode</span><span class="sxs-lookup"><span data-stu-id="c7e04-102">ICorDebugChain::GetStackRange Method</span></span>
<span data-ttu-id="c7e04-103">Obtient la plage d’adresses du segment de pile pour cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="c7e04-103">Gets the address range of the stack segment for this chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7e04-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7e04-104">Syntax</span></span>  
  
```  
HRESULT GetStackRange (  
    [out] CORDB_ADDRESS      *pStart,   
    [out] CORDB_ADDRESS      *pEnd  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c7e04-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7e04-105">Parameters</span></span>  
 `pStart`  
 <span data-ttu-id="c7e04-106">[out] Un pointeur vers un `CORDB_ADDRESS` valeur qui est l’adresse de départ du segment de pile.</span><span class="sxs-lookup"><span data-stu-id="c7e04-106">[out] A pointer to a `CORDB_ADDRESS` value that is the starting address of the stack segment.</span></span>  
  
 `pEnd`  
 <span data-ttu-id="c7e04-107">[out] Un pointeur vers un `CORDB_ADDRESS` valeur qui est l’adresse de fin du segment de pile.</span><span class="sxs-lookup"><span data-stu-id="c7e04-107">[out] A pointer to a `CORDB_ADDRESS` value that is the ending address of the stack segment.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c7e04-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c7e04-108">Remarks</span></span>  
 <span data-ttu-id="c7e04-109">La plage numérique est utile uniquement pour la comparaison des emplacements de frame de pile.</span><span class="sxs-lookup"><span data-stu-id="c7e04-109">The numeric range is meaningful only for comparison of stack frame locations.</span></span> <span data-ttu-id="c7e04-110">Vous ne pouvez pas faire d’hypothèses sur ce qui est réellement stocké dans la pile.</span><span class="sxs-lookup"><span data-stu-id="c7e04-110">You cannot make any assumptions about what is actually stored on the stack.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c7e04-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c7e04-111">Requirements</span></span>  
 <span data-ttu-id="c7e04-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c7e04-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7e04-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c7e04-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c7e04-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c7e04-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c7e04-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7e04-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
