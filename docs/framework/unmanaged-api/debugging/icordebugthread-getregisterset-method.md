---
title: ICorDebugThread::GetRegisterSet, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetRegisterSet
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetRegisterSet
helpviewer_keywords:
- ICorDebugThread::GetRegisterSet method [.NET Framework debugging]
- GetRegisterSet method, ICorDebugThread interface [.NET Framework debugging]
ms.assetid: 3b9b6260-98ac-4cfd-88e5-5d7614f94a0c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 909bcad035516c494d1f867b71bb8f52939eba13
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61993991"
---
# <a name="icordebugthreadgetregisterset-method"></a><span data-ttu-id="63465-102">ICorDebugThread::GetRegisterSet, méthode</span><span class="sxs-lookup"><span data-stu-id="63465-102">ICorDebugThread::GetRegisterSet Method</span></span>
<span data-ttu-id="63465-103">Obtient un pointeur d’interface vers le jeu de Registre qui est associé à la partie active de cet objet ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="63465-103">Gets an interface pointer to the register set that is associated with the active part of this ICorDebugThread object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63465-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63465-104">Syntax</span></span>  
  
```  
HRESULT GetRegisterSet (  
    [out] ICorDebugRegisterSet **ppRegisters  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="63465-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63465-105">Parameters</span></span>  
 `ppRegisters`  
 <span data-ttu-id="63465-106">[out] Un pointeur vers l’adresse d’un [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) objet d’interface qui représente le Registre est définie pour la partie active de ce thread.</span><span class="sxs-lookup"><span data-stu-id="63465-106">[out] A pointer to the address of an [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) interface object that represents the register set for the active part of this thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="63465-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63465-107">Requirements</span></span>  
 <span data-ttu-id="63465-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="63465-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="63465-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="63465-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="63465-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="63465-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="63465-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="63465-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
