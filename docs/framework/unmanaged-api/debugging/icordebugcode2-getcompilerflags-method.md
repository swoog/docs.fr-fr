---
title: ICorDebugCode2::GetCompilerFlags, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCode2.GetCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode2::GetCompilerFlags
helpviewer_keywords:
- GetCompilerFlags method [.NET Framework debugging]
- ICorDebugCode2::GetCompilerFlags method [.NET Framework debugging]
ms.assetid: 532e9dfd-d114-4c75-b952-1accce102643
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2dc6344616dfa5e633fca140ab2dab2b95c81a4b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33411280"
---
# <a name="icordebugcode2getcompilerflags-method"></a><span data-ttu-id="073b2-102">ICorDebugCode2::GetCompilerFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="073b2-102">ICorDebugCode2::GetCompilerFlags Method</span></span>
<span data-ttu-id="073b2-103">Obtient les indicateurs qui spécifient les conditions dans lesquelles cet objet de code a été soit juste-à-temps (JIT) compilé ou généré à l’aide du Générateur d’images natives (Ngen.exe).</span><span class="sxs-lookup"><span data-stu-id="073b2-103">Gets the flags that specify the conditions under which this code object was either just-in-time (JIT) compiled or generated using the native image generator (Ngen.exe).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="073b2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="073b2-104">Syntax</span></span>  
  
```  
HRESULT GetCompilerFlags (  
    [out] DWORD *pdwFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="073b2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="073b2-105">Parameters</span></span>  
 `pdwFlags`  
 <span data-ttu-id="073b2-106">[out] Un pointeur vers une valeur de la [CorDebugJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md) énumération qui spécifie le comportement du compilateur JIT ou le Générateur d’images natives.</span><span class="sxs-lookup"><span data-stu-id="073b2-106">[out] A pointer to a value of the [CorDebugJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md) enumeration that specifies the behavior of the JIT compiler or the native image generator.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="073b2-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="073b2-107">Requirements</span></span>  
 <span data-ttu-id="073b2-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="073b2-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="073b2-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="073b2-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="073b2-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="073b2-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="073b2-111">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="073b2-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="073b2-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="073b2-112">See Also</span></span>  
 
