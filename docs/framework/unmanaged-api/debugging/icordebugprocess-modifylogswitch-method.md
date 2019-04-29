---
title: ICorDebugProcess::ModifyLogSwitch, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.ModifyLogSwitch
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::ModifyLogSwitch
helpviewer_keywords:
- ICorDebugProcess::ModifyLogSwitch method [.NET Framework debugging]
- ModifyLogSwitch method [.NET Framework debugging]
ms.assetid: 5fd30875-555e-4e96-877b-5dd266cde7c4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4b1c85499e5269027da2c2a01ab67aab2c5da626
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775542"
---
# <a name="icordebugprocessmodifylogswitch-method"></a><span data-ttu-id="ac04c-102">ICorDebugProcess::ModifyLogSwitch, méthode</span><span class="sxs-lookup"><span data-stu-id="ac04c-102">ICorDebugProcess::ModifyLogSwitch Method</span></span>
<span data-ttu-id="ac04c-103">Définit le niveau de gravité du commutateur de journal spécifié.</span><span class="sxs-lookup"><span data-stu-id="ac04c-103">Sets the severity level of the specified log switch.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac04c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac04c-104">Syntax</span></span>  
  
```  
HRESULT ModifyLogSwitch(  
    [in] WCHAR *pLogSwitchName,  
    [in] LONG  lLevel);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ac04c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac04c-105">Parameters</span></span>  
 `pLogSwitchName`  
 <span data-ttu-id="ac04c-106">[in] Un pointeur vers une chaîne qui spécifie le nom du commutateur de journal.</span><span class="sxs-lookup"><span data-stu-id="ac04c-106">[in] A pointer to a string that specifies the name of the log switch.</span></span>  
  
 `lLevel`  
 <span data-ttu-id="ac04c-107">[in] Le niveau de gravité à définir pour le commutateur de journal spécifié.</span><span class="sxs-lookup"><span data-stu-id="ac04c-107">[in] The severity level to be set for the specified log switch.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ac04c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ac04c-108">Remarks</span></span>  
 <span data-ttu-id="ac04c-109">Cette méthode est valide uniquement après la [ICorDebugManagedCallback::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createprocess-method.md) rappel s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ac04c-109">This method is valid only after the [ICorDebugManagedCallback::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createprocess-method.md) callback has occurred.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ac04c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac04c-110">Requirements</span></span>  
 <span data-ttu-id="ac04c-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ac04c-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ac04c-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ac04c-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ac04c-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ac04c-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ac04c-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ac04c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
