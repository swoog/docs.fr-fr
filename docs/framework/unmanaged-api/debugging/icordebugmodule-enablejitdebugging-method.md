---
title: ICorDebugModule::EnableJITDebugging, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.EnableJITDebugging
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::EnableJITDebugging
helpviewer_keywords:
- ICorDebugModule::EnableJITDebugging method [.NET Framework debugging]
- EnableJITDebugging method [.NET Framework debugging]
ms.assetid: 0a65e2a4-5bb6-496c-ae6f-40474426b5a6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 642c4fd600d10ef89a08aa32bef5c8e7455552c7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61937174"
---
# <a name="icordebugmoduleenablejitdebugging-method"></a><span data-ttu-id="1cfaf-102">ICorDebugModule::EnableJITDebugging, méthode</span><span class="sxs-lookup"><span data-stu-id="1cfaf-102">ICorDebugModule::EnableJITDebugging Method</span></span>
<span data-ttu-id="1cfaf-103">Contrôle si le compilateur juste-à-temps (JIT) conserve des informations de débogage pour les méthodes de ce module.</span><span class="sxs-lookup"><span data-stu-id="1cfaf-103">Controls whether the just-in-time (JIT) compiler preserves debugging information for methods within this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1cfaf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cfaf-104">Syntax</span></span>  
  
```  
HRESULT EnableJITDebugging(  
    [in] BOOL bTrackJITInfo,  
    [in] BOOL bAllowJitOpts  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1cfaf-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cfaf-105">Parameters</span></span>  
 `bTrackJITInfo`  
 <span data-ttu-id="1cfaf-106">[in] Définissez cette valeur sur `true` pour permettre au compilateur JIT de conserver les informations de mappage entre la version de Microsoft intermediate language (MSIL) et la version compilé par JIT de chaque méthode dans ce module.</span><span class="sxs-lookup"><span data-stu-id="1cfaf-106">[in] Set this value to `true` to enable the JIT compiler to preserve mapping information between the Microsoft intermediate language (MSIL) version and the JIT-compiled version of each method in this module.</span></span>  
  
 `bAllowJitOpts`  
 <span data-ttu-id="1cfaf-107">[in] Définissez cette valeur sur `true` pour permettre au compilateur JIT générer du code avec certaines optimisations spécifiques au JIT pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="1cfaf-107">[in] Set this value to `true` to enable the JIT compiler to generate code with certain JIT-specific optimizations for debugging.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1cfaf-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1cfaf-108">Remarks</span></span>  
 <span data-ttu-id="1cfaf-109">Le débogage JIT est activé par défaut pour tous les modules sont chargés lorsque le débogueur est actif.</span><span class="sxs-lookup"><span data-stu-id="1cfaf-109">JIT debugging is enabled by default for all modules that are loaded when the debugger is active.</span></span> <span data-ttu-id="1cfaf-110">Par programmation l’activation ou désactivation des paramètres substitue les paramètres globaux.</span><span class="sxs-lookup"><span data-stu-id="1cfaf-110">Programmatically enabling or disabling the settings overrides global settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1cfaf-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cfaf-111">Requirements</span></span>  
 <span data-ttu-id="1cfaf-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1cfaf-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1cfaf-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1cfaf-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1cfaf-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1cfaf-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1cfaf-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1cfaf-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
