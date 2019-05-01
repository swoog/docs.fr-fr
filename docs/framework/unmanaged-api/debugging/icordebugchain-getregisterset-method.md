---
title: ICorDebugChain::GetRegisterSet, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetRegisterSet
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetRegisterSet
helpviewer_keywords:
- ICorDebugChain::GetRegisterSet method [.NET Framework debugging]
- GetRegisterSet method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: bc4288b6-3331-4ae3-990d-e1d6e62ecb67
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f366a40e1e3cd196f480c5849c49419c7daeea9e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61989480"
---
# <a name="icordebugchaingetregisterset-method"></a><span data-ttu-id="72c26-102">ICorDebugChain::GetRegisterSet, méthode</span><span class="sxs-lookup"><span data-stu-id="72c26-102">ICorDebugChain::GetRegisterSet Method</span></span>
<span data-ttu-id="72c26-103">Obtient le jeu de registres pour la partie active de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="72c26-103">Gets the register set for the active part of this chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72c26-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72c26-104">Syntax</span></span>  
  
```  
HRESULT GetRegisterSet (  
    [out] ICorDebugRegisterSet **ppRegisters  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="72c26-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72c26-105">Parameters</span></span>  
 `ppRegisters`  
 <span data-ttu-id="72c26-106">[out] Un pointeur vers l’adresse d’un [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) objet qui représente le Registre défini pour la partie active de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="72c26-106">[out] A pointer to the address of an [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) object that represents the register set for the active part of this chain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="72c26-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72c26-107">Requirements</span></span>  
 <span data-ttu-id="72c26-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="72c26-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="72c26-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="72c26-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="72c26-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="72c26-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="72c26-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="72c26-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
