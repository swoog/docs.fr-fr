---
title: Méthode ICoreClrDebugTarget::FreeMemory
ms.date: 03/30/2017
api_name:
- ICoreDebugTarget.FreeMemory
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- ICoreClrDebugTarget::FreeMemory
helpviewer_keywords:
- remote debugging API [Silverlight]
- FreeMemory method, ICoreClrDebugTarget interface [Silverlight debugging]
- ICorClrDebugTarget::FreeMemory method [Silverlight debugging]
- Silverlight, remote debugging
ms.assetid: 98f2a0db-a6ec-4f9b-861d-f82485237d08
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ec156ca7590a2ec637cb59e022fc2dd1a71226e0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61993577"
---
# <a name="icoreclrdebugtargetfreememory-method"></a><span data-ttu-id="a4cd6-102">Méthode ICoreClrDebugTarget::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="a4cd6-102">ICoreClrDebugTarget::FreeMemory Method</span></span>
<span data-ttu-id="a4cd6-103">Libère la mémoire allouée par le [ICoreClrDebugTarget::EnumProcesses](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumprocesses-method.md) et [ICoreClrDebugTarget::EnumRuntimes](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumruntimes-method.md) méthodes.</span><span class="sxs-lookup"><span data-stu-id="a4cd6-103">Frees the memory allocated by the [ICoreClrDebugTarget::EnumProcesses](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumprocesses-method.md) and [ICoreClrDebugTarget::EnumRuntimes](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumruntimes-method.md) methods.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4cd6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4cd6-104">Syntax</span></span>  
  
```  
void FreeMemory (  
     [in] void*pMemory);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a4cd6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4cd6-105">Parameters</span></span>  
 `pMemory`  
 <span data-ttu-id="a4cd6-106">[in] Un pointeur vers le tableau qui est retourné par la [ICoreClrDebugTarget::EnumProcesses](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumprocesses-method.md) ou [ICoreClrDebugTarget::EnumRuntimes](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumruntimes-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="a4cd6-106">[in] A pointer to the array that is returned by either the [ICoreClrDebugTarget::EnumProcesses](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumprocesses-method.md) or the [ICoreClrDebugTarget::EnumRuntimes](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumruntimes-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a4cd6-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4cd6-107">Requirements</span></span>  
 <span data-ttu-id="a4cd6-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a4cd6-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a4cd6-109">**En-tête :** CoreClrRemoteDebuggingInterfaces.h</span><span class="sxs-lookup"><span data-stu-id="a4cd6-109">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="a4cd6-110">**Bibliothèque :** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="a4cd6-110">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="a4cd6-111">**Versions du .NET framework :** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="a4cd6-111">**.NET Framework Versions:** 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a4cd6-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4cd6-112">See also</span></span>

- [<span data-ttu-id="a4cd6-113">ICoreClrDebugTarget, interface</span><span class="sxs-lookup"><span data-stu-id="a4cd6-113">ICoreClrDebugTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-interface.md)
