---
title: ICorDebugThread4::GetCurrentCustomDebuggerNotification, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread4.GetCurrentCustomDebuggerNotification Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread4::GetCurrentCustomDebuggerNotification
helpviewer_keywords:
- GetCurrentCustomDebuggerNotification method [.NET Framework debugging]
- ICorDebugThread4::GetCurrentCustomDebuggerNotification method [.NET Framework debugging]
ms.assetid: 57e0f2d2-5f0e-4e2d-99ec-3f26632eb693
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f626ff6e562bd9bc94440f31e9470a45cc32cfbd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59216325"
---
# <a name="icordebugthread4getcurrentcustomdebuggernotification-method"></a><span data-ttu-id="48788-102">ICorDebugThread4::GetCurrentCustomDebuggerNotification, méthode</span><span class="sxs-lookup"><span data-stu-id="48788-102">ICorDebugThread4::GetCurrentCustomDebuggerNotification Method</span></span>

<span data-ttu-id="48788-103">Obtient les valeurs combinées [ICorDebugManagedCallback3::CustomNotification](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md) objet sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="48788-103">Gets the current [ICorDebugManagedCallback3::CustomNotification](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md) object on the current thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="48788-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48788-104">Syntax</span></span>

```cpp
HRESULT GetCurrentCustomDebuggerNotification(
    [out] ICorDebugValue **ppNotificationObject
    );
```

## <a name="parameters"></a><span data-ttu-id="48788-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48788-105">Parameters</span></span>

`ppNotificationObject`\
<span data-ttu-id="48788-106">[out] Un pointeur vers l’actuel `ICorDebugManagedCallback3::CustomNotification` objet sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="48788-106">[out] A pointer to the current `ICorDebugManagedCallback3::CustomNotification` object on the current thread.</span></span>

## <a name="remarks"></a><span data-ttu-id="48788-107">Notes</span><span class="sxs-lookup"><span data-stu-id="48788-107">Remarks</span></span>

<span data-ttu-id="48788-108">La valeur de `ppNotificationObject` a la valeur null si la méthode n’est pas appelée depuis un `ICorDebugManagedCallback3::CustomNotification` rappel, ou si aucun objet de notification en cours n’existe.</span><span class="sxs-lookup"><span data-stu-id="48788-108">The value of `ppNotificationObject` is null if the method is not called from within a `ICorDebugManagedCallback3::CustomNotification` callback, or if no current notification object exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="48788-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48788-109">Requirements</span></span>

<span data-ttu-id="48788-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="48788-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="48788-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="48788-111">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="48788-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="48788-112">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="48788-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="48788-113">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="48788-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48788-114">See also</span></span>

- [<span data-ttu-id="48788-115">ICorDebugThread4, interface</span><span class="sxs-lookup"><span data-stu-id="48788-115">ICorDebugThread4 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread4-interface.md)
- [<span data-ttu-id="48788-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="48788-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="48788-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="48788-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
