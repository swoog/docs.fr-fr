---
title: ICorDebugProcess3::SetEnableCustomNotification, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess3.SetEnableCustomNotification Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess3::SetEnableCustomNotification
helpviewer_keywords:
- ICorDebugProcess3::SetEnableCustomNotification method [.NET Framework debugging]
- SetEnableCustomNotification method [.NET Framework debugging]
ms.assetid: afd88ee9-2589-4461-a75a-9b6fe55a2525
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e8c8725bf21aefa3abf5fc41366d8f983bd686b2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59175745"
---
# <a name="icordebugprocess3setenablecustomnotification-method"></a><span data-ttu-id="58901-102">ICorDebugProcess3::SetEnableCustomNotification, méthode</span><span class="sxs-lookup"><span data-stu-id="58901-102">ICorDebugProcess3::SetEnableCustomNotification Method</span></span>
<span data-ttu-id="58901-103">Active et désactive les notifications de débogueur personnalisées du type spécifié.</span><span class="sxs-lookup"><span data-stu-id="58901-103">Enables and disables custom debugger notifications of the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58901-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58901-104">Syntax</span></span>  
  
```  
HRESULT SetEnableCustomNotification(ICorDebugClass * pClass,  
                                    BOOL fEnable);  
```  
  
## <a name="parameters"></a><span data-ttu-id="58901-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58901-105">Parameters</span></span>  
 `pClass`  
 <span data-ttu-id="58901-106">[in] Type qui spécifie les notifications de débogueur personnalisées.</span><span class="sxs-lookup"><span data-stu-id="58901-106">[in] The type that specifies custom debugger notifications.</span></span>  
  
 `fEnable`  
 <span data-ttu-id="58901-107">[in] `true` pour activer les notifications de débogueur personnalisées ; `false` pour désactiver les notifications.</span><span class="sxs-lookup"><span data-stu-id="58901-107">[in] `true` to enable custom debugger notifications; `false` to disable notifications.</span></span> <span data-ttu-id="58901-108">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="58901-108">The default value is `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="58901-109">Notes</span><span class="sxs-lookup"><span data-stu-id="58901-109">Remarks</span></span>  
 <span data-ttu-id="58901-110">Lorsque `fEnable` a la valeur `true`, les appels à la <xref:System.Diagnostics.Debugger.NotifyOfCrossThreadDependency%2A?displayProperty=nameWithType> déclencheur de la méthode un [ICorDebugManagedCallback3::CustomNotification](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="58901-110">When `fEnable` is set to `true`, calls to the <xref:System.Diagnostics.Debugger.NotifyOfCrossThreadDependency%2A?displayProperty=nameWithType> method trigger an [ICorDebugManagedCallback3::CustomNotification](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md) callback.</span></span> <span data-ttu-id="58901-111">Notifications sont désactivées par défaut ; Par conséquent, le débogueur doit spécifier les types de notification qu’il connaît et souhaite gérer.</span><span class="sxs-lookup"><span data-stu-id="58901-111">Notifications are disabled by default; therefore, the debugger must specify any notification types it knows about and wants to handle.</span></span> <span data-ttu-id="58901-112">Étant donné que le [ICorDebugClass](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) classe est délimitée par le domaine d’application, le débogueur doit appeler `SetEnableCustomNotification` pour chaque domaine d’application dans le processus s’il souhaite recevoir la notification de l’ensemble du processus.</span><span class="sxs-lookup"><span data-stu-id="58901-112">Because the [ICorDebugClass](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) class is scoped by application domain, the debugger must call `SetEnableCustomNotification` for every application domain in the process if it wants to receive the notification across the entire process.</span></span>  
  
 <span data-ttu-id="58901-113">En commençant par le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)], la seule notification prise en charge est une notification de dépendance inter-threads.</span><span class="sxs-lookup"><span data-stu-id="58901-113">Starting with the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)], the only supported notification is a cross-thread dependency notification.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="58901-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58901-114">Requirements</span></span>  
 <span data-ttu-id="58901-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="58901-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="58901-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="58901-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="58901-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="58901-117">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="58901-118">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="58901-118">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="58901-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58901-119">See also</span></span>

- [<span data-ttu-id="58901-120">ICorDebugProcess3, interface</span><span class="sxs-lookup"><span data-stu-id="58901-120">ICorDebugProcess3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess3-interface.md)
- [<span data-ttu-id="58901-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="58901-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="58901-122">Débogage</span><span class="sxs-lookup"><span data-stu-id="58901-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
