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
ms.openlocfilehash: 71722293bfb80a7e57393916560f922d970ea2ab
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33415640"
---
# <a name="icordebugmoduleenablejitdebugging-method"></a><span data-ttu-id="16146-102">ICorDebugModule::EnableJITDebugging, méthode</span><span class="sxs-lookup"><span data-stu-id="16146-102">ICorDebugModule::EnableJITDebugging Method</span></span>
<span data-ttu-id="16146-103">Contrôle si le compilateur (JIT) juste-à-temps conserve les informations de débogage pour les méthodes de ce module.</span><span class="sxs-lookup"><span data-stu-id="16146-103">Controls whether the just-in-time (JIT) compiler preserves debugging information for methods within this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="16146-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16146-104">Syntax</span></span>  
  
```  
HRESULT EnableJITDebugging(  
    [in] BOOL bTrackJITInfo,  
    [in] BOOL bAllowJitOpts  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="16146-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16146-105">Parameters</span></span>  
 `bTrackJITInfo`  
 <span data-ttu-id="16146-106">[in] Définissez cette valeur sur `true` pour permettre au compilateur JIT de conserver les informations de mappage entre la version de langage intermédiaire (MSIL) de Microsoft et de la version de compilation JIT de chaque méthode dans ce module.</span><span class="sxs-lookup"><span data-stu-id="16146-106">[in] Set this value to `true` to enable the JIT compiler to preserve mapping information between the Microsoft intermediate language (MSIL) version and the JIT-compiled version of each method in this module.</span></span>  
  
 `bAllowJitOpts`  
 <span data-ttu-id="16146-107">[in] Définissez cette valeur sur `true` pour permettre au compilateur JIT de générer du code avec certaines optimisations spécifiques au JIT pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="16146-107">[in] Set this value to `true` to enable the JIT compiler to generate code with certain JIT-specific optimizations for debugging.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="16146-108">Notes</span><span class="sxs-lookup"><span data-stu-id="16146-108">Remarks</span></span>  
 <span data-ttu-id="16146-109">Débogage JIT est activé par défaut pour tous les modules qui sont chargés lorsque le débogueur est actif.</span><span class="sxs-lookup"><span data-stu-id="16146-109">JIT debugging is enabled by default for all modules that are loaded when the debugger is active.</span></span> <span data-ttu-id="16146-110">Par programmation l’activation ou désactivation des paramètres substitue les paramètres globaux.</span><span class="sxs-lookup"><span data-stu-id="16146-110">Programmatically enabling or disabling the settings overrides global settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="16146-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="16146-111">Requirements</span></span>  
 <span data-ttu-id="16146-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="16146-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="16146-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="16146-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="16146-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="16146-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="16146-115">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="16146-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
