---
title: ICorDebugProcess2::GetDesiredNGENCompilerFlags, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2.GetDesiredNGENCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2::GetDesiredNGENCompilerFlags
helpviewer_keywords:
- ICorDebugProcess2::GetDesiredNGENCompilerFlags method [.NET Framework debugging]
- GetDesiredNGENCompilerFlags method [.NET Framework debugging]
ms.assetid: fc834580-3a90-4315-95d2-349b6bb7d059
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a59067f72005e87152680e4f990fc74e4acdaa9b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61948913"
---
# <a name="icordebugprocess2getdesiredngencompilerflags-method"></a><span data-ttu-id="ae68c-102">ICorDebugProcess2::GetDesiredNGENCompilerFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="ae68c-102">ICorDebugProcess2::GetDesiredNGENCompilerFlags Method</span></span>
<span data-ttu-id="ae68c-103">Obtient le compilateur actuel indicateur des paramètres utilisés par le common language runtime (CLR) pour sélectionner le bon précompilé (autrement dit, native) l’image à charger dans ce processus.</span><span class="sxs-lookup"><span data-stu-id="ae68c-103">Gets the current compiler flag settings that the common language runtime (CLR) uses to select the correct precompiled (that is, native) image to be loaded into this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae68c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae68c-104">Syntax</span></span>  
  
```  
HRESULT GetDesiredNGENCompilerFlags (  
    [out] DWORD   *pdwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ae68c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae68c-105">Parameters</span></span>  
 `pdwFlags`  
 <span data-ttu-id="ae68c-106">[out] Un pointeur vers une combinaison au niveau du bit de la [CorDebugJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md) valeurs d’énumération qui sont utilisés pour sélectionner l’image précompilée correcte à charger.</span><span class="sxs-lookup"><span data-stu-id="ae68c-106">[out] A pointer to a bitwise combination of the [CorDebugJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md) enumeration values that are used to select the correct precompiled image to be loaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ae68c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ae68c-107">Remarks</span></span>  
 <span data-ttu-id="ae68c-108">Utiliser le [ICorDebugProcess2::SetDesiredNGENCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-setdesiredngencompilerflags-method.md) méthode pour définir les indicateurs qui utilisera le CLR pour sélectionner l’image précompilée correcte à charger.</span><span class="sxs-lookup"><span data-stu-id="ae68c-108">Use the [ICorDebugProcess2::SetDesiredNGENCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-setdesiredngencompilerflags-method.md) method to set the flags that the CLR will use to select the correct pre-compiled image to load.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae68c-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae68c-109">Requirements</span></span>  
 <span data-ttu-id="ae68c-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ae68c-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae68c-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ae68c-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ae68c-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ae68c-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ae68c-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae68c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
